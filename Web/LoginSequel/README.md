# Login Sequel
## Description 
<a href=http://login_sequel.tjctf.org/>Login</a> as admin you must. This time, the client is of no use :(. What to do?

## Solution
Berdasarkan problem description, kita sepertinyua diharapkan masuk sebagai username admin. Kemudian kita bisa mengetahui bagaimana proses login bekerja.
![image](https://user-images.githubusercontent.com/61267430/83213788-39c69e00-a18d-11ea-8b98-57bd883203d9.png)
<br>
Kita mengetahui bahwa script diatas sangat rentan terhadap SQL Injection attack, kemudian saya coba meng-inject ke login-nya.

![image](https://user-images.githubusercontent.com/61267430/83213876-6f6b8700-a18d-11ea-82e0-8c1001fc99e3.png)
<br>
Sayangnya, terdeteksi SQL Injection ketika kita menginputkan AND atau OR pada form. Kemudian kita coba SQL Comment Injection dengan menginput admin'/* , pada username, dan */ , pada password sehingga tidak memerlukan password untuk login, dan kita berhasil login:

![image](https://user-images.githubusercontent.com/61267430/83214010-c4a79880-a18d-11ea-8570-6965afff6271.png)


## Flag
tjctf{W0w_wHa1_a_SqL1_exPeRt!}