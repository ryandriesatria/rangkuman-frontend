## **Lifecycle:**
**Functional Component Lifecycle:**
 - Komponen fungsional tidak memiliki siklus hidup, tetapi dapat menggunakan Hooks `useEffect` untuk menangani efek samping.

**useEffect Hooks:**
- Digunakan untuk menjalankan efek samping dalam komponen fungsional.
	```jsx
	import React, { useEffect } from 'react';

	function MyComponent() {
	  useEffect(() => {
	    // Efek samping disini
	    return () => {
	      // Membersihkan efek samping disini
	    };
	  }, [dependency]);
	}
	```

 **Multiple useEffect dalam Satu Komponen:**
- Menggunakan Hooks `useEffect` beberapa kali dalam satu komponen.
	```jsx
	useEffect(() => {
	  // Efek samping pertama
	}, [dependency1]);

	useEffect(() => {
	  // Efek samping kedua
	}, [dependency2]);
	```


## Data Fetching
**Rangkuman React.js Data Fetching:**

**Membuat Dummy API Menggunakan JSON Server:**
   - JSON Server adalah alat untuk membuat server API palsu dengan menggunakan file JSON sebagai sumber datanya.
   - Menggunakan JSON Server memungkinkan pengembang untuk membuat API palsu dengan cepat untuk keperluan pengembangan dan pengujian.
   
 **Melakukan Permintaan ke REST API Menggunakan Library HTTP Client:**
   - **Menggunakan Axios:**
     Axios adalah library HTTP client yang populer dan mudah digunakan dalam React.
     ```javascript
     import axios from 'axios';

     axios.get('https://api.example.com/data')
       .then(response => console.log(response.data))
       .catch(error => console.error('Error:', error));
     ```
   - **Menggunakan Fetch:**
     Fetch adalah API bawaan browser yang digunakan untuk melakukan permintaan HTTP.
     ```javascript
     fetch('https://api.example.com/data')
       .then(response => response.json())
       .then(data => console.log(data))
       .catch(error => console.error('Error:', error));
     ```

 **Menyimpan Data Tanggapan pada State:**
   - Menyimpan data yang diperoleh dari permintaan HTTP pada state React menggunakan useState hook.
   - Contoh:
     ```javascript
     const [data, setData] = useState(null);

     useEffect(() => {
       fetchData();
     }, []);

     const fetchData = async () => {
       const response = await axios.get('https://api.example.com/data');
       setData(response.data);
     };
     ```

 **Melakukan Permintaan dalam useEffect untuk Mengambil Data Halaman Awal:**
   - Menggunakan useEffect hook untuk melakukan permintaan saat komponen dimuat pertama kali.
   - Contoh:
     ```javascript
     useEffect(() => {
       fetchData();
     }, []);
     ```

 **Menampilkan Status Loading Selama Pengambilan Data Berlangsung:**
   - Menunjukkan elemen loading saat data sedang diambil dari server.
   - Contoh:
		```jsx
		const [loading, setLoading] = useState(true);

		useEffect(() => {
		  axios.get('https://jsonplaceholder.typicode.com/posts')
		    .then(response => {
		      setPosts(response.data);
		      setLoading(false);
		    })
		    .catch(error => {
		      console.error('Error:', error);
		      setLoading(false);
		    });
		}, []);

		return (
		  <div>
		    {loading ? <p>Loading...</p> : (
		      <ul>
		        {posts.map(post => (
		          <li key={post.id}>{post.title}</li>
		        ))}
		      </ul>
		    )}
		  </div>
		);
		```

 **Menggunakan Library Pengambilan Data React yang Tepat:**
   - **React SWR:**
     React SWR (Stale-While-Revalidate) adalah library pengambilan data yang memungkinkan pengguna untuk mengelola data dengan mudah dan efisien.
	    ```jsx
		const [loading, setLoading] = useState(true);

		useEffect(() => {
		  axios.get('https://jsonplaceholder.typicode.com/posts')
		    .then(response => {
		      setPosts(response.data);
		      setLoading(false);
		    })
		    .catch(error => {
		      console.error('Error:', error);
		      setLoading(false);
		    });
		}, []);

		return (
		  <div>
		    {loading ? <p>Loading...</p> : (
		      <ul>
		        {posts.map(post => (
		          <li key={post.id}>{post.title}</li>
		        ))}
		      </ul>
		    )}
		  </div>
		);
		```
   - **React Query:**
     React Query adalah library pengambilan data yang dirancang untuk penggunaan di React. Ini menyediakan banyak fitur seperti caching, pagination, dan refetching.
	    ```jsx
		import { useQuery } from 'react-query';

		const { data, isLoading, isError } = useQuery('posts', async () => {
		  const response = await axios.get('https://jsonplaceholder.typicode.com/posts');
		  return response.data;
		});

		if (isLoading) return <div>Loading...</div>;
		if (isError) return <div>Error loading data</div>;

		return (
		  <ul>
		    {data.map(post => (
		      <li key={post.id}>{post.title}</li>
		    ))}
		  </ul>
		);
		```


