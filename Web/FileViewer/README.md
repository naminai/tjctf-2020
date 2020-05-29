# File Viewer
## Description 
So I've been developing this really cool <a href=http://file_viewer.tjctf.org/>site</a> where you can read text files! It's still in beta mode, though, so there's only six files you can read.

## Solution
Pertama kita kunjungi situs-nya dan kita lihat.
![image](https://user-images.githubusercontent.com/61267430/83211116-7cd14300-a186-11ea-8d50-9ec34e44ddf3.png)
<br>
Kita coba input apple.txt ke pencarian dan kita bisa melihat bahwa terdapat kelemahan, terutama di Remote File Inclusion.
<br>
![image](https://user-images.githubusercontent.com/61267430/83211196-b144ff00-a186-11ea-8755-50bff6a9c13e.png) 
<br>
Kita bisa lihat di URL, bahwa file menunjuk pada `location_link_nama_file.txt`. Kita coba dengan google.com
<br>
![image](https://user-images.githubusercontent.com/61267430/83211296-f10be680-a186-11ea-869e-62c06aad4b80.png)
<br>
Saya berpikir untuk menggunakan pastebin untuk menjalankan remote shell untuk menemukan lokasi file. Berikut programnya:
![image](https://user-images.githubusercontent.com/61267430/83211769-29f88b00-a188-11ea-862b-5454bc1e2fbc.png)
<br>
Saya copy link raw paste-nya, dan didapatkan direktori-nya seperti ini:
![image](https://user-images.githubusercontent.com/61267430/83211848-53b1b200-a188-11ea-97fe-06e420a0f9dd.png)
<br>
Kita bisa melihat terdapat direktori i_wonder_whats_in_here. Kita bisa melihat lebih lanjut dengan mengubah bagian dari program kita:
<br>
![image](https://user-images.githubusercontent.com/61267430/83211944-8bb8f500-a188-11ea-95b8-dc452f77b76f.png)
<br>
Dan kita dapatkan isi dari direktori i_wonder_whats_in_here:
![image](https://user-images.githubusercontent.com/61267430/83212018-b73bdf80-a188-11ea-81bc-2cfc73f7d16f.png)
<br>
Setelah itu, kita buka dengan `cat` flag.php.
<br>
![image](https://user-images.githubusercontent.com/61267430/83212099-e81c1480-a188-11ea-9d54-1575ff6b61de.png)
<br>
Dan kita dapatkan flag-nya.
<br>
![image](https://user-images.githubusercontent.com/61267430/83212292-6d9fc480-a189-11ea-925f-90ddb91cfaf9.png)

## Flag
tjctf{n1c3_j0b_with_lf1_2_rc3