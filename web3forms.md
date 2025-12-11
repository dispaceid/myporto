### Cara Memasang Form Web3Forms + hCaptcha
**Tingkat Kesulitan: Menengah**

1. **Sesuaikan kode form ke template website.**
   Salin hanya baris pertama dan kedua `form action` di bawah ini, lalu sesuaikan `access_key`, kemudian atribut `name` pada setiap input.

   > **Catatan:** Pastikan atribut `name` (contoh: `name="email"`) sesuai dengan data yang ingin Anda tangkap.

   **Kode Form Lengkap:**
   ```html
   <form action="https://api.web3forms.com/submit" method="POST">
       <input type="hidden" name="access_key" value="KEY_ANDA">

       <input type="text" name="name" placeholder="Nama Anda" required>

       <input type="email" name="email" placeholder="Alamat Email" required>

       <textarea name="message" placeholder="Pesan Anda" required></textarea>

       <div class="h-captcha" data-captcha="true"></div>

       <button type="submit">Kirim Pesan</button>
   </form>


2.  **Tambahkan Script Client.**
    Letakkan kode berikut tepat sebelum tag penutup `</body>` pada file HTML Anda agar hCaptcha berfungsi:

    ```html
    <script src="https://web3forms.com/client/script.js" async defer></script>
    ```
