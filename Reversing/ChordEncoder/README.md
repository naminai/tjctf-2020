# Chord Encoder
## Description 
I tried creating my own <a href=https://static.tjctf.org/67be5bd036a4be8323314d1da6ad2e673963f76634a62ec47d53fb07a04a3722_chords.txt>chords</a>, but my <a href=https://static.tjctf.org/c29857b8d4d1b2dfe502b5053d73844a08358ae681b2af8de6829b765dc2c28e_notes.txt>encoded sheet music</a> is a little hard to read. Please play me my song!

<a href=https://static.tjctf.org/da36df431da358250884ff9765e8c0c5f054b845aff31b85e37229159176bb9f_chord_encoder.py>chord_encoder.py</a>

## Solution
Saya coba lihat isi dari notes.txt namun hanya berupa angka 0, 1, dan 2. Seperti ini:
`1121112111211002112101121121001001210000101221121011200102000110120200101100100111211011001020020010111012011202001011112110121121011211211002112110020200101111210112020010111121010112102001121100211211011020020001010`
<br>
Kemudian, saya coba untuk menilik chords.txt dan di deklarasikan seperti ini:
<br>
- A 0112  <br>
- B 2110  <br>
- C 1012  <br>
- D 020   <br>
- E 0200  <br>
- F 1121  <br>
- G 001   <br>
- a 0122  <br>
- b 2100  <br>
- c 1002  <br>
- d 010   <br>
- e 0100  <br>
- f 1011  <br>
- g 000   <br>

Saya coba konversi notes.txt berdasarkan chords.txt dan menjadi seperti ini: `FFFcFAFGGbGaFAGDGCEfGGfGGFfGDEfCAEfFCFAFcFcEfFAEfFsFEFxFfDDGd`
<br>
Namun, ternyata belum selesai disitu saja. Ketika saya melihat pada chord_encoder.py, ternyata huruf besar kita ubah menjadi angka, sehingga cipher menjadi seperti ini: `666c61677b7a6174735f776f745f315f63616c6c5f615f6d656c6f447d`.

Dan jika di convert ke ascii maka akan mendapatkan flag-nya.
![image](https://user-images.githubusercontent.com/61267430/83220820-3daeec00-a19e-11ea-8228-8cf344bc9539.png) 

## Flag
flag{zats_wot_1_call_a_meloD}