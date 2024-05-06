### Server
![img.png](img.png)

### Client 1
![img_1.png](img_1.png)

### Client 2
![img_2.png](img_2.png)

### Client 3
![img_3.png](img_3.png)

Untuk menjalankannya, saya menjalankan perintah `cargo run --bin server` untuk menjalankan server. Lalu, saya 
menjalankan perintah `cargo run --bin client` pada 3 terminal yang berbeda untuk menjalankan 3 client. Ketika saya 
mengirimkan sebuah message dari client 1, message tersebut akan di-broadcat oleh server ke client lainnya, begitu juga 
saat saya mengirimkan message dari client lainnya.