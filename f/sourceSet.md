SourceSet
=========

> Membuat daftar gambar responsif untuk atribut HTML5 `srcset`.

Sintaks
-------

~~~ .xml
sourceSet(sumber, ukuran[, rasio])
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
<img expr:src='data:post.firstImageUrl' expr:srcset='sourceSet(data:post.firstImageUrl, [128, 256, 512])'/>
~~~