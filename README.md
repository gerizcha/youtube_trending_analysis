[UPDATE]

Have been working on this for 2 weeks, with the highest motivation is learning and investing.
This is also due to my project as a assignment project of bootcamp Data Science and Machine Learning.

The story was:
ABCXYZ company is one of the securities companies in the United States, which is currently focusing on increasing Brand Awareness.
The Marketing Director assigns projects to achieve this goal. One of his tasks is to make the video on the company's official channel penetrate trending on YouTube no later than 3 months from the time the video is uploaded. Therefore, one of the Data Scientists in the company is assigned to do an analysis of what needs to be done to optimize the opportunity for videos on the company's official YouTube channel to become Trending. The results of this analysis will be presented to the Marketing Director and also to the Creative Team for implementation.

***Detail in Bahasa***


# **Latar Belakang:**
> Perusahaan ABCXYZ adalah salah satu perusahaan sekuritas di Amerika Serikat, yang saat ini sedang berfokus pada peningkatan *Brand Awareness*. <br><br>
Direktur Marketing memberikan project kepada divisi-divisi terkait sebagai salah satu strategi untuk mencapai tujuan tersebut. Salah satu tugasnya adalah dengan membuat video dalam official channel perusahaannya menembus trending di YouTube paling lambat 3 bulan dari video diunggah.<br><br>Oleh karena itu, salah satu Data Scientist dalam perusahaan tersebut ditugaskan untuk melakukan analisis mengenai apa-apa saja yang perlu dilakukan untuk mengoptimalkan peluang video di official channel YouTube perusahaan menjadi *trending*. Hasil dari analisis ini akan dipresentasikan kepada Direktur Marketing dan juga kepada Tim Creative untuk diimplementasikan.

## **Pernyataan Masalah**
> 1. Bagaimana gambaran umum mengenai Trending YouTube secara keseluruhan maupun secara periodik?
> 2. Apa saja variabel yang harus diperhatikan untuk mengoptimalkan peluang video muncul di Trending YouTube?
> 3. Apa saja *insights* dan *actionable recommendations* yang didapatkan dari analisis ini?

# **Data**
 > 1. Gambaran data dengan melihat sampel nama kolom dan isi dalam barisnya <br>
 > 2. Ringkasan tipe data dari setiap kolom <br>
 > 3. Data hilang *(missing value)* <br>
 > 4. Statistika deskriptif kolom-kolom numerik<br>
 > 5. Statistika deskriptif kolom-kolom non-numerik
 
 ## **Pembersihan dan Manipulasi Data**
> 1. Menghapus data duplikat <br>
> 2. Mengidentifikasi dan menghapus kolom-kolom yang tidak perlu dianalisis <br>
> 3. Mengidentifikasi dan mengubah tipe data sesuai relevansinya <br>
> 4. Menindaklanjuti data hilang/missing value <br>
> 5. Mengidentifikasi dan menindaklanjuti anomali

# **Analisis Data**
> 1. `Analisis Umum` : pemaparan jumlah video yang muncul di trending dalam skala bulanan dan juga Statistika Deskriptif secara umum. <br>
> 2. `Analisis Konten` : analisis video berdasarkan kategori, termasuk mengenai judul dan penggunaan tagar (*hashtag*) yang dikaitkan dengan jumlah video dan views yang terkait dengan setiap kategori. <br>
> 3. `Analisis Reaksi` : mengenai jumlah komentar, like, dan dislike pada video yang juga dikaitkan dengan jumlah views.
> 4. `Analisis Waktu Unggah` : mengenai waktu pengunggahan video dan dikaitkan dengan jumlah video maupun jumlah views.

## **Uji Korelasi**
>1. Melakukan uji normalitas <br>
>2. Melakukan uji korelasi yang tepat digunakan berdasarkan hasil uji normalitas <br>

# **Jawaban Pernyataan Masalah**

