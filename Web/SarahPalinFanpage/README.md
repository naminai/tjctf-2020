# Sarah Palin Fanpage
## Description 
Are you a true fan of Alaska's most famous governor? Visit the <a href=http://sarah_palin_fanpage.tjctf.org/>Sarah Palin fanpage</a>.

## Solution
Saya coba kunjungi situsnya, dan kita lihat di VIP Area terdapat batasan akses untuk masuk. Ternyata untuk bisa masuk harus me-like Sarah Palin Top 10 Moments. Namun, saya hanya bisa melakukan like hingga 5 kali sebelum akses di-deny sehingga tidak bisa lebih dari itu.

![image](https://user-images.githubusercontent.com/61267430/83214273-616a3600-a18e-11ea-81f4-6e67d964f05b.png)

Saya coba melihat di debugger ternyata ada file JavaScript bernama likes.js, saya berpikir mungkin ada kita bisa memanipulasi data likes disitu namun ternyata tidak membuahkan hasil.

![image](https://user-images.githubusercontent.com/61267430/83214416-bc039200-a18e-11ea-915c-477fa1eb9963.png)

Kemudian saya coba cek storage->cookies dan ternyata ada satu value yang tidak berubah selama berpindah tab atau browser, yaitu value dari `data`. Kemudian saya coba decode value-nya dengan Base64 Decoder.

![image](https://user-images.githubusercontent.com/61267430/83214483-e2293200-a18e-11ea-9e9c-6bdbd3c5bdb8.png)

Benar sekali, value data akan berubah apabila kita melakukan like, sehingga jika belum di like nilainya false dan jika sudah maka true, kemudian kita ganti semuanya menjadi true lalu kita encode ke Base64 lagi dan kita masukkan value baru itu ke data.

![image](https://user-images.githubusercontent.com/61267430/83214696-6976a580-a18f-11ea-9747-190f22922256.png)

Lalu kita dapatkan flag-nya.

![image](https://user-images.githubusercontent.com/61267430/83214745-827f5680-a18f-11ea-9349-e61d62641a5d.png)

## Flag
tjctf{wkDd2Pi4rxiRaM5lOcLo979rru8MFqVHKdTqPBm4k3iQd8n0sWbBkOfuq9vDTGN9suZgYlH3jq6QTp3tG3EYapzsTHL7ycqRTP5Qf6rQSB33DcQaaqwQhpbuqPBm4k3iQd8n0sWbBkOf}