---
title: 
layout: post
author:
categories: [Math]
excerpt: "Artikel ini akan membahas perbedaan antara subset/himpunan (⊆) dan element of/anggota dari (∈) beserta contoh-contohnya"
description: "Artikel ini akan membahas perbedaan antara subset/himpunan (⊆) dan element of/anggota dari (∈) beserta contoh-contohnya"
---

# Perbedaan ∈ dan ⊆
Artikel ini saya tulis berawal dari kebingungan yang saya rasakan dalam simbol matematika pada materi himpunan yaitu disini perbedaan antara ∈ vs ⊆ sampai-sampai saya salah menjawab soal saat di perkkuliahan karena sulit membedakan antara ∈ dan ⊆. Agar saya tidak lupa, saya membuat artikel ini untuk arsipan :).

Sebelum saya menulis artikel ini, saya membaca terlebih dahulu materi tersebut dalam sebuah slide yang sangat bagus yang dibuat oleh web.stanford.edu, kamu bisa cek [Disini](https://web.stanford.edu/class/cs103/resources/Guide%20to%20Elements%20and%20Subsets.pdf), materi disana sangat bagus dan membuat saya sekarang dapat membedakan antara ∈ dan ⊆ dan menulis artikel ini.

Beberapa istilah :
* `set` adalah himpunan.
* `subset` adalah himpunan bagian, himpunan yang seluruh anggota berada di himpunan lain.
* `Empty Set` adalah set/himpunan yang tidak memiliki element

Oke kita mulai, pertama kita perlu ketahui kedua simbol tersebut(∈ dan ⊆) merepresentasikan keterhubungan. Kalau masi bingung, kita bisa mulai dari arti dari masing-masing simbol tersebut.

### Element-of / ∈
Apa arti ∈ ?
∈ adalah simbol yang bermakna "element-of" atau dalam bahasa indonesianya adalah "anggota dari", ini dipakai untuk menyatakan bahwa suatu object merupakan anggota dari sebuah set/himpunan.

__Contoh__: Apakah pernyataan ini benar? `a ∈ {a, b}`.
Pernyataan tersebut benar, karena jika kita melihat kesana, terdapat `a` (disebelah kiri) di dalam himpunan `{a, b}` (disebelah kanan), yang mengindikasikan bahwa `a` termasuk merupakan anggota dari himpunan `{a, b}`.
Sebaliknya jika element nya tidak ada di dalam seperti `c ∉ {a, b}`, karena element `c` sendiri tidak terdapat di dalam himpunan, mengindikasi bahwa ia bukan merupakan anggota dari himpunan tersebut.

__intinya yang perlu diingat adalah__, pada `x ∈ S` yang dimana `x` adalah harus berupa object merupakan anggota-dari himpunan `S`, jadi `S` disini harus berupa set/himpunan.
Kalau kita bicara object, kita bisa bayangkan itu adalah sesuatu seperti suatu elemen, yang sudah solid, terbungkus, dsb. Object bisa saja berupa suatu elemen, set, gambar, dsb. Intinya adalah apakah object tersebut berada di dalam set disebelah kanan ataupun tidak untuk mengindikasikan "anggota-dari" (`∈`). 

Sebagai contoh jika object berupa set, apakah object set tersebut `{a,b}` berada didalam set disebelah kanan `{a, {a,b}}`?, jawabannya iya, seperti `{a,b}` ∈ {a, `{a,b}`}.

Simpel bukan? Sekarang kita akan melajutkan untuk simbol `⊆`.

### Subset-of /  ⊆
simbol `⊆` disebut "subset-of" atau "himpunan bagian dari", menyatakan hubungan antara dua set/himpunan. Ingat ya..Antara-dua-himpunan.

__intinya adalah__, contoh pada `S ⊆ T` yang bermakna dimana setiap object/element yang terdapat di dalam set/himpunan `S` berada di dalam set/himpunan `T`.

__Contoh__: {`e`, `f`} ⊆ {a, b, c, d, `e`, `f`}, pernyataan ini benar karena memang didalam himpunan di sebelah kiri yaitu `e dan f` terdapat didalam himpunan disebelah kanan yaitu {a, b, c, d, `e, f`}.

Jika tidak terdapat maka kita dapat menggunakan simbol &nsub;.

Sekarang, gimana jika pernyataan `b ⊆ {a, b, c}`?, apakah pernyataan tersebut benar?. Jawabannya tidak, karena jelas bahwa bahwa disebelah kiri haruslah berupa himpunan (ciri-ciri himpunan didalamnya ada isinya dan isinya tersebut ada gak di himpunan sebelah kanan), sedangkan contoh diatas `b` merupakan element yang dimana isinya tidak dapat didefinisikan jadi pernyataan tersebut tidak benar. yang benar adalah `b` merupakan anggota-dari `{a, b, c}` yang bisa dibuat dengan `b ∈ {a, b, c}`.

#### Advanced
Sekarang semoga kita sudah tahu nih perbedaan yang mendasar dari kedua simbol tersebut, mari masuk ke mode lebih dalam lagi.

Bagaimana jika terdapat sebuah set `{1, {1, 2}, 3}`, set ini didalamnya terdapat 3 object/element yaitu `1`, `{1, 2}` dan `3`. Dapat dilihat disini, object kedua berupa sebuah set, jadi ini bermakna set didalam set bukan?.

Berikut pernyataan yang benar terkait set `{1, {1, 2}, 3}` diatas.
* `1 `&#8712;` { 1, {1, 2}, 4 }` -> element `1` merupakan anggota dari set. 
* `{1} `&#8713;` { 1, {1, 2}, 4 }` -> tidak terdapat element `{1}` di dalam set sebelah kanan, harap diperhatikan element/object `{1}` tidak sama dengan `1`. 
* `{1} `&sub;` { 1, {1, 2}, 4 }` -> isi himpunan `{1}` yaitu `1` terdapat di dalam set sebelah kanan {`1`, {1,2}, 4}. 
* `1 `&nsub;` {1, {1, 2}, 4}` -> karena `1` bukan merupakan set karena isinya tidak terdefisini, jika isinya tidak bisa dilihat bagaimana kita bisa katakan bahwa isinya terdapat didalam set {1, {1, 2}, 4}.
* `{1, 2} `&#8712;` { 1, {1, 2}, 4 }` -> element `{1, 2}` merupakan anggota dari set.
* `{1, 2} `&nsub;` { 1, {1, 2}, 4 }` -> isi dari `{1, 2}` yaitu 1 & 2 tidak terdapat keduanya didalam set sebelah kanan. hanya `1` saja yang terdapat dan `2` tidak, karena fokus kita himpunan terluarnya, set/himpunan dalam set/himpunan yaitu `{1,2}` disebelah kanan tidak termasuk.
* `2 `&#8713;` { 1, {1, 2}, 4 }` -> fokus himpunan terluar, `2` tidak terdapat didalam set sebelah kanan, himpunan didalam himpunan yaitu `{1, 2}` tidak dihitung.

### Empty Set Ø
__Tambahan__,
The Empty Set adalah set/himpunan yang tidak memiliki element, dapat dibuat berupa `Ø` atau `{}`.

karena ia adalah himpunan kosong maka beberapa pernyataan berikut benar:
* `x `&#8713;` Ø` -> karena element `x` pasti tidak ada di dalam set Ø, karena set Ø memang tidak ada isinya.
* `Ø `&sub;` S` -> himpunan kosong adalah subset dari himpunan apapun S. ini adalah vacuous truth. Ibaratnya gini, himpunan kosong {} tidak memiliki isi/isinya kosong, kosong terdapat/tidak di dalam set `S` tidak berpengaruh terhadap `S` itu sendiri. 

__Contoh__ pernyataan yang benar : 
* `Ø `&#8713;` { 1, {2, 3}, 4 }` -> jelas Ø bukan merupakan anggota dari set kanan. anggota set kanan hanya `1`, `{2,3}`, dan `4`.
* `Ø `&sub;` { 1, {2, 3}, 4 }` -> karena himpunan kosong subset dari setiap set.
