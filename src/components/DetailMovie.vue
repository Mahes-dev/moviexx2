<template>
    <div class="container">
        <div class="header">
            <h1 class="header-title">INDO XX2</h1>
            <h3 class="header-subtitle">Kumpulan Film Indonesia Tergokil</h3>
        </div>
        <div class="movie" v-for="(data, index) in movie" :value="data" :key="index">
            <div class="movie-item" v-if="filmId == data.id">
                <h1 class="page-title">Movie Details</h1>
                <img v-bind:src="data.image"  class="img-fluid img-movie" v-bind:alt="data">
                <div>
                    <h1>{{data.title}}</h1>
                    <h2>IMDb : {{data.rating}}</h2>
                    <h4>{{data.release}} | {{data.duration}} | {{data.genre}} | {{data.age}}</h4>
                    <br/><br/>
                    <p>Director : {{data.director}}</p>
                    <p>Cast by : {{data.cast}}</p>
                    <h4>SYNOPSYS</h4>
                    <p class="desc">{{data.desc}}</p>
                </div>
            </div>
        </div>
        <div class="back">
            <router-link to='/'><button class="btn-back">BACK TO HOME</button></router-link>
        </div>
        <div class="footer">
            <h5>Copyright &copy;2020. Created by Great Mahes. All rights reserved</h5>
        </div>
    </div>
</template>
<script>
import Img1 from '../assets/movie/akubencidancinta.jpg';
import Img2 from '../assets/movie/dilan1991.jpg';
import Img3 from '../assets/movie/asih.jpg';
import Img4 from '../assets/movie/sesuaiapk.jpg';
import Img5 from '../assets/movie/comic8.jpg';
import Img6 from '../assets/movie/yowisben2.jpg';
import Img7 from '../assets/movie/theraid.jpg';
import Img8 from '../assets/movie/imperfect.jpg';


