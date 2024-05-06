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

### Mengganti port menjadi 8080
![img_4.png](img_4.png)

Pada file server.rs, kita juga perlu mengganti port websocket menjadi 8080 agar message dari client dapat di-broadcast. 
Port tersebut didefinisikan di function main dan disimpan pada variabel `listener`

### Menambahkan informasi IP pada client
#### Client 1
![img_5.png](img_5.png)

#### Client 2
![img_6.png](img_6.png)

Saya mengganti isi teks yang akan di-broadcast pada file server.rs menjadi `bcast_tx.send(format!("{addr} : {text}"))?;`
 untuk memberikan informasi IP asal message tersebut dikirimkan pada client.