## **1. Bagaimana gambaran umum mengenai Trending YouTube secara keseluruhan maupun secara periodik?** 
- Secara keseluruhan, video yang paling banyak muncul di Trending YouTube adalah kategori Entertainment. <br>
- Jika dilihat dalam skala bulanan, jumlah video yang muncul di Trending YouTube variatif. Ini mengindikasikan bahwa tidak ada minimum atau maksimum jumlah video yang bisa muncul di Trending YouTube.<br>
- Dari jumlah views, justru kategori Music adalah kategori yang mendominasi dari keseluruhan video.<br>
- Jumlah views semua video dari waktu ke waktu selalu meningkat. Terutama di bulan Mei 2018 dan Juni 2018, angka total views signifikan meningkat dari bulan-bulan sebelumnya.<br>
- Selaras dengan jumlah views, ternyata kategori Music memiliki jumlah likes dan jumlah comments yang paling tinggi juga. Menariknya, ternyata kategori Music pun adalah kategori yang jumlah dislikes-nya paling tinggi. Ini mengindikasikan bahwa semakin banyak jumlah views, berpotensi semakin tinggi pula reaction dari pada pengguna YouTube dengan comments, likes, maupun dislikes.<br>
- Mayoritas video memiliki kurang lebih 681 ribu penayangan dalam rentang 241 ribu sampai 1,82 juta total views.<br>
- Mayoritas video memiliki kurang lebih 18 ribu likes dalam rentang 5 ribu sampai 55 ribu likes.<br>
- Mayoritas video memiliki kurang lebih 630 likes dalam rentang 202 sampai 1936 dislikes.<br>
- Mayoritas video memiliki 1855 komentar dalam rentang 613 sampai 5752 komentar.<br>
- Secara proporsi, hampir semua video yang muncul di Trending YouTube (98%-99%) mengaktifkan kolom komentar dan mengaktifkan Like & Dislikes.<br>
- Berdasarkan panjang karakter dalam judul, mayoritas video memiliki judul dengan jumlah 46 karakter dalam rentang 34-61 karakter.<br>
- Hanya ada sebagian kecil video (6%) dengan judul video menggunakan huruf kapital semua. Mayoritas video memiliki judul dengan campuran kapital dan non-kapital.<br>
- Mayoritas video menggunakan kurang lebih 18 hashtags dalam rentang 9 sampai 28 hashtags.<br>
- Berdasarkan hari, video paling banyak diunggah di hari Jumat. Berdasarkan jam, video paling banyak diunggah di jam 4 sore.<br>
- Mayoritas video muncul di Trending YouTube kurang lebih 5 hari dalam rentang 3 sampai 9 hari sejak video diunggah. <br>

## **2. Apa saja variabel yang harus diperhatikan untuk mengoptimalkan peluang video muncul di Trending YouTube?**
> **`- Views`** <br>
> **`- Likes`**<br>
> **`- Dislikes`** `(dengan catatan)`<br>
> **`- Comment Count`**

`Views` dapat disimpulkan menjadi variabel yang paling penting di antara variabel lainnya karena memutar video adalah langkah pertama yang harus pengguna YouTube lakukan sebelum memberikan *reaction* terhadap video. Dengan pembuktian bahwa `views, jumlah komentar, jumlah likes dan dislikes` berkorelasi sangat kuat antara satu sama lain, hal ini menunjukkan bahwa meningkatnya satu variabel berpotensi meningkatkan variabel lainnya.<br><br>Ada catatan penting bahwa variabel `dislikes` berkorelasi kuat pula dengan variabel lainnya tetapi variabel ini bukanlah variabel yang "baik" pada suatu video, sehingga meningkatkan `dislikes` untuk meningkatkan `views, likes, dan jumlah komentar` bukanlah hal yang tepat untuk dilakukan.<br>

`Jumlah karakter pada judul, dan jumlah hashtags` tidak berkorelasi dengan variabel apapun, tetapi bisa dikaitkan dengan pusat data yaitu **IQR dan median** yang dapat merepresentasikan variabel-variabel tersebut. 