export default {
  data() {
    return {
      filmId: this.$route.params.id,
      movie: [
        {
          id: 1,
          image: Img1,
          title: 'A: Aku, Benci & Cinta (2017)',
          rating: '7,5/10',
          release: '16 Agustus 2017',
          duration: '1 j 35 m',
          genre: 'Drama, Romance',
          age: '13+',
          director: 'Rizki Balki',
          cast: 'Indah Permatasari, Jefri Nichol, Amanda Rawles, and many more.',
          desc: 'Bagi Anggia (Indah Permatasari), Alvaro (Jefri Nichol) adalah cowok yang paling menyebalkan di sekolah. Alvaro jadi ketua OSIS, sedangkan Anggia jadi wakilnya. Setiap kali rapat, mereka tidak pernah akur. Suatu ketika Anggia tidak setuju rencana diadakannya prom. Alvaro pun mengejek bahwa Anggia takut tidak akan dapat pasangan. Untungnya ada sahabat kakak Anggia yang bernama Alex (Brandon Salim) yang penuh perhatian dan pengertian. Namun kemudian nasib terus menyatukan Anggia dan Alvaro. Alvaro ditugaskan untuk menjadi tutor musik bagi Anggia setiap kali jam sekolah usai. Hari demi hari membuat Anggia mengenal Alvaro lebih dekat sehingga mulai menimbulkan kekaguman dan rasa suka di antara keduanya. Namun, tidak mudah bagi keduanya untuk mengakui perasaan tersebut. Masih ada Alex dalam kehidupan Anggia, sedangkan Alvaro masih memiliki Athala (Amanda Rawles), gadis yang masih terbaring koma.',
        },
        {
          id: 2,
          image: Img2,
          title: 'Dilan 1991 (2020)',
          rating: '0,0/10',
          release: '28 Februari 2020',
          duration: '2j 1m',
          genre: 'Drama, Romance',
          age: '13+',
          director: 'Pidi Baiq, Fajar Bustomi',
          cast: ' Iqbaal Dhiafakhri Ramadhan, Vanesha Prescilla, Ira Wibowo, and many more.',
          desc: '22 Desember 1990, Dilan (Iqbaal Ramadhan) dan Milea (Vanesha Prescilla) resmi berpacaran. Ditengah kebahagiaan mereka Dilan terancam dikeluarkan dari sekolah akibat perkelahian dengan Anhar (Giulio Parengkuan). Dilan juga semakin sering berkelahi dan mendapatkan musuh. Milea khawatir dengan masa depan Dilan. Milea merasa berhak melarang Dilan terlibat dalam geng motor. Suatu ketika, Dilan dikeroyok oleh orang tak dikenal. Saat mengetahui siapa yang berbuat, Dilan merencanakan balas dendam. Milea akhirnya meminta Dilan berhenti dari geng motor atau hubungan mereka berakhir. Dilan, seorang panglima tempur dan ketua geng motor akan selalu terlibat masalah. Di tengah semua masalah itu, hadir Yugo (Jerome Kurnia), anak dari sepupu jauh ayah Milea yang baru pulang dari Belgia. Mereka sering menghabiskan waktu bersama. Yugo menyukai Milea, dan Milea hanya mencintai Dilan.',
        },
        {
          id: 3,
          image: Img3,
          title: 'ASIH (2018)',
          rating: '5.2/10',
          release: '11 Oktober 2018',
          duration: '1j 17m',
          genre: 'Horror',
          age: '17+',
          director: 'Awi Suryadi',
          cast: 'Shareefa Daanish, Citra Kirana, Darius Sinathrya, Marini, Alex Abbad, Djenar Maesa Ayu, and many more.',
          desc: '37 tahun sebelum peristiwa di film Danur, Ita, seorang wanita yang hamil tua, hidup bersama dengan suaminya, Andi, dan ibunya di sekitar Kota Bandung. Ita khawatir karena Amelia lahir sebulan lebih awal. Bidan yang mengurus kelahiran Amelia, Sekar Nurmala, tidak mempermasalahkan ini, tetapi dia berpesan bahwa Ita harus waspada terhadap makhluk gaib selama 40 hari kedepan. Pasalnya, dia mendengar bahwa, di desa sebelah, seorang wanita bernama Asih baru saja bunuh diri setelah membunuh anaknya sendiri. Dia juga menceritakan mengenai Abah, seorang sakti yang juga tinggal di desa sebelah dan memiliki kemampuan untuk melacak hal supranatural. Suatu hari, Ita menemukan sebuah sisir di depan tempat tidur Amelia. Dia tidak menyadari hantu Asih yang berdiri didekatnya. Hari-hari berikutnya, Ita dan ibunya diteror oleh Asih. Andi awalnya tidak percaya, tetapi dia berubah pikiran setelah dia melihat Asih memakan ari-ari Amelia yang dikuburkan di belakang rumah. Kengerian berujung ketika, tepat seminggu setelah Amelia lahir, dia hilang saat Ita sedang memandikannya. Ita mendesak Andi untuk meminta bantuan dari Abah. Abah menceritakan latar belakang Asih. Dilahirkan dengan nama Kasih, dia merantau ke kota hanya untuk kembali dengan keadaan hamil tanpa suami. Dicampakkan oleh orang tua dan penduduk desa, Asih memilih untuk membunuh bayinya dan dirinya sendiri. Semenjak saat itu, dia mencari anak lain untuk mengganti bayinya. Pohon beringin tempat dimana Asih mengakhiri hidupnya ternyata terletak hanya beberapa meter dari rumah Andi dan Ita. Mereka berhasil menemukan Amelia setelah Abah menyuruh Andi mengumandangkan azan di depan pohon, tetapi Asih berpindah merasuki Ita dan memaksanya untuk menenggelamkan Amelia. Berkat bantuan Abah, Ita berhasil menghalau pengaruh Asih sebelum dia dapat membunuh Amelia. Keesokan harinya, ibu menancapkan sisir Asih di pohon beringin sesuai dengan saran Abah. 37 tahun kemudian, di pohon yang sama, sisir Asih diambil oleh Riri.',
        },
        {
          id: 4,
          image: Img4,
          title: 'Sesuai Aplikasi (2018)',
          rating: '6.8/10',
          release: '6 December 2018',
          duration: '1j 29m',
          genre: 'Action, Comedy',
          age: '17+',
          director: 'Adink Liwutang',
          cast: '  Valentino Peter, Lolox, Ernest Prakasa, and many more.',
          desc: 'Cerita persahabatan dua driver ojek online, Pras (Valentino Peter) dan Duras (Lolox). Keduanya harus berjuang untuk memenuhi kebutuhan hidup mereka. Suatu hari Sakti (Ernest Prakasa) seorang pencuri ulung yang berkedok pemilik warung kopi bernama Nasgitel (Panas Legi Kentel) kehilangan barang curiannya. Rupanya berlian yang ia curi dari Ci Asiu sang rentenir (Dayu Wijanto) itu tak sengaja terbawa oleh diva dangdut Sofiyah (Titi Kamal).',
        },
        {
          id: 5,
          image: Img5,
          title: 'COMIC 8 (2014)',
          rating: '7.0/10',
          release: '29 January 2014',
          duration: '1j 46m',
          genre: 'Action, Comedy',
          age: '17+',
          director: 'Anggy Umbara',
          cast: ' Ernest Prakasa, Kemal Palevi, Arie Kriting, and many more.',
          desc: 'Delapan anak muda masing-masing mempunyai alasan dan motif yang berbeda-beda dalam melakukan perampokan bank. Ada yang merampok karena galau, hobi, iseng, olahraga adrenalin, bahkan ada yang merampok untuk menghidupi panti asuhan dan rakyat miskin. Kedelapan Perampok tersebut akan terbagi menjadi tiga tim dengan kemampuan dan jam terbang yang berbeda-beda. Aksi pun berkembang dari perampokan yang awalnya terlihat seperti kebetulan yang aneh, terkepung oleh pasukan polisi dengan AKP-nya yang super cantik, sampai akhirnya mereka harus saling bekerja sama dan menemukan jawaban dari teka teki yang ada serta mencari jalan keluar terbaik untuk semua.',
        },
        {
          id: 6,
          image: Img6,
          title: 'Yowis Ben 2 (2019)',
          rating: '7.4/10',
          release: '14 March 2019',
          duration: '1j 49m',
          genre: 'Comedy, Drama',
          age: '13+',
          director: 'Fajar Nugros, Bayu Skak',
          cast: ' Bayu Skak, Joshua Suherman, Brandon Salim, and many more.',
          desc: 'Usai diputus Susan (Cut Meyriska), Bayu (Bayu Skak) dihadapkan pada naiknya harga kontrakan yang membuat dia, ibunya dan Cak Jon (Arief Didu) terancam diusir. Untungnya Yowis Ben populer di Malang dan jadi satu-satunya harapan Bayu menyelesaikan persoalan keuangan. Celakanya masing-masing personil menyimpan masalah. Yayan (Tutus Thomson) menikah dengan Mia (Anggika Bolsterli); krisis keluarga Nando (Brandon Salim) karena ayahnya memutuskan menikah lagi; dan Doni (Joshua Suherman) berambisi punya pacar. Bayu memecat Cak Jon, lalu mempercayakan Yowis Ben kepada Cak Jim (Timo Scheunemann), yang mengklaim dirinya sudah membesarkan banyak artis nasional. Mereka pun hijrah ke Bandung. Tapi, kredibilitas Cak Jim mencurigakan dan Bayu juga harus meluluhkan hati bapak super galak karena dia jatuh cinta dengan Asih (Anya Geraldine), putrinya.',
        },
        {
          id: 7,
          image: Img7,
          title: 'The Raid: Redemption (2011)',
          rating: '7,6/10',
          release: '21 Maret 2012',
          duration: '1j 41m',
          genre: 'Action, Thriller',
          age: '17+',
          director: 'Gareth Evans',
          cast: 'Iko Uwais, Ananda George, Ray Sahetapy, and many more.',
          desc: 'Di jantung daerah kumuh Jakarta berdiri sebuah gedung apartemen tua yang menjadi markas persembunyian para pembunuh dan bandit kelas dunia yang paling berbahaya. Sampai saat ini, blok apartemen kumuh tersebut telah dianggap tidak pernah tersentuh siapa pun, bahkan untuk perwira polisi yang paling berani sekalipun. Diam-diam di bawah kegelapan dan keheningan fajar, sebuah tim elit SWAT (pasukan khusus) berjumlah 20 orang ditugaskan untuk menyerbu apartemen persembunyian tersebut untuk menyergap gembong narkotik terkenal yang menguasai gedung tersebut. Tapi ketika sebuah pertemuan dengan seorang pengintai membuka rencana mereka dan berita tentang serangan mereka mencapai sang gembong narkotik, lampu dalam gedung tiba-tiba padam dan semua pintu keluar diblokir. Terdampar di lantai enam dan tanpa jalan keluar, satuan khusus tersebut harus berjuang melawan penjahat-penjahat terburuk dan terkejam untuk bertahan hidup dalam misi penyerbuan tersebut.',
        },
        {
          id: 8,
          image: Img8,
          title: 'Imperfect (2019)',
          rating: '8,1/10',
          release: '19 December 2019',
          duration: '1j 53m',
          genre: 'Comedy, Drama, Family',
          age: '13+',
          director: 'Ernest Prakasa',
          cast: 'Jessica Mila, Reza Rahadian, Yasmin Napper, and many more.',
          desc: 'Berkisah mengenai Rara (Jessica Mila) yang terlahir dengan gen gemuk dan kulit sawo matang, warisan sang ayah. Sementara, adiknya Lulu (Yasmin Napper) mengikuti gen ibu mereka Debby (Karina Suwandi) yang merupakan mantan peragawati tahun 1990-an. Rara sendiri bekerja sebagai manajer riset di sebuah perusahaan kosmetik. Meski mendapat perlakuan tidak menyenangkan dari lingkungan sekitar, namun Rara mencintai pekerjaannya. Untung ada Dika (Reza Rahadian), kekasih yang mencintai Rara apa adanya. Suatu hari, muncul peluang bagi Rara untuk naik jabatan di kantor, tapi bos Rara yakni KELVIN (Dion Wiyoko) mengharuskan Rara mengubah total penampilannya jika ia mau mengemban tanggung jawab baru ini.',
        },
      ],
    };
  },
};
</script>
<style scoped>
    .container {
        width: auto;
    }
    .header {
        padding: 50px;
        grid-column: 1/5;
        background-color: #FF007F;
        color: #fff;
        text-align: left;
    }
    .header-title {
      font-family: monospace;
      font-size: 80px;
      color: #fff;
    }
    .header-subtitle {
      font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
      font-size: 20px;
    }
    .movie-item {
        padding: 50px;
        width: auto;
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        grid-auto-rows: minmax(50px, auto);
        text-align: left;
        background-color: #ededed;
    }
    .page-title {
        grid-column: 1/3;
        text-align: center;
        padding-bottom: 30px;
        background-color: #ededed;
        color: #fc6363;
        font-family: 'Times New Roman', Times, serif;
    }
    .back {
      text-align: center;
      padding-bottom: 50px;
      background-color: #ededed;
    }
    .btn-back {
        background-color: #fc6363;
        color: #fff;
        border: 0px;
        border-radius: 60px;
        text-align: center;
        margin: 5px 2px;
        padding: 20px 15px;
        cursor: pointer;
        transition: 0.3s;
        margin: 20px;
        width: 300px;
    }
    .btn-back:hover {
        background-color: transparent;
        border: 2px solid #fc6363;
        color: #fc6363;
    }
    .img-movie {
        width: 500px;
        box-shadow: 0 20px 25px 0 rgba(0,0,0,0.2);
        transition: 0.3s ease;
    }
    .desc {
        text-align: justify;
    }
    .footer {
        padding: 10px;
        grid-column: 1/5;
        background-color: #fc6363;
        color: #fff;
        text-align: center;
    }
</style>
