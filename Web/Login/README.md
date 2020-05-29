# Login
## Description 
Could you login into this <a href=http://login.tjctf.org/>very secure site</a>? Best of luck!

## Solution
Kita masuk ke situs, kemudian kita dihadapkan pada login page. Bisa kita lihat pada script, terdapat beberapa hal penting:
- Bahwa username bernama admin
- Bahwa password di decode dengan menggunakan karakter hex.
![image](https://user-images.githubusercontent.com/61267430/83212726-76dd6100-a18a-11ea-8b10-078bb1e95910.png)
<br>
![image](https://user-images.githubusercontent.com/61267430/83212784-a68c6900-a18a-11ea-903d-0884a26212cc.png)
<br>
Dengan begini, kita mengkonfirmasi bahwa username adalah admin, dan dicocokkan dengan admin. Maka, kita tahu bahwa password-nya memang adalah hasil dari MD5 yang sudah diketahui diatas. Sekarang kita decode menggunakan MD5 Decoder Online dan kita dapatkan password-nya.
![image](https://user-images.githubusercontent.com/61267430/83212958-14d12b80-a18b-11ea-906b-c04041bfb366.png)
<br>
Setelah itu, kita masukkan username dan password dan kita dapatkan flag-nya.
<br>
![image](https://user-images.githubusercontent.com/61267430/83212996-316d6380-a18b-11ea-8cd4-748a0256d17e.png)

## Flag
tjctf{inevitable890898}