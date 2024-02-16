## Form Handling

**Controlled Input:**
   - **Mengontrol Satu Input pada Satu State:**
     ```jsx
     const [name, setName] = useState('');

     <input type="text" value={name} onChange={(e) => setName(e.target.value)} />
     ```
   - **Mengontrol Banyak Input pada Satu State:**
     ```jsx
     const [formData, setFormData] = useState({ username: '', password: '' });

     <input type="text" value={formData.username} onChange={(e) => setFormData({ ...formData, username: e.target.value })} />
     <input type="password" value={formData.password} onChange={(e) => setFormData({ ...formData, password: e.target.value })} />
     ```
   - **Mengontrol Input Jenis Lainnya (select, radio, checkbox, dll):**
     ```jsx
     const [selectedOption, setSelectedOption] = useState('');

     <select value={selectedOption} onChange={(e) => setSelectedOption(e.target.value)}>
       <option value="option1">Option 1</option>
       <option value="option2">Option 2</option>
     </select>
     ```

**Membungkus Input Menggunakan Elemen Form HTML:**
   - **Menangani Pengiriman Form menggunakan onSubmit Event:**
     ```jsx
     const handleSubmit = (e) => {
       e.preventDefault();
       // Lakukan sesuatu dengan data form
     };

     <form onSubmit={handleSubmit}>
       {/* Input fields */}
       <button type="submit">Submit</button>
     </form>
     ```
   - **Menggunakan event.preventDefault() Untuk Mencegah Reload:**
     ```jsx
     const handleSubmit = (e) => {
       e.preventDefault();
       // Lakukan sesuatu dengan data form
     };
     ```
   - **Validasi Input Menggunakan Atribut Validasi HTML Bawaan:**
     ```jsx
     <input type="email" required />
     ```

**Menggunakan React Hook Form untuk Mengontrol Input:**
   - React Hook Form adalah library yang digunakan untuk mengelola form dalam React secara efisien.
   - Contoh:
     ```jsx
     const { register, handleSubmit } = useForm();

     <form onSubmit={handleSubmit(onSubmit)}>
       <input type="text" {...register('username', { required: true })} />
       <button type="submit">Submit</button>
     </form>
     ```

**Validasi Input Menggunakan YUP + React Hook Form:**
   - YUP adalah library validasi schema yang kompatibel dengan React Hook Form.
   - Contoh:
     ```jsx
     const schema = yup.object().shape({
       username: yup.string().required(),
       password: yup.string().required().min(6),
     });

     <form onSubmit={handleSubmit(onSubmit)}>
       <input type="text" {...register('username')} />
       <input type="password" {...register('password')} />
       <button type="submit">Submit</button>
     </form>
     ```

**Mengirim Data Input ke REST API Menggunakan HTTP Client:**
   - Menggunakan axios atau fetch untuk mengirim data input ke REST API.
   - Contoh menggunakan Axios:
     ```jsx
     const handleSubmit = async (formData) => {
       try {
         const response = await axios.post('https://api.example.com/data', formData);
         console.log('Data berhasil dikirim:', response.data);
       } catch (error) {
         console.error('Error:', error);
       }
     };
     ```


