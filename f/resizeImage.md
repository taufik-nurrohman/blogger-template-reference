resizeImage
===========

> Mengubah ukuran gambar.

Sintaks
-------

~~~ .xml
resizeImage(sumber, ukuran[, rasio])
~~~

Parameter
---------

Parameter | Deskripsi                       | Contoh
--------- | ------------------------------- | -------------------------
`sumber`  | URL gambar.                     | `data:post.firstImageUrl`
`ukuran`  | Lebar gambar yang dikehendaki.  | `200`
`rasio`   | Rasio potongan gambar.          | `"1:1"`, `"4:3"`

### Catatan

 - Jika nilai parameter `sumber` tidak dapat diubah ukurannya (misalnya, gambar bukan berasal dari **Picasa** atau **Google Photos**), maka fungsi ini akan mengembalikan ke nilai asli dari `sumber` tanpa adanya modifikasi
 - Nilai parameter `rasio` harus berupa integer
 - Jika parameter `rasio` ditentukan, gambar akan dipotong sesuai dengan perbandingan dimensi yang ditentukan.

Penggunaan
----------

~~~ .xml
<img expr:src='resizeImage(data:post.firstImageUrl, 200, &quot;1:1&quot;)'/>
~~~

~~~ .xml
<b:with var='image' value='resizeImage(data:post.firstImageUrl, 200, &quot;1:1&quot;)'>
  <p><strong>URL Gambar:</strong> <data:image/></p>
</b:with>
~~~