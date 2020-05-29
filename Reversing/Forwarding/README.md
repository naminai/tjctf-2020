# Forwarding
## Description 
It can't be that hard... right?

<a href=https://static.tjctf.org/d9c4527bc1d5c58c1192f00f2e2ff68f84c345fd2522aeee63a0916897197a7a_forwarding>forwarding</a>

## Solution
Pertama saya coba jalankan filenya, namun tidak berbentuk apa-apa. Kemudian saya coba menggunakan command `strings forwarding | grep tjctf` untuk mendapatkan semua printable character dalam program dan kita pipe dengan grep flag format yaitu tjctf dan kemudian didapatkan flag-nya.
<br>
![image](https://user-images.githubusercontent.com/61267430/83203930-bef18900-a174-11ea-9f24-daf69b4fbf5b.png)

## Flag
tjctf{just_g3tt1n9_st4rt3d}