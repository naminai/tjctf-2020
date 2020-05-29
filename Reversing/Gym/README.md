# Gym
## Description 
Aneesh wants to acquire a summer bod for beach week, but time is running out. Can you help him <a href=https://static.tjctf.org/bed9d7b7327958dab4d07b06772a032f3e97455e310956558579e8838762b5e2_gym>create a plan</a> to attain his goal?

nc p1.tjctf.org 8008

## Solution
Disini kita bisa menjalankan file-nya, dan kita bisa mengetahui bahwa berat badan awal adalah 211 dan berat badan akhir haruslah 180.
<br>
![image](https://user-images.githubusercontent.com/61267430/83204181-68d11580-a175-11ea-8c9a-d479b9aefe86.png)
<br>
Permasalahnnya adalah kita tidak tahu penilaian option 1, 2, 3, dan 4 dan bagaimana pengaruhnya dalam penurunan berat badan. Maka dari itu, kita akan menggunakan IDA atau Interactive Disassembler untuk mendapatkan pseudo source code program.
<br>
![image](https://user-images.githubusercontent.com/61267430/83205046-ac2c8380-a177-11ea-9b3c-969b28a19bc4.png)  
<br>
Setelah itu, kita bisa mendapatkan C program-nya dengan menggunakan `IDA->Produce File->Create C file`. Setelah itu, kita lihat logic dari program-nya.
<br>
![image](https://user-images.githubusercontent.com/61267430/83205354-881d7200-a178-11ea-99bd-9c015ec3383f.png)
![image](https://user-images.githubusercontent.com/61267430/83205266-4b517b00-a178-11ea-9ab1-cd65d08fbc74.png)
<br>
Bisa kita lihat, bahwa terdapat nilai masing-masing option:
Option 1: 4
Option 2: 1
Option 3: 2
Option 4: 3

Dan beberapa kondisi:
Jika v3 (aktivitas) == 2, maka kurangi 1.
Jika v3 > 2, maka dicek lagi:
Jika v3 = 3, maka kurangi 2 (go run).
Jika v3 = 4, maka kurangi 2 (go run) dan kurangi 1 (go sleep).
Jika v3 = 1, maka kurangi 4 (eat healthy).
<br><br>
Dengan begitu kita tahu bahwa untuk mencapai 211, maka harus ada 1 kali 2, dan 4 kali 3. Maka dari 7 hari, urutannya bisa menjadi 
<br>
2->3->3->3->3->3->3.
<br>
Dan didapatkan flagnya.

![image](https://user-images.githubusercontent.com/61267430/83205922-fadb1d00-a179-11ea-9448-1b9c8b8104a4.png)

## Flag
tjctf{w3iGht_l055_i5_d1ff1CuLt}