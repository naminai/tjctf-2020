# Gamer W
## Description 
Can you figure out how to <a href=http://gamer_w.tjctf.org/>cheat</a> the system? Grab his hat to prove your victory!

## Solution
Pertama-tama, kita masuk ke dalam game, dan kita mendapatkan hint bahwa kita disuruh meng-install CETUS, sebuah ekstensi browser untuk Mozilla dan Chrome. Dengan CETUS, kita bisa mencari dan memanipulasi value beberapa hal (HP Player, HP Boss, Coins). Kita mengetahui bahwa darah musuh dan darah player dalam bentuk float karena bisa bernilai negatif, maka dari itu kita cari HP Player dan Boss. 

![image](https://user-images.githubusercontent.com/61267430/83215115-5d3f1800-a190-11ea-9c69-6db9b9cfd98e.png)

Kita temukan HP kita, lalu kita bookmark dan kita freeze. Kemudian, kita berhadapan dengan Boss, sehingga kita harus menentukan HP dari Boss tersebut. Masih mudah, disini kita freeze HP Player, sehingga kita tidak terkena damage apapun.
<br><br>
Pada fase 3 Boss Fight, ternyata boss-nya terus beregenarasi lebih cepat dari damage kita. Sehingga, kita harus mencari dan memanipulasi damage milik Player kita.

![image](https://user-images.githubusercontent.com/61267430/83215575-84e2b000-a191-11ea-98b4-dfc332fc3b11.png)
<br>
kita change value-nya ke 300, sehingga damage-nya insta-kill.

![image](https://user-images.githubusercontent.com/61267430/83215683-be1b2000-a191-11ea-8a06-26da4b9d1936.png)
<br>

Kemudian kita dihalangi oleh box pada fase terakhir, sehingga kita tidak bisa bergerak dari spawn. Namun, kita bisa mencari value speed untuk menerobos box tersebut.

![image](https://user-images.githubusercontent.com/61267430/83215962-5addbd80-a192-11ea-91af-7ff30e489e80.png)
<br>
Kita dapatkan speed-nya dan kita ubah ke 100.

![image](https://user-images.githubusercontent.com/61267430/83215998-6e892400-a192-11ea-9a73-8652e6bdaa47.png)
<br>
Kemudian kita keluar dan bunuh boss-nya. Sehingga mendapatkan flag:

![image](https://user-images.githubusercontent.com/61267430/83216053-91b3d380-a192-11ea-9549-a097a25a38aa.png)

## Flag
tjctf{c3tus_del3tus_ur_m3ms__g0ne}