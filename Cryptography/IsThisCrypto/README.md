# Is This Crypto?
## Description 
<a href=https://static.tjctf.org/e141851decd4f7afab034c7055db229bd54011d2860ebd622302088fd4e062ae_file.txt>Is this crypto?</a>

## Solution
Sekilas, nampak seperti random gibberish. Kita melihat hint, namun hint-nya pun tidak terlalu berguna. Kemudian kita gunakan command `file`, dan kita mendapatkan hasil seperti berikut:
<br>
file.txt: Non-ISO extended-ASCII text, with very long lines, with no line terminators
<br>
Non-ISO extended-ASCII text, kemudian saya mencoba mencari tabel extended ASCII. Setelah dilihat-lihat, ternyata yang dimaksud adalah second Unicode block pada Unicode standard atau nama lainnya yaitu Latin 1 Supplement. Kita coba cari font-nya pada <a href=https://jrgraphix.net/r/Unicode/00A0-00FF>website ini</a>
<br><br>
Kita coba translasikan dengan menggunakan tabel berikut, namun masih menjadi gibberish. Setelah lama buntu, akhirnya kita mengetahui bahwa setiap kolom dan baris telah ditukar secara ganjil genap (kolom 1 ke 2 dan 2 ke 1) pada tabel tersebut. Maka kita coba ganti dengan menggunakan website <a href=https://cryptii.com/pipes/alphabetical-substitution>Cryptii</a>. Kemudian kita mendapatkan hasil seperti berikut:
<br><br>
Cryptography is a discipline that has been around for quite a long time, but in recent times it has seen an explosion of research and implementation. This discipline seeks to provide secure communication and shared data storage using public key cryptography, which essentially reduces the damage that can be done through encryption.
<br><br>
tjctf{n0_th5_is_kyl3}
<br><br>
The Data Centre Standard for Confidentiality and Integrity states that a computer system must not contain any information that cannot be provided at the time of requesting it. The purpose of this standard is to ensure that no data from a connected computer system can be accessed by an unauthorised party. This would allow users to protect their data and make their personal information secure, which is more important than ever 

## Flag
tjctf{n0_th5_is_kyl3}