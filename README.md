# Reflection Module 6

### Commit 1

Fungsi `handle_connection` bekerja mengatur aliran data dari TCP. Caranya, fungsi `handle_connection` mengambil data dari `TcpStream`, dan memakai `BufReader` untuk membaca datanya supaya lebih gampang dan cepat. `handle_connection` membaca terus menerus sampai menemukan baris yang kosong, soalnya di format HTTP, baris kosong tandanya sudah selesai bagian awalnya. Dan semua yang dibaca tadi tersimpan ke dalam satu tempat, jadi kayak kumpulan permintaan HTTP. Terus, di akhir, `handle_connection` menunjukkan apa yang sudah dikumpulin tadi. Jadi, intinya, dia mengurus data dari TCP, baca per baris, terus mengumpulkan sampai ketemu baris kosong, dan akan menunjukkan hasilnya.