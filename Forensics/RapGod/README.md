# Rap God
## Description 
My rapper friend Big Y sent me his <a href=https://static.tjctf.org/302ed01b56ae5988e8b8ad8d9bba402a2934c71508593f5dc9e95aed913d20cf_BigYAudio.mp3>latest track</a> but something sounded a little off about it. Help me find out if he was trying to tell me something with it. Submit your answer as tjctf{message}

## Solution
Pertama-tama saya mencoba mendengarkan audio dari file tersebut, namun tidak terdengar adanya apapun. Kemudian, saya mencoba untuk menggunakan Audicity untuk mendapatkan spektogram dari file audio tersebut. Dengan mengubah view-nya kita dapat melihat sesuatu yang menarik.
<br>
![Flag](flag.jpg)
<br>
Dari gambar diatas, ternyata ada beberapa gambar yang menarik. Mengingat penyelenggara TJCTF adalah orang Amerika, saya teringat tentang meme 9-11 Conspiracy dan teringat tentang font Wingdings. Kita coba cocokkan dengan font Wingdings yang terbaru dan kita dapatkan kata QUICKSONIC. Kita dapatkan flag-nya. 

## Flag
tjctf{QUICKSONIC}