# Circles
## Description 
Some typefaces are mysterious, like this one - its origins are an enigma wrapped within a riddle, indeed.
<br>
<a href= https://static.tjctf.org/f5e809c4c49f2c7d607d77c99f07bbd8e9b46dfbe61779201f5b185ed6642de3_Circles.png>Circles.png</a>

## Solution
Pertama-tama, kita dapat berasumsi bahwa flag-nya dapat didapatkan dengan mendekripsikan font-nya, dan dari description challenge, kita bisa mengetahui bahwa flag tersebut dapat menjadi: tjctf{?????f??_f??t}
<br><br>
Kemudian, kita mendapatkan hint sebagai berikut:
<br><br>
To obtain the flag, you should find the font that was used to encode the message in the picture. If you Google the description of the problem, the first website that pops up seems promising. Using a dictionary to guess/bruteforce words without finding the font will not help you. Each circle in the image represents an alphanumeric character that is part of the flag. The brackets and the underscore in the image are NOT part of the font used to encrypt the flag. 
<br><br>
Kemudian kita melakukan pencarian di Google description dari challenge tersebut dan kita bisa menemukan <a href=https://www.fonts.com/font/mans-greback/notera/story>website yang menarik</a>. Kita bisa menggunakan keyword "Circular" untuk mendapatkan font bernama USF Circular Design. Dengan sedikit tenaga kasar, kita bisa mendekripsikan pesannya dan mendapatkan flag-nya


## Flag
tjctf{B3auT1ful_f0Nt}