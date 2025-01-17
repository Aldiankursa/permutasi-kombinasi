# permutasi-kombinasi
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Permutasi Dan Kombinasi 1 TRPL A</title>
    <style>
        /* CSS */
        * {
            margin: 0;
            padding: 0;
            scroll-behavior: smooth;
        }

        body {
            font-family: tahoma;
            margin: 0;
            padding: 0;
        }

        header {
            background: #f5f5f5;
            padding: 10px 20px;
        }

        .top-bar {
            display: flex;
            justify-content: space-between;
            font-size: 14px;
            border-bottom: 1px solid #ddd;
        }

        .logo-section {
            text-align: center;
            padding: 10px 0;
        }

        .logo-section img {
            height: 50px;
            margin: 0 10px;
        }

        nav {
            position: sticky;
        }

        .active {
            background-color: #04aa64;
        }

        nav.main-menu {
            position: sticky;
            top: 0; /* Agar navbar tetap berada di bagian atas saat digulir */
            z-index: 1000; /* Agar navbar berada di atas konten lain */
            background-color: #333; /* Warna latar belakang navbar */
        }


        .main-menu ul {
            list-style: none;
            display: flex;
            justify-content: center;
            background: #333;
            margin: 0;
            padding: 0;
        }

        .main-menu ul li {
            margin: 0;
        }

        .main-menu ul li a {
            text-decoration: none;
            color: #fff;
            padding: 15px 20px;
            display: block;
        }

        .main-menu ul li a:hover {
            background: #555;
        }

        .banner {
            position: relative;
        }

        .banner h1 {
            position: absolute;
            top: 40%;
            left: 50%;
            transform: translate(-50%, -50%);
            color: white;
            padding: 10px 20px;
            text-align: center;
            font-size:5rem;
            text-shadow: 4px 4px 4px black;
            z-index: 10; /* Prioritas di atas gambar */
        }

        .judul-profil, .judul-permutasi {
            margin-top: 60px;
            text-align: center;
            font-size: 2rem;
            color: black;
        }

        .jdl-video, .jdl-kalkulator {
            color: black;
        }

        .profile {
            display: flex;
            justify-content: center; 
            align-items: flex-start; /* Memastikan semua item sejajar di bagian atas */
            gap: 100px; /* Jarak antar item */
            margin-top: 20px;
        }

        .profile-item {
            text-align: center;
            width: 200px; /* Pastikan semua item memiliki lebar yang sama */
        }

        .profile-item img {
            display: block; /* Menghilangkan jarak bawaan dari gambar */
            width: 100%; /* Ukuran gambar proporsional dengan container */
            height: auto; /* Memastikan gambar tetap proporsional */
            border-radius: 10px; /* Membuat gambar bulat */
            box-shadow: 4px 4px 4px grey; /* Menambahkan efek bayangan */
        }

        .profile-item span {
            display: block;
            margin-top: 10px;
            font-weight: bold;
            font-size: 1rem;
            line-height: 1.5; /* Menambahkan spasi antar teks untuk estetika */
        }

        .pengertian-permutasi {
            margin-left: 20px;
        }

        .cnth-pb {
            margin-left: 40px;
        }

        .cnth-ptb {
            margin-left: 40px;
            margin-right: 570px;
        }

        .des1-permutasi {
            margin-left: 20px;
            margin-right: 600px;
            text-align: justify;
        }

        .rp {
            margin-left:40px;
            border: 2px solid black;
            margin-right: 850px;
            padding: 20px;
            text-align: center;
        }

        .jjp {
            margin-left: 40px;
        }

        .cnth-puyb, .cnth-pduys, .cnth-psiklis {
            margin-left: 40px;
            margin-right: 570px;
        }

        .rume {
            margin-left:40px;
        }

        .pengulangan-diperbolehkan, .pengulangan-tidak-dibolehkan {
            margin-left: 60px;
        }

        .pbr {
            margin-left: 40px;
        }

        .img1 {
            float: right;
            margin-left: 30px;
            box-shadow: 2px 2px 2px 2px black;
        }

        .kmbnsi {
            margin-top: 100px;
        }

        .judul-kombinasi {
            text-align: center;
            font-size: 2rem;
            color: black;
        }

        .pengertian-kombinasi {
            margin-left: 20px;
        }

        .des1-kombinasi {
            margin-left: 20px;
            margin-right: 600px;
            text-align: justify;
        }

        .cnth-ktb {
            margin-left: 40px;
        }

        .img2 {
            float: left;
            margin-left: 35px;
            box-shadow: 2px 2px 2px 2px black;    
        }

        .img4 {
            float: left;
            margin-left: 35px;
            box-shadow: 2px 2px 2px 2px black;
        }

        .cnth-kb {
            margin-left: 40px;
            margin-right: 570px;
        }

        .img3 {
            float: left;
            margin-left: 35px;
            box-shadow: 2px 2px 2px 2px black;
        }

        .img5 {
            float: left;
            margin-left: 35px;
            box-shadow: 2px 2px 2px 2px black;
        }

        .vp {
            margin-top: 100px;
            text-align: center;
        }

        .vpr {
            margin-top: 20px;
            display: flex;
            gap: 0.5rem;
            justify-content: center;
            margin-left: 20px;
            margin-right: 20px;
        }

        iframe {
            border-radius: 20px;
        }

        .cal1 h1 {
            margin-top: 100px;
            text-align: center;
        }

        .cal1 h2 {
            margin-top: 30px;
            text-align: center;
        }

        .container {
            max-width: 1000px;
            margin: 0 auto;
            padding: 20px;
            background-color: #f9f9f9;
            border-radius: 10px;
            box-shadow: 2px 2px 2px grey;
        }

        h1 {
            font-size: 2rem;
            margin-bottom: 20px;
            color: #333;
        }

        h2 {
            font-size: 1.5rem;
            margin-bottom: 20px;
            color: #555;
        }

        .input-group {
            margin-bottom: 20px;
            text-align: left;
        }

        .input-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: bold;
            color: #333;
        }

        .input-group input {
            width: 100%;
            padding: 10px;
            font-size: 1rem;
            border: 2px solid #ddd;
            border-radius: 5px;
            box-sizing: border-box;
        }

        .input-group input:focus {
            border-color: #04aa64;
            outline: none;
        }

        .input-group div {
            display: flex;
            gap: 10px;
            justify-content: center;
            align-items: center;
        }

        .input-group input[type="radio"] {
            width: auto;
        }

        .button {
            background-color: #04aa64;
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            font-size: 1.2rem;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }

        .button:hover {
            background-color: #037b4b;
        }

        .result {
            margin-top: 20px;
            font-size: 1.2rem;
            font-weight: bold;
            color: #333;
        }

        .quiz {
            margin-top: 100px;
            text-align: center;
            margin-bottom: 20px;
        }

        .kahoot {
            display: flex;
            justify-content: center;
        }
