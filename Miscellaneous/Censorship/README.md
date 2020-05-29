# Censorship
## Description 
My friend has some top-secret government intel. He left a message, but the government censored him! They didn't want the information to be leaked, but can you find out what he was trying to say?

`nc p1.tjctf.org 8003`

## Solution
Pertama-tama, saya mencoba menginput jawaban yang benar, namun hanya terdapat flag yang sudah disensor. 
![image](https://user-images.githubusercontent.com/61267430/83106039-f82ee800-a0e5-11ea-9f40-46b8c141be5e.png)

Sepertinya masalahnya bukan reversing program, karena tidak disediakan source code program. Maka dapat disimpulkan bahwa problem ada di server side. Sehingga, kemungkinannya adalah kita harus meng-input sedemikian cepat sehingga kita bisa mendapatkan flag-nya. Dengan menggunakan `censorship.py`, kita dapatkan flag-nya.
![image](https://user-images.githubusercontent.com/61267430/83106090-0f6dd580-a0e6-11ea-96bb-4029ea85e1cb.png)

## Flag
tjctf{TH3_1llum1n4ti_I5_R3aL}