## **3. Apa saja *insights* dan *actionable recommendations* yang didapatkan dari analisis ini?**
> - Buatlah konten dengan jangkauan `segmentasi yang luas` sehingga meningkatkan potensi video tersebut ditonton oleh banyak pengguna. <br>
Semakin banyak video diputar *(views)*, semakin tinggi pula potensi untuk banyaknya likes dan komentar. Banyaknya *reaction* seperti likes dan komentar itu kembali lagi meningkatkan potensi video diputar kembali maupun menjangkau pengguna YouTube lainnya sehingga views pun akan semakin meningkat.<br>
> - Buatlah target segmentasi luas yang menjangkau `beberapa rentang usia`, misalnya usia remaja sampai usia tua. Jika video relevan dengan berbagai rentang usia, potensi jumlah pengguna YouTube yang akan menonton pun semakin meningkat.<br>
> - Konten harus berhasil menstimulasi pengguna untuk `menulis di kolom komentar`, misalnya dengan kuis, menanyakan opini/preferensi, meminta pengguna untuk menceritakan kisahnya dalam investasi, atau lainnya.<br>
> - Selalu balas komentar dalam video, karena selain meningkatkan `jumlah komentar`, minimal pengguna YouTube yang menulis komentar tersebut akan kembali ke video untuk melihat balasan yang berpotensi untuk memutar kembali video. Dengan semakin banyaknya komentar, akan semakin besar juga potensi peningkatan `jumlah views`. <br>
> - Mengingat dua kategori utama yaitu `Entertainment` dan `Music` yang secara signifikan mendominasi baik secara jumlah video maupun jumlah views, buatlah bumbu-bumbu hiburan dalam konten dan pemutaran musik sebagai *backsound*.
> - Menonaktifkan kolom komentar dan button *like* & *dislike* tidak disarankan, mengingat `total views, jumlah likes, dan jumlah komentar` saling mempengaruhi secara kuat antara satu sama lain.<br> 
> - Variabel `dislikes` berkorelasi kuat pula dengan variabel lainnya tetapi variabel ini bukanlah variabel yang "baik" pada suatu video, sehingga meningkatkan `dislikes` untuk meningkatkan `views, likes, dan jumlah komentar` bukanlah hal yang tepat untuk dilakukan. <br>
> - `Jumlah karakter` tidak berkorelasi dengan apapun, tetapi jika melihat pusat data, mayoritas video memiliki judul dengan kurang lebih `46 karakter` dalam rentang `34 sampai 61 karakter`. Judul sebaiknya tidak terlalu panjang sehingga judul dapat terlihat semua.
> - Penggunaan huruf semua kapital maupun nonkapital pada judul dibebaskan, disesuaikan saja dengan kontennya. Buatlah *copy writing* pada judul yang menarik bagi pengguna YouTube agar tertarik untuk mengklik dan memutar video tersebut sehingga menghasilkan `views`.<br>
> - Penggunaan hashtags dan `jumlah hashtags` tidak berkorelasi dengan variabel apapun. Mayoritas video memiliki `18 hashtags` dalam rentang `9 sampai 28 hashtags`. Buatlah  hashtag-hashtag yang relevan dengan video, karena ketika pengguna mengetik *keyword* dan menganggap video relevan dengan apa yang ia cari, ini akan mendorong *reaction* positif dari pengguna YouTube seperti Likes dan Komentar, yang akan kembali *looping* menghasilkan `jumlah views` yang lebih banyak.
> - Untuk `hari dan jam pengunggahan video`, referensi bisa mengacu pada modus. Video paling banyak diunggah di `hari Jumat`. Untuk jam, video paling banyak diunggah di `jam 4 sore`. Selaras dengan pola berdasarkan jumlah video maupun jumlah views, yang paling tinggi adalah hari Jumat. Mengingat secara umum, mayoritas orang memiliki banyak waktu luang di akhir pekan (Sabtu dan Minggu) karena hari libur. Cara ini dapat mengoptimalkan video menghasilkan banyak views dalam waktu yang relatif singkat sehingga meningkatkan peluang muncul di Trending YouTube. <br>
> - Semakin lama rentang waktu dari video diunggah belum tentu masih menghasilkan `views, likes, dan komentar` yang lebih banyak pula. Oleh karena itu, kejar views maupun *reaction* positif pada video secepat mungkin. Data membuktikan bahwa mayoritas video muncul di Trending kurang lebih `5 hari` setelah video diunggah, di `antara 3 sampai 9 hari`. Secara keseluruhan, video-video muncul di Trending YouTube dengan rentang 0 sampai 30 hari sejak video diunggah, sehingga butuh perhatian khusus pada 30 hari pertama, terutama di 9 hari pertama, untuk menghasilkan views, likes, dan komentar.<br>
> - Pernyataan resmi dari pihak Google mengenai pertimbangan-pertimbangan bagaimana video bisa muncul di Trending YouTube ada di tautan ini *https://support.google.com/youtube/answer/7239739?hl=en* untuk menjadi tambahan referensi untuk membuat konten.

-------------
This analysis will provide you many references of codes/syntaxes, the systematic and coherent explanation, and insights also actionable recommendations.
The dataset was very old though, but you can cherry picking based on your needs.
I HOPE IT WOULD HELP!
-------------

-------------
I am using lottts of libraries here, but guess what? 
I only installed and imported ONE LIBRARY --- pyforest ---
You can thank me later B-)
-------------

-------------
WARNING!<br>
For better experience, you better download this (.ipynb) and run on your own. Have tried many times uploading but my visualizations which using Plotly Express are not displayed. 
-------------


Also I have the tableau story (in English), you guys can check here<br>
https://public.tableau.com/app/profile/gerizcha.aprilia.pardede/viz/CP2_Gerizcha_YouTubeTrendingAnalysis/Story1 <br>
<br>
Explanation video (in Bahasa) : https://youtu.be/5AW1cok8t1U
<br>
Link dataset : https://drive.google.com/drive/folders/1JFhDSfs4vzWuCdsBFObEp5sVLQMo-dR1