</style>

    </style>
</head>
<body>
    <header>
        <div class="logo-section">
            <img src="W.png" alt="Politeknik Manufaktur Negeri Bangka Belitung">
            <img src="f.jpg" alt="matematika"> 
        </div>
    </header>

    <!-- Navigation Menu -->
    <nav class="main-menu">
        <ul>
            <li><a href="#home">BERANDA</a></li>
            <li><a href="#profil">PROFIL</a></li>
            <li><a href="#permutasi">PERMUTASI</a></li>
            <li><a href="#kombinasi">KOMBINASI</a></li> 
            <li><a href="#video">VIDEO</a></li> 
            <li><a href="#kalkulator">KALKULATOR</a></li>
            <li><a href="#quiz">QUIZ</a></li>
        </ul>
    </nav>

    <!-- Banner -->
     <section id="home">
    <main>
        <div class="banner">
            <img src="gkb.jpg" width="100%"">
            <h1 class="judul">PERMUTASI <br>DAN <br>KOMBINASI</h1>
        </div>
    </main>
    </section>

    <section class="prfl" id="profil">
        <h2 class="judul-profil">PROFIL</h2>
        <div class="profile">
            <div class="profile-item">
        <img src="ALDIAN.jpeg" width="200" style="border-radius: 100px; box-shadow: 4px 4px 4px grey;">
        <span class="aldian">ALDIAN KURNIAWAN SAPUTRA <br>
            <p>Kelas : 1 TRPL A <br>
            NPM : 1062404</p>
        </span>
        </div>
        <div class="profile-item">
        <img src="HIKMAL.jpeg" class="gmbr-hikmal" width="200" style="border-radius: 100px; box-shadow: 4px 4px 4px grey;">
        <span class="hikmal">HIKMAL AFIQAH FEBRIAN <br>
            <p>Kelas : 1 TRPL A <br>
            NPM : 1062414</p>
        </span>
        </div>
        <div class="profile-item">
        <img src="NIA.jpeg" class="gmbr-nia" width="200" style="border-radius: 100px; box-shadow: 4px 4px 4px grey;">
        <span class="nia">NIA LEILA PUTRI <br>
            <p>Kelas : 1 TRPL A <br>
            NPM : 1062424</p>
        </span>
        </div>
    </div>
    </section>
