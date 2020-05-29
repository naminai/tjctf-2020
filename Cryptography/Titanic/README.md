# Titanic
## Description 
I wrapped tjctf{} around the lowercase version of a word said in the 1997 film "Titanic" and created an MD5 hash of it: 9326ea0931baf5786cde7f280f965ebb

## Solution
Disini, kita mengetahui bahwa flag semuanya terdiri dari lowercase dan kemungkinan tidak memiliki angka di dalamnya, dikarenakan merupakan sebuah kata yang "diucapkan". Pertama-tama, kita tahu bahwa terdapat spesial karakter pada plaintext, karena hash decryptor tidak berhasil men-decrypt. Lalu, kita coba download subtitle untuk Titanic <a href=https://yts-subs.com/movie-imdb/tt0120338>disini</a>. 
<br><br>
Kemudian kita gunakan bruteforce untuk mencari seluruh kata yang memiliki spesial character dan kita bungkus semua kata itu dengan format `tjctf{kata_spesial}`. Hasilnya kita dapatkan flag dengan keyword `marlborough's` setelah kita cocokkan pada MD5 Hasher.

![image](https://user-images.githubusercontent.com/61267430/83221042-eeb58680-a19e-11ea-9ab4-886e79699ab4.png)


## Flag
tjctf{marlborough's}