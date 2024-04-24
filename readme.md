# Spring Security with JWT

Urutan : User ⇄ AuthFilter ⇄ Auth Manager ⇄ Auth Provider ⇄ UserDetailService 
              ⇄ Security Context
1. User send request 
2. Setelah itu di filter oleh authfilter
3. Dikirim ke auth manager 
4. Diikirim ke auth provider 
5. setelah berhasil dicocokan makan akan dikirimkan ke uth Provider ⇄ Auth Manager ⇄ AuthFilter
6. Token (jika dia berhasil membuktikan bahwa dia adalah sang user itu sendiri), Token digunakan untuk mengakses endpoint yg tersedia tanpa melalui filter security lagi
    tinggal menggunakan token untuk mengakses endpoint yang tersedia ( token juga memiliki kadaluarwsa )
## Filter Chain 
Filter chain digunakan untuk memfilter any request sebelum dia hit service atau code base kita