<br>
    <section class="prmtsi" id="permutasi">
        <div>
        <h2 class="judul-permutasi">PERMUTASI</h2>

        <h3 class="pengertian-permutasi">Pengertian Permutasi</h3>
        <br>
        <p class="des1-permutasi">Permutasi adalah susunan atau urutan elemen-elemen dalam suatu himpunan. Dalam matematika, 
            permutasi merujuk pada cara-cara untuk mengatur atau menyusun objek-objek (misalnya angka, 
            huruf, atau benda) dari suatu himpunan dalam urutan tertentu.
        <br>
        <br>
        <b>Terdapat dua macam permutasi :</b> 
        <br><br>
        <ul style="margin-left: 40px;"><b>1. Pengulangan Berulang.</b></ul>
        <br>
           <p class="cnth-pb">Contoh : <br> 
            Kunci PIN pada handphone, angkanya bisa saja 2-4-4-9
        </ul>
        <br>
        <br>
        <ul style="margin-left: 40px;"><b>2. Permutasi Tidak Berulang</b></ul>
        <br>
            <p class="cnth-ptb">Contoh : <br>
                Tiga pembalap pertama yang melewati garis akhir, tidak mungkin satu pembalap menjadi 
                juara 1 dan juara 2 secara bersamaan.
            </p>
            <br>
        <img class="rume" src="permutasi1.png">
        <br>
        <br>
        <p class="jjp"><b>Jenis-Jenis Permutasi</b></p>
        <br>
        <ul style="margin-left: 40px;"><b>1. Permutasi unsur yang berbeda</b> </ul>
        <br>
           <img class="rume" src="permutasi2.png">
           <br>
            <p class="cnth-puyb">Contoh :<br> 
            Misalnya ada 3 unsur huruf yaitu A, B dan C</p>
        <br>
        <ul style="margin-left: 40px;"><b>2. Permutasi dengan unsur yang sama</b></ul>
        <br>
        <img class="rume" src="permutasi3.png">
        <br>
        <p class="cnth-pduys">Contoh : <br>
            Permutasi dari kata "MISS" memiliki 4 huruf</p>
        <br>
        <ul style="margin-left: 40px;"><b>3. Permutasi Siklis</b></ul>
        <br>
        <img class="rume" src="permutasi4.png">
        <br>
        <p class="cnth-psiklis">Contoh : <br>
            Ada 4 orang anak duduk secara melingkar</p>
        <br>
        <ul style="margin-left: 40px;"><b>4. Permutasi Berulang</b></ul>
        <br>
        <img class="rume" src="permutasi5.png">
        <br>
        <p class="pbr">Permutasi dapat dibagi menjadi 2, yaitu :</p>
        <br>
            <p class="pengulangan-diperbolehkan">A. Pengulangan Diperbolehkan</p>
            <br>
            <img class="rume" src="permutasi6.png">
        <br><br>
            <p class="pengulangan-tidak-dibolehkan">B. Pengulangan tidak Diperbolehkan</p>
            <br>
            <img class="rume" src="permutasi7.png">
        </div>
    </section>

    <section class="kmbnsi" id="kombinasi">
        <div>
        <h2 class="judul-kombinasi">KOMBINASI</h2>

        <h3 class="pengertian-kombinasi">Pengertian Kombinasi</h3>
        <br>
        <p class="des1-kombinasi">Kombinasi adalah cara memilih sejumlah elemen dari suatu kumpulan tanpa memperhatikan urutan. 
            Berbeda dengan permutasi yang memperhatikan urutan, dalam kombinasi, susunan elemen tidak menjadi faktor. 
            Kombinasi digunakan ketika kita hanya ingin mengetahui berapa banyak cara memilih elemen tertentu tanpa peduli bagaimana urutannya.
        <br>
        <br>

        <b>Terdapat dua macam kombinasi :</b> 
        <br>
        <br>
        <ul style="margin-left: 40px;"><b>1. Kombinasi Tanpa Pengulangan.</b> </ul>
        <br>
        <img class="rume" src="kombinasi1.png">
        <br><br>
        <p class="cnth-ktb">Contoh : <br>
            Dalam sebuah kotak terdapat 5 bola bernomor 1, 2, 3, 4, 5.
            Berapa cara memilih 3 bola tanpa memperhatikan urutan?
        </p>
        <br>
        <img class="rume" src="k1.png">
        <img class="rume" src="k2.png">
        <br>
        <br>
        <ul style="margin-left: 40px;"><b>2. Kombinasi Dengan Pengulangan</b></ul>
        <br>
        <img class="rume" src="kombinasi2.png">
        <br><br>
            <p class="cnth-kb">Contoh : <br>
                Dalam sebuah toko, ada 3 jenis buah (apel, pisang, jeruk) dan 
                kita ingin memilih 4 buah dengan pengulangan diperbolehkan. 
                Berapa cara memilihnya?
            </p>
            <br>
            <img class="rume" src="k3.png">
            <img class="rume" src="k4.png">
            <img class="rume" src="k5.png">

        </div>
    </section>

    <section class="vp" id="video">
        <h1 class="jdl-video">VIDEO PEMBELAJARAN</h1>
        <div class="vpr">
            <iframe width="800" height="400" src="https://www.youtube.com/embed/OGrdR59UEFY?si=KPfJcfAidS7zKKuP" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
        <br><br>
            <iframe width="800" height="400" src="https://www.youtube.com/embed/a3DHrNYRVbg?si=31GK3wwdHL-KlHpw" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
        </div>
        <div class="vpr">
            <iframe width="800" height="400" src="https://www.youtube.com/embed/bHA4AztiM0s?si=a2AQeA8NyYPP1rA-" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
        <br><br>
            <iframe width="800" height="400" src="https://www.youtube.com/embed/GC8GiIuOqmY?si=NL2Ib5kdDtQnb1pr" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
        </div>
        <br>
        <iframe width="860" height="400" src="https://www.youtube.com/embed/xpq6ful12Bo?si=HhocQXxiei-UVB25" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
    </section>

    <section class="cal1" id="kalkulator">
        <h1>KALKULATOR</h1>
        <div class="container">
            <h2>Kalkulator Permutasi dan Kombinasi</h2>
            <div>
                <label for="tipe">Pilih:</label>
                <input type="radio" id="permutasi" name="tipe" value="permutasi" checked>
                <label for="permutasi">Permutasi</label>
                <input type="radio" id="kombinasi" name="tipe" value="kombinasi">
                <label for="kombinasi">Kombinasi</label>
            </div>
            <div>
                <label for="pengulangan">Pengulangan:</label>
                <input type="radio" id="tanpa-pengulangan" name="pengulangan" value="tanpa-pengulangan" checked>
                <label for="tanpa-pengulangan">Tanpa pengulangan</label>
                <input type="radio" id="dengan-pengulangan" name="pengulangan" value="dengan-pengulangan">
                <label for="dengan-pengulangan">Dengan pengulangan</label>
            </div>
            <div class="input-group">
                <label for="n">Masukkan n:</label>
                <input type="number" id="n" required>
            </div>
            <div class="input-group">
                <label for="r">Masukkan r:</label>
                <input type="number" id="r" required>
            </div>
            <button class="button" onclick="hitung()">Hitung</button>
            <div class="result" id="hasil"></div>
            <div class="steps" id="langkah"></div>
        </div>
    </section>

    <section class="quiz" id="quiz">
        <h1>QUIZ PEMBELAJARAN</h1>
    <div class="kahoot">
        <iframe width="1000" height="400" src="https://kahoot.it/challenge/04214774?challenge-id=5eeb99e0-9553-480f-86a9-07d7088b3d7e_1734500058438" frameborder="0" allowfullscreen></iframe>
    </div>
    </section>

    <script>
        function faktorial(num) {
            if (num === 0 || num === 1) return 1;
            return num * faktorial(num - 1);
        }
    
        function hitung() {
            const n = parseInt(document.getElementById('n').value);
            const r = parseInt(document.getElementById('r').value);
            const tipe = document.querySelector('input[name="tipe"]:checked').value;
            const pengulangan = document.querySelector('input[name="pengulangan"]:checked').value;
            let hasil;
            let langkah = "";

             // Validasi nilai n dan r
            if (n < r) {
                document.getElementById('hasil').textContent = "Nilai n harus lebih besar atau sama dengan nilai r.";
                document.getElementById('langkah').innerHTML = "";
                return; // Hentikan fungsi jika n < r
            }
    
            if (tipe === 'permutasi') {
                if (pengulangan === 'tanpa-pengulangan') {
                    hasil = faktorial(n) / faktorial(n - r);
                    langkah = `P(n, r) = n! / (n - r)!<br>P(${n}, ${r}) = ${n}! / (${n} - ${r})!<br>P(${n}, ${r}) = ${faktorial(n)} / ${faktorial(n - r)}<br>P(${n}, ${r}) = ${hasil}`;
                } else {
                    hasil = Math.pow(n, r);
                    langkah = `P(n, r) = n^r<br>P(${n}, ${r}) = ${n}^${r}<br>P(${n}, ${r}) = ${hasil}`;
                }
            } else if (tipe === 'kombinasi') {
                if (pengulangan === 'tanpa-pengulangan') {
                    hasil = faktorial(n) / (faktorial(r) * faktorial(n - r));
                    langkah = `C(n, r) = n! / (r! * (n - r)!)<br>C(${n}, ${r}) = ${n}! / (${r}! * (${n} - ${r})!)<br>C(${n}, ${r}) = ${faktorial(n)} / (${faktorial(r)} * ${faktorial(n - r)})<br>C(${n}, ${r}) = ${hasil}`;
                } else {
                    hasil = faktorial(n + r - 1) / (faktorial(r) * faktorial(n - 1));
                    langkah = `C'(n, r) = (n + r - 1)! / (r! * (n - 1)!)<br>C'(${n}, ${r}) = (${n} + ${r} - 1)! / (${r}! * (${n} - 1)!)<br>C'(${n}, ${r}) = ${faktorial(n + r - 1)} / (${faktorial(r)} * ${faktorial(n - 1)})<br>C'(${n}, ${r}) = ${hasil}`;
                }
            }
    
            document.getElementById('hasil').textContent = `Hasil: ${hasil}`;
            document.getElementById('langkah').innerHTML = `<strong>Penyelesaian:</strong><br>${langkah}`;
        }
    </script>

    <footer style="background-color: #333; color: white; text-align: center; padding: 20px;">
        <div>
            <p>&copy; 2024 Matematika Diskrit - Politeknik Manufaktur Negeri Bangka Belitung</p>
            <p>All Rights Reserved</p>
        </div>
        <div>
            <p>Contact Us: <a href="https://polman-babel.ac.id/" style="color: #04aa64; text-decoration: none;">info@polman-babel.ac.id</a></p>
        </div>
        <div>
            <p>Follow Us: 
                <a href="https://Instagram.com/polmanbabelofficial" target="_blank" style="color: #04aa64; text-decoration: none;">Instagram</a> | 
                <a href="https://Youtube.com/@polman-babelAcId" target="_blank" style="color: #04aa64; text-decoration: none;">Youtube</a>
            </p>
        </div>
    </footer>
    
</body>
</html>
