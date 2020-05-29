# Zipped Up
## Description 
My friend changed the password of his Minecraft account that I was using so that I would stop being so addicted. Now he wants me to work for the password and sent me this <a href=https://static.tjctf.org/663d7cda5bde67bd38a8de1f07fb9fab9dd8dd0b75607bb459c899acb0ace980_0.zip>zip file</a>. I tried unzipping the folder, but it just led to another zipped file. Can you find me the password so I can play Minecraft again?

## Solution
Pertama-tama kita download zip file-nya. Namun, sama seperti description problem, kita sadar bahwa Zip File ini tampak seperti Russian Doll. Dibuka satu layer masih ada layer lagi di bawahnya. Sehingga, kita bisa menggunakan sesuatu untuk mempermudah proses unzipping ini. Kita juga harus memikirkan tentang bagaimana hal-nya dengan file seperti `1.tar.bz` yang memiliki 2 proses unzipping. Maka dari itu, kita menggunakan 7z untuk unzipping, karena sangat versatile sehingga mencakup banyak extension file. 
<br>
Kita menggunakan script ini:
<br><br>
`for i in {0..1001}; do find -iname $i.* -exec 7z e -aos -bso0 {} ;; find -iname $i.* -exec 7z e -aos -bso0 {} ;; find -iname $i.* -exec 7z e -aos -bso0 {} ;; done`
<br><br>
Kemudian kita gunakan command `cat *.txt | grep tjctf` untuk mendapatkan flag-nya.
<br>
![image](https://user-images.githubusercontent.com/61267430/83114358-1222f780-a0f3-11ea-8ad4-ced617bd6c46.png)

## Flag
tjctf{p3sky_z1p_f1L35}