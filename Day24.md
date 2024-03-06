
**Rangkuman React State Management:**
  
React state management adalah proses mengelola dan menyimpan data dalam aplikasi React agar dapat diakses dan diperbarui dengan mudah. Dalam React, state merujuk pada data dinamis yang dikelola oleh komponen. State biasanya digunakan untuk menyimpan informasi seperti input pengguna, status aplikasi, atau data yang diperoleh dari backend.

1. **React Context:**
Context adalah cara untuk membagikan data ke dalam pohon komponen React tanpa perlu meneruskan prop secara eksplisit ke setiap tingkat komponen. Ini memungkinkan komponen-komponen dalam aplikasi untuk mengakses data secara global.
   - **Membuat Konteks dengan Fungsi createContext:**
		`createContext()` adalah fungsi yang disediakan oleh React untuk membuat sebuah konteks baru.
     ```jsx
     const MyContext = createContext();
     ```
   - **Membungkus Komponen Halaman dengan Context Provider:**
	   Komponen yang ingin mengakses data atau function pada konteks harus dibungkus dengan `<MyContext.Provider>`. Properti `value` yang diberikan kepada Provider akan diturunkan ke semua komponen yang berada dalam hirarki konteks tersebut.
     ```jsx
     <MyContext.Provider value={value}>
       {/* Komponen-komponen di dalamnya */}
     </MyContext.Provider>
     ```
   - **Mengonsumsi Konteks dengan Hook useContext:**
	   `useContext()` adalah hook yang disediakan oleh React untuk mengonsumsi nilai dari suatu konteks.
     ```jsx
     const value = useContext(MyContext);
     ```

2. **Redux:**
Redux adalah library untuk state management. Redux menyediakan struktur yang jelas untuk mengatur state aplikasi dan memungkinkan pengelolaan state yang kompleks dengan baik. Redux menggunakan konsep store, actions, dan reducers untuk mengelola state secara terpusat.
   - **Konfigurasi Dasar Store:**
	Store pada Redux adalah objek yang menyimpan seluruh state aplikasi. Dibuat menggunakan fungsi `createStore()` yang disediakan oleh Redux. Ini menerima reducer sebagai argumen.
     ```jsx
     import { createStore } from 'redux';
     const store = createStore(reducer);
     ```
   - **Membuat Fungsi Reducer dengan Switch Case:**
	   Reducer adalah fungsi yang mengatur perubahan pada state dalam store Redux. Ini menerima dua argumen: state saat ini dan aksi yang dipicu. Pada dasarnya, reducer berisi switch case yang menangani tipe-tipe aksi yang dapat mempengaruhi state.
     ```jsx
     const initialState = { count: 0 };

     function counterReducer(state = initialState, action) {
       switch (action.type) {
         case 'INCREMENT':
           return { count: state.count + 1 };
         case 'DECREMENT':
           return { count: state.count - 1 };
         default:
           return state;
       }
     }
     ```
   - **Catatan: State Redux Bersifat Imutabel (Tidak Dapat Diubah):**
	   Redux menerapkan prinsip bahwa state bersifat imutabel, artinya state tidak dapat diubah langsung. Untuk memperbarui state, kita harus membuat salinan baru dari state yang ada dan mengembalikan salinan tersebut.
     ```jsx
     // Contoh: Tidak dapat melakukan perubahan langsung pada state
     // state.count++;
     ```
   - **Mengonsumsi State dengan Hook useSelector:**
	   `useSelector()` adalah hook yang disediakan oleh React Redux untuk mengambil data dari store Redux. Ini memungkinkan komponen untuk mengakses bagian tertentu dari state global.
     ```jsx
     const count = useSelector(state => state.count);
     ```
   - **Memperbarui State dengan Hook useDispatch:**
	   `useDispatch()` adalah hook yang disediakan oleh React Redux untuk memanggil aksi (actions) dalam store Redux. Ini memungkinkan komponen untuk memicu perubahan pada state dengan cara mengirim aksi ke store.
     ```jsx
     const dispatch = useDispatch();
     const increment = () => dispatch({ type: 'INCREMENT' });
     ```

3. **Membuat Reducer dengan createSlice dari Redux Toolkit:**
   - Redux Toolkit menyediakan `createSlice` untuk membuat slice reducer dengan konfigurasi yang lebih sederhana.
	   ```jsx
	   import { createSlice } from '@reduxjs/toolkit';

	   const counterSlice = createSlice({
	     name: 'counter',
	     initialState: { value: 0 },
	     reducers: {
	       increment: state => {
	         state.value += 1;
	       },
	       decrement: state => {
	         state.value -= 1;
	       },
	     },
	   });

	   export const { increment, decrement } = counterSlice.actions;
	   export default counterSlice.reducer;
	   ```

