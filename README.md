<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>PRODI HUKUM - Portal Hukum untuk Mahasiswa</title>
  <!-- Bootstrap 5 CSS -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">
  <!-- Font Awesome 6 -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <style>
    /* ===== TEMA GELAP PREMIUM ===== */
    :root {
      --bg-body: #0b0f15;
      --sidebar-bg: #0a1e3c;
      --sidebar-hover: #123456;
      --main-bg: #1a1e24;
      --main-text: #f0f4fa;
      --card-bg: #2a2f38;
      --text-light: #f0f4fa;
      --text-muted: #a0b3cc;
      --primary-accent: #3b7cff;
      --warning-accent: #ffb347;
      --info-accent: #5fa7e7;
      --border-dark: #2a3a55;
    }

    body {
      background: var(--bg-body);
      font-family: 'Segoe UI', system-ui, sans-serif;
      color: #e0e0e0;
    }

    /* Navbar */
    .navbar {
      background-color: #0a1424 !important;
      border-bottom: 1px solid #1f2b3c;
      padding: 0.75rem 1rem;
    }
    .navbar-brand {
      font-weight: 700;
      color: #ffffff !important;
      font-size: 1.5rem;
      white-space: nowrap;
    }
    .navbar .btn-outline-warning {
      color: #ffb347;
      border-color: #ffb347;
    }
    .navbar .btn-outline-warning:hover {
      background-color: #ffb347;
      color: #0a1424;
    }
    .navbar .btn-outline-info {
      color: #5fa7e7;
      border-color: #5fa7e7;
    }
    .navbar .btn-outline-info:hover {
      background-color: #5fa7e7;
      color: #0a1424;
    }
    .navbar .btn-outline-success {
      color: #6fcf97;
      border-color: #6fcf97;
    }
    .navbar .btn-outline-success:hover {
      background-color: #6fcf97;
      color: #0a1424;
    }

    /* Sidebar kiri (biru elegan) */
    .sidebar {
      background: var(--sidebar-bg);
      border-radius: 1rem 0 0 1rem;
      box-shadow: 0 0.5rem 1.5rem rgba(0, 0, 0, 0.6);
      height: calc(100vh - 80px);
      overflow-y: auto;
      padding: 1.5rem 1rem;
      color: var(--text-light);
      border-right: 1px solid var(--border-dark);
    }
    .sidebar h5 {
      color: white;
      font-weight: 600;
      letter-spacing: 0.3px;
      margin-bottom: 1.5rem;
    }
    /* Accordion styling */
    .accordion-item {
      background-color: transparent;
      border: none;
      margin-bottom: 0.5rem;
    }
    .accordion-button {
      background-color: #123456;
      color: white;
      border: none;
      box-shadow: none;
      padding: 0.75rem 1rem;
      border-radius: 0.5rem !important;
      font-weight: 500;
    }
    .accordion-button:not(.collapsed) {
      background-color: #1e4a7a;
      color: white;
    }
    .accordion-button:focus {
      box-shadow: none;
      border-color: transparent;
    }
    .accordion-button::after {
      filter: invert(1);
    }
    .accordion-body {
      padding: 0.25rem 0 0 1.5rem;
    }
    .list-group-flush .list-group-item {
      background-color: transparent;
      color: #d0e0ff;
      border: none;
      padding: 0.5rem 1rem;
      border-radius: 0.3rem;
      margin-bottom: 0.1rem;
    }
    .list-group-flush .list-group-item:hover {
      background-color: #1f3a5e;
      color: white;
    }
    .list-group-flush .list-group-item.active {
      background-color: #2f4b73;
      color: white;
    }

    /* Main panel (gelap, agar menyatu) */
    .main-panel {
      background: var(--main-bg);
      border-radius: 0 1rem 1rem 0;
      box-shadow: 0 0.5rem 1.5rem rgba(0, 0, 0, 0.5);
      height: calc(100vh - 80px);
      overflow-y: auto;
      padding: 1.5rem;
      color: var(--main-text);
    }
    .main-panel h5 {
      color: #ffffff;
    }
    .main-panel .text-secondary {
      color: #b0c4de !important;
    }

    /* badge kategori */
    .badge-kuhp {
      background-color: #2f4b73;
      color: white;
      font-weight: 500;
    }

    /* hasil pencarian, bookmark, catatan di panel utama */
    .list-group-item {
      background-color: var(--card-bg);
      border: 1px solid #3a4a62;
      color: var(--main-text);
    }
    .list-group-item-action:hover {
      background-color: #2f3f5a;
      color: white;
    }
    .list-group-item .badge-kuhp {
      background-color: #1e4a7a;
      color: white;
    }

    /* modal */
    .modal-content {
      background-color: #1e2b3c;
      color: #eef4ff;
      border: 1px solid #2f4b73;
    }
    .modal-header, .modal-footer {
      border-color: #2f4b73;
    }
    .modal-title {
      color: white;
    }
    .btn-close {
      filter: invert(1) grayscale(100%) brightness(200%);
    }

    /* footer */
    .footer-note {
      font-size: 0.8rem;
      color: #8a9db0;
    }

    /* form kontrol */
    .form-control, .input-group-text {
      background-color: #1e2b3c;
      border-color: #2f4b73;
      color: white;
    }
    .form-control:focus {
      background-color: #243447;
      color: white;
      border-color: #3b7cff;
      box-shadow: 0 0 0 0.2rem rgba(59, 124, 255, 0.25);
    }
    .input-group-text {
      color: #a0b3cc;
    }
    .btn-primary {
      background-color: #3b7cff;
      border-color: #3b7cff;
    }
    .btn-primary:hover {
      background-color: #2563eb;
      border-color: #2563eb;
    }

    /* scrollbar premium untuk sidebar */
    .sidebar::-webkit-scrollbar {
      width: 6px;
    }
    .sidebar::-webkit-scrollbar-track {
      background: #0a1e3c;
    }
    .sidebar::-webkit-scrollbar-thumb {
      background: #2f4b73;
      border-radius: 10px;
    }
    .sidebar::-webkit-scrollbar-thumb:hover {
      background: #3b7cff;
    }

    /* bookmark icon */
    .bookmark-icon {
      color: #8a9fb0;
      transition: 0.2s;
      cursor: pointer;
    }
    .bookmark-icon.active {
      color: #ffb347;
    }
    .fa-sticky-note.text-info {
      color: #5fa7e7 !important;
    }

    /* untuk tampilan mata kuliah & skripsi */
    .mk-card, .skripsi-card {
      border-left: 4px solid #3b7cff;
      margin-bottom: 1rem;
    }
    .mk-actions, .skripsi-actions {
      display: flex;
      gap: 0.5rem;
    }
    .mk-content, .skripsi-content {
      line-height: 1.7;
      text-align: justify;
      margin-top: 0.5rem;
    }
    .mk-content p, .skripsi-content p {
      margin-bottom: 0.8rem;
    }
    .skripsi-meta {
      font-size: 0.85rem;
      color: #b0c4de;
      margin-bottom: 0.5rem;
    }

    /* dashboard card */
    .dashboard-card {
      background: var(--card-bg);
      border-radius: 1rem;
      padding: 2rem;
      text-align: center;
      border: 1px solid #3a4a62;
      max-width: 600px;
      margin: 2rem auto;
    }
    .dashboard-icon {
      font-size: 4rem;
      color: #3b7cff;
      margin-bottom: 1rem;
    }
    .dashboard-title {
      font-size: 2rem;
      font-weight: 600;
      color: white;
      margin-bottom: 1rem;
    }
    .dashboard-text {
      font-size: 1.1rem;
      color: #b0c4de;
      margin-bottom: 1.5rem;
    }

    /* Penyesuaian untuk mobile: form pencarian selalu tampil */
    .navbar .search-form {
      flex: 1 1 100%;
      margin: 0.5rem 0;
    }
    @media (min-width: 992px) {
      .navbar .search-form {
        flex: 1 1 auto;
        max-width: 50%;
        margin: 0 1rem;
      }
    }
  </style>
</head>
<body>

  <!-- Navbar (gelap) dengan form pencarian selalu tampil -->
  <nav class="navbar navbar-expand-lg shadow-sm">
    <div class="container-fluid flex-wrap flex-lg-nowrap">
      <a class="navbar-brand" href="#" onclick="showDashboard(); return false;"><i class="fas fa-gavel me-2 text-primary"></i>PRODI HUKUM</a>
      
      <!-- Form pencarian - selalu tampil, di luar tombol toggle -->
      <form class="search-form d-flex order-3 order-lg-2" id="searchForm" onsubmit="event.preventDefault(); searchPasal();">
        <div class="input-group">
          <span class="input-group-text bg-transparent"><i class="fas fa-search text-primary"></i></span>
          <input type="text" class="form-control border-start-0" id="searchInput" placeholder="Cari pasal / tanyakan..." value="">
          <button class="btn btn-primary" type="submit"><i class="fas fa-arrow-right"></i></button>
        </div>
      </form>

      <!-- Tombol toggle untuk menu bookmark, catatan, update -->
      <button class="navbar-toggler order-2 order-lg-3" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="collapse navbar-collapse order-4 order-lg-4" id="navbarNav">
        <div class="d-flex gap-2 ms-auto">
          <button class="btn btn-outline-warning" onclick="showBookmarksView()"><i class="fas fa-bookmark me-1"></i>Bookmark</button>
          <button class="btn btn-outline-info" onclick="showNotesView()"><i class="fas fa-pen me-1"></i>Catatan</button>
          <button class="btn btn-outline-success" onclick="simulateUpdate()"><i class="fas fa-sync-alt me-1"></i>Update</button>
        </div>
      </div>
    </div>
  </nav>

  <!-- Main Content -->
  <div class="container-fluid px-4 py-3">
    <div class="row g-3">
      <!-- SIDEBAR KIRI: Folder Kategori -->
      <div class="col-lg-3">
        <div class="sidebar">
          <h5 class="fw-bold"><i class="fas fa-folder me-2 text-primary"></i>Kategori</h5>
          <div class="accordion" id="sidebarAccordion">
            <!-- Semua Pasal -->
            <div class="accordion-item">
              <h2 class="accordion-header" id="headingAll">
                <button class="accordion-button" type="button" data-bs-toggle="collapse" data-bs-target="#collapseAll" aria-expanded="true" aria-controls="collapseAll">
                  <i class="fas fa-book me-2"></i> Semua Pasal
                </button>
              </h2>
              <div id="collapseAll" class="accordion-collapse collapse show" aria-labelledby="headingAll" data-bs-parent="#sidebarAccordion">
                <div class="accordion-body p-0">
                  <div class="list-group list-group-flush">
                    <a href="#" class="list-group-item list-group-item-action" data-category="KUHP Perdata" onclick="selectCategory('KUHP Perdata')">KUHP Perdata</a>
                    <a href="#" class="list-group-item list-group-item-action" data-category="KUHP Pidana Lama" onclick="selectCategory('KUHP Pidana Lama')">KUHP Pidana Lama</a>
                    <a href="#" class="list-group-item list-group-item-action" data-category="KUHP Pidana Baru" onclick="selectCategory('KUHP Pidana Baru')">KUHP Pidana Baru</a>
                  </div>
                </div>
              </div>
            </div>
            <!-- Mata Kuliah -->
            <div class="accordion-item">
              <h2 class="accordion-header" id="headingMK">
                <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#collapseMK" aria-expanded="false" aria-controls="collapseMK">
                  <i class="fas fa-graduation-cap me-2"></i> Mata Kuliah
                </button>
              </h2>
              <div id="collapseMK" class="accordion-collapse collapse" aria-labelledby="headingMK" data-bs-parent="#sidebarAccordion">
                <div class="accordion-body p-0">
                  <div class="list-group list-group-flush">
                    <a href="#" class="list-group-item list-group-item-action" onclick="showMataKuliah('Hukum Dasar')">Hukum Dasar</a>
                    <a href="#" class="list-group-item list-group-item-action" onclick="showMataKuliah('Hukum Sipil')">Hukum Sipil</a>
                    <a href="#" class="list-group-item list-group-item-action" onclick="showMataKuliah('Hukum Pidana')">Hukum Pidana</a>
                    <a href="#" class="list-group-item list-group-item-action" onclick="showMataKuliah('Hukum Internasional')">Hukum Internasional</a>
                    <a href="#" class="list-group-item list-group-item-action" onclick="showMataKuliah('Hukum Administrasi Negara')">Hukum Administrasi Negara</a>
                    <a href="#" class="list-group-item list-group-item-action" onclick="showMataKuliah('Hukum Bisnis')">Hukum Bisnis</a>
                    <a href="#" class="list-group-item list-group-item-action" onclick="showMataKuliah('Hukum Lingkungan')">Hukum Lingkungan</a>
                    <a href="#" class="list-group-item list-group-item-action" onclick="showMataKuliah('Hukum Hak Asasi Manusia')">Hukum Hak Asasi Manusia</a>
                  </div>
                </div>
              </div>
            </div>
            <!-- Skripsi Mahasiswa -->
            <div class="accordion-item">
              <h2 class="accordion-header" id="headingSkripsi">
                <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#collapseSkripsi" aria-expanded="false" aria-controls="collapseSkripsi">
                  <i class="fas fa-file-alt me-2"></i> Skripsi Mahasiswa
                </button>
              </h2>
              <div id="collapseSkripsi" class="accordion-collapse collapse" aria-labelledby="headingSkripsi" data-bs-parent="#sidebarAccordion">
                <div class="accordion-body p-0">
                  <div class="list-group list-group-flush">
                    <a href="#" class="list-group-item list-group-item-action" onclick="showSkripsi('2023')">Skripsi 2023</a>
                    <a href="#" class="list-group-item list-group-item-action" onclick="showSkripsi('2024')">Skripsi 2024</a>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- MAIN PANEL KANAN: konten dinamis -->
      <div class="col-lg-9">
        <div class="main-panel" id="mainPanel">
          <div id="viewContent">
            <!-- akan diisi oleh JavaScript -->
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- Modal Detail Pasal -->
  <div class="modal fade" id="pasalModal" tabindex="-1" aria-labelledby="pasalModalLabel" aria-hidden="true">
    <div class="modal-dialog modal-lg">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title" id="pasalModalLabel">Detail Pasal</h5>
          <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
        </div>
        <div class="modal-body" id="pasalModalBody"></div>
        <div class="modal-footer">
          <button type="button" class="btn btn-outline-secondary" data-bs-dismiss="modal">Tutup</button>
        </div>
      </div>
    </div>
  </div>

  <!-- Modal untuk Tambah/Edit Materi Mata Kuliah -->
  <div class="modal fade" id="mkModal" tabindex="-1" aria-labelledby="mkModalLabel" aria-hidden="true">
    <div class="modal-dialog">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title" id="mkModalLabel">Tambah Materi</h5>
          <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
        </div>
        <div class="modal-body">
          <form id="mkForm">
            <input type="hidden" id="mkEditId" value="">
            <div class="mb-3">
              <label for="mkTitle" class="form-label">Judul Materi</label>
              <input type="text" class="form-control" id="mkTitle" required>
            </div>
            <div class="mb-3">
              <label for="mkContent" class="form-label">Konten (gunakan baris baru untuk paragraf)</label>
              <textarea class="form-control" id="mkContent" rows="6" required></textarea>
            </div>
          </form>
        </div>
        <div class="modal-footer">
          <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Batal</button>
          <button type="button" class="btn btn-primary" onclick="saveMKItem()">Simpan</button>
        </div>
      </div>
    </div>
  </div>

  <!-- Bootstrap JS & Popper -->
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"></script>
  
  <script>
    // (JavaScript tetap sama seperti kode Anda sebelumnya, saya hanya akan menyertakan versi lengkapnya agar tidak ada bagian yang terpotong)
    // ----- DATA PASAL (INTEGRASI SUMBER HUKUM) -----
    let lawsData = [
      // KUHP Perdata - data asli (sumber: KUHPerdata)
      { id: 'perdata-1234', category: 'KUHP Perdata', number: '1234', title: 'Perikatan pada Umumnya', content: 'Pasal 1234 KUHPerdata: Tiap-tiap perikatan adalah untuk memberikan sesuatu, untuk berbuat sesuatu, atau untuk tidak berbuat sesuatu.' },
      { id: 'perdata-1243', category: 'KUHP Perdata', number: '1243', title: 'Penggantian Biaya, Rugi dan Bunga', content: 'Pasal 1243 KUHPerdata: Penggantian biaya, rugi dan bunga karena tak dipenuhinya suatu perikatan, barulah mulai diwajibkan, apabila si berutang, setelah dinyatakan lalai memenuhi perikatannya, tetap melalaikannya, atau jika sesuatu yang harus diberikan atau dilakukannya hanya dapat diberikan atau dilakukannya dalam waktu yang melampaui waktu yang telah ditentukan.' },
      { id: 'perdata-1365', category: 'KUHP Perdata', number: '1365', title: 'Perbuatan Melawan Hukum', content: 'Pasal 1365 KUHPerdata: Tiap perbuatan melawan hukum yang membawa kerugian kepada orang lain, mewajibkan orang yang karena salahnya menerbitkan kerugian itu, mengganti kerugian tersebut.' },
      { id: 'perdata-1366', category: 'KUHP Perdata', number: '1366', title: 'Tanggung Jawab atas Kelalaian', content: 'Pasal 1366 KUHPerdata: Setiap orang bertanggung jawab tidak saja untuk kerugian yang disebabkan karena perbuatannya, tetapi juga untuk kerugian yang disebabkan karena kelalaiannya atau kurang hati-hatinya.' },
      { id: 'perdata-1367', category: 'KUHP Perdata', number: '1367', title: 'Tanggung Jawab atas Perbuatan Orang Lain', content: 'Pasal 1367 KUHPerdata: Seseorang tidak hanya bertanggung jawab untuk kerugian yang disebabkan karena perbuatannya sendiri, melainkan juga untuk kerugian yang disebabkan karena perbuatan orang-orang yang menjadi tanggungannya atau disebabkan oleh barang-barang yang berada di bawah pengawasannya.' },
      { id: 'perdata-1320', category: 'KUHP Perdata', number: '1320', title: 'Syarat Sah Perjanjian', content: 'Pasal 1320 KUHPerdata: Untuk sahnya suatu perjanjian diperlukan empat syarat: 1. sepakat mereka yang mengikatkan dirinya; 2. kecakapan untuk membuat suatu perikatan; 3. suatu hal tertentu; 4. suatu sebab yang halal.' },
      { id: 'perdata-1338', category: 'KUHP Perdata', number: '1338', title: 'Kebebasan Berkontrak', content: 'Pasal 1338 KUHPerdata: Semua perjanjian yang dibuat secara sah berlaku sebagai undang-undang bagi mereka yang membuatnya. Suatu perjanjian tidak dapat ditarik kembali selain dengan sepakat kedua belah pihak, atau karena alasan-alasan yang oleh undang-undang dinyatakan cukup untuk itu. Suatu perjanjian harus dilaksanakan dengan itikad baik.' },
      
      // KUHP Pidana Lama (data sebelumnya)
      { id: 'pidana-lama-362', category: 'KUHP Pidana Lama', number: '362', title: 'Pencurian', content: 'Pasal 362 KUHP (lama): Barang siapa mengambil barang sesuatu, yang seluruhnya atau sebagian kepunyaan orang lain, dengan maksud untuk dimiliki secara melawan hukum, diancam karena pencurian, dengan pidana penjara paling lama lima tahun atau pidana denda paling banyak sembilan ratus rupiah.' },
      { id: 'pidana-lama-338', category: 'KUHP Pidana Lama', number: '338', title: 'Pembunuhan', content: 'Pasal 338 KUHP (lama): Barang siapa sengaja merampas nyawa orang lain, diancam karena pembunuhan dengan pidana penjara paling lama lima belas tahun.' },
      
      // KUHP Pidana Baru (data sebelumnya)
      { id: 'pidana-baru-476', category: 'KUHP Pidana Baru', number: '476', title: 'Pencurian', content: 'Pasal 476 UU 1/2023 (baru): Setiap orang yang mengambil suatu barang yang sebagian atau seluruhnya milik orang lain dengan maksud untuk dimiliki secara melawan hukum, dipidana karena pencurian dengan pidana penjara paling lama 5 tahun atau pidana denda paling banyak kategori V.' },
      { id: 'pidana-baru-459', category: 'KUHP Pidana Baru', number: '459', title: 'Pembunuhan', content: 'Pasal 459 UU 1/2023 (baru): Setiap orang yang merampas nyawa orang lain dengan sengaja, dipidana karena pembunuhan dengan pidana penjara paling lama 15 tahun.' }
    ];

    // ----- STATE APLIKASI -----
    let currentView = 'dashboard';        // default dashboard
    let currentMK = null;                 // mata kuliah yang sedang dibuka
    let currentSkripsiYear = null;        // tahun skripsi yang sedang dibuka
    let bookmarks = JSON.parse(localStorage.getItem('lawBookmarks')) || [];      // array of id
    let notes = JSON.parse(localStorage.getItem('lawNotes')) || {};              // object id -> text

    // Data mata kuliah disimpan di localStorage dengan kunci 'mkData'
    let mkData = JSON.parse(localStorage.getItem('mkData')) || {};

    // Data skripsi - diambil dari repository universitas (contoh data lengkap)
    const skripsiData = {
      '2023': [
        { 
          id: 'skripsi-2023-001', 
          title: 'PERLINDUNGAN HUKUM TERHADAP KORBAN ARISAN ONLINE TIDAK BERIZIN DI WILAYAH POLRES SUKABUMI KOTA',
          author: 'Aufa Dary Naufal Rusmana, Asti Sri Mulyanti, Temmy Fitriah Alfiany',
          abstract: 'Penelitian ini menjelaskan bagaimana perlindungan hukum terhadap korban yang mengalami kerugian akibat arisan berbasis online ditinjau dari pasal 1243 KUHPerdata dan bagaimana penegakan hukum terhadap pemilik arisan online tidak berizin. Pada April 2023, kasus arisan sultan di Sukabumi bermula ketika pemilik menyebarkan informasi arisan dan investasi melalui media sosial Instagram. Pemilik arisan menjanjikan keuntungan berkisar 5 hingga 10 persen. Namun setelah jatuh tempo yang disepakati, baik modal maupun keuntungan tidak pernah dikembalikan. Bentuk perlindungan hukum bagi peserta arisan online adalah dengan membayar ganti rugi sebagaimana diatur dalam Pasal 1243 KUHPerdata. Bentuk penegakan hukum terhadap pemilik arisan online dapat dijerat dengan Pasal 372 jo Pasal 378 KUHP dan/atau Undang-Undang Nomor 8 Tahun 2010.' 
        },
        {
          id: 'skripsi-2023-002',
          title: 'Analisis Yuridis Tindak Pidana Pembunuhan Berencana yang Disertai Mutilasi',
          author: 'Acyntia Agata',
          abstract: 'Penelitian ini menganalisis pertimbangan hakim dalam menjatuhkan pidana terhadap pelaku tindak pidana pembunuhan berencana yang disertai mutilasi. Studi kasus Putusan Pengadilan Negeri Sleman Nomor 349/Pid.B/2023/PN Smn dan Putusan Pengadilan Negeri Serui Nomor 50/Pid.B/2019/PN Sru. Hasil penelitian menunjukkan bahwa pertimbangan hakim didasarkan pada terpenuhinya unsur-unsur Pasal 340 KUHP tentang pembunuhan berencana serta pemberatan pidana karena tindakan mutilasi yang menimbulkan keresahan masyarakat.'
        },
        {
          id: 'skripsi-2023-003',
          title: 'Kepastian Hukum Terhadap Pelanggaran Hak Cipta di Bidang Sinematografi Berdasarkan Undang-Undang Hak Cipta dan UU ITE',
          author: 'Louis Martin Lumban Raja',
          abstract: 'Pelanggaran hak cipta di bidang sinematografi marak terjadi di tengah kemajuan teknologi. Penelitian ini mengkaji kepastian hukum bagi pemegang hak cipta sinematografi serta upaya penegakan hukum terhadap pelanggaran yang dilakukan melalui platform digital. Undang-Undang Hak Cipta dan Undang-Undang ITE memberikan perlindungan, namun implementasinya masih menghadapi kendala dalam hal pembuktian dan penindakan pelanggaran lintas yurisdiksi.'
        }
      ],
      '2024': [
        {
          id: 'skripsi-2024-001',
          title: 'ANALISIS PUTUSAN PENGADILAN NEGERI KOTA SUKABUMI NOMOR 3/PID.SUS-ANAK/2023/PN SKB DALAM PERKARA KEKERASAN SEKSUAL TERHADAP ANAK',
          author: 'Muhammad Saddam Firdaus, Ujuh Juhana',
          abstract: 'Penelitian ini bertujuan untuk mengkaji dan menganalisis bagaimana penerapan hukum dan efektivitas pemidanaan dalam putusan Pengadilan Negeri Kota Sukabumi Nomor 3/Pid.Sus-Anak/2023/PN.Skb. Kekerasan seksual terhadap anak merupakan tindakan pelecehan atau pemaksaan seksual yang dilakukan terhadap anak di bawah umur. Anak yang berhadapan dengan hukum terbukti bersalah melakukan kekerasan dengan memaksa anak melakukan hubungan seksual berulang kali, melanggar Pasal 81 ayat (1) Jo. Pasal 76D Undang-Undang Perlindungan Anak. Anak dijatuhi pidana penjara di LPKA dan pelatihan kerja.'
        },
        {
          id: 'skripsi-2024-002',
          title: 'Tinjauan Yuridis Terhadap Gugatan Perbuatan Melawan Hukum Dalam Peralihan Kepemilikan Hak Atas Tanah',
          author: 'Diaz Diani',
          abstract: 'Penelitian ini menganalisis pertimbangan hukum Hakim dalam mengkualifisir kriteria perbuatan melawan hukum dalam peralihan kepemilikan hak atas tanah serta pertimbangannya dalam mengabulkan gugatan ganti kerugian pada Putusan Pengadilan Negeri Kudus Nomor 17/Pdt.G/2023/PN Kds. Majelis Hakim menyatakan bahwa tindakan Para Tergugat adalah perbuatan melawan hukum yang melanggar hak orang lain berupa hak subyektif atas harta kekayaan. Tergugat II juga melanggar kewajiban hukumnya sebagai Notaris PPAT sebagaimana diatur dalam Pasal 16 ayat (1), (7) serta Pasal 44 Undang-Undang Nomor 2 Tahun 2014 tentang Jabatan Notaris.'
        },
        {
          id: 'skripsi-2024-003',
          title: 'ANALISIS MENGENAI DAMPAK LINGKUNGAN BERDASARKAN UNDANG-UNDANG NOMOR 6 TAHUN 2023',
          author: 'Aqilah Gina Handira',
          abstract: 'Penulisan skripsi ini adalah untuk mengetahui pelaksanaan kajian analisis mengenai dampak lingkungan (AMDAL) terhadap Undang-Undang Nomor 6 Tahun 2023, dimana terdapat perubahan kebijakan atas peraturan yang telah dihapuskan, diperbaharui maupun ditambahkan. Dokumen AMDAL merupakan prasyarat penting dalam perizinan berusaha yang semestinya tetap diprioritaskan untuk mendukung pembangunan berkelanjutan. Komisi Penilai AMDAL (KPA) sangat penting dalam memastikan efektivitas dan efisiensi proses penilaian AMDAL.'
        },
        {
          id: 'skripsi-2024-004',
          title: 'Digital Forensic dalam Pembuktian Tindak Pidana Ujaran Kebencian dalam Undang-Undang Informasi dan Transaksi Elektronik',
          author: 'Rizky Mahendra',
          abstract: 'Ujaran kebencian di media sosial yang menimbulkan konflik dan perpecahan di masyarakat seringkali tidak dilakukan oleh pemilik akun media sosial yang sebenarnya. Penelitian ini mengkaji peran digital forensic dalam pembuktian tindak pidana ujaran kebencian serta kekuatan pembuktiannya di persidangan berdasarkan Undang-Undang ITE. Studi Putusan Nomor 103/PID.SUS/2020/PN BLG dan Nomor 1379/PID.Sus/2020/PT.MDN menunjukkan bahwa digital forensic menjadi kunci dalam mengungkap pelaku sesungguhnya.'
        }
      ]
    };

    // Simpan perubahan ke localStorage
    function saveBookmarks() {
      localStorage.setItem('lawBookmarks', JSON.stringify(bookmarks));
    }
    function saveNotes() {
      localStorage.setItem('lawNotes', JSON.stringify(notes));
    }
    function saveMKData() {
      localStorage.setItem('mkData', JSON.stringify(mkData));
    }

    // ----- FUNGSI UPDATE OTOMATIS (SIMULASI) -----
    function simulateUpdate() {
      const newPasal = {
        id: 'pidana-baru-480', 
        category: 'KUHP Pidana Baru', 
        number: '480', 
        title: 'Pengeroyokan', 
        content: 'Pasal 480 UU 1/2023: Setiap orang yang turut serta dalam kekerasan terhadap orang atau barang di muka umum diancam pidana penjara paling lama 7 tahun.'
      };
      if (!lawsData.find(p => p.id === newPasal.id)) {
        lawsData.push(newPasal);
      } else {
        lawsData = lawsData.map(p => p.id === newPasal.id ? {...p, content: newPasal.content + ' [versi terbaru]'} : p);
      }
      alert('Update otomatis dari sumber hukum berhasil! (simulasi: pasal baru ditambahkan/diperbarui)');
      if (currentView === 'category' && window.currentCategory) {
        showCategoryPasal(window.currentCategory);
      }
    }

    // ----- BOOKMARK TOGGLE -----
    function toggleBookmark(id) {
      if (bookmarks.includes(id)) {
        bookmarks = bookmarks.filter(b => b !== id);
      } else {
        bookmarks.push(id);
      }
      saveBookmarks();
      refreshCurrentView();
    }

    function isBookmarked(id) {
      return bookmarks.includes(id);
    }

    // ----- CATATAN -----
    function editNote(id) {
      const existing = notes[id] || '';
      const newNote = prompt('Tulis catatan untuk pasal ini:', existing);
      if (newNote !== null) {
        if (newNote.trim() === '') {
          delete notes[id];
        } else {
          notes[id] = newNote.trim();
        }
        saveNotes();
        refreshCurrentView();
      }
    }

    // ----- MENAMPILKAN DETAIL PASAL DI MODAL -----
    function showPasalDetail(id) {
      const law = lawsData.find(l => l.id === id);
      if (!law) return;
      const bookmarked = isBookmarked(id);
      const note = notes[id] || '';
      const modalBody = document.getElementById('pasalModalBody');
      modalBody.innerHTML = `
        <h5 class="text-primary">${law.category} - Pasal ${law.number}</h5>
        <h6>${law.title}</h6>
        <p class="mt-3">${law.content}</p>
        <hr>
        <div class="d-flex gap-3 align-items-center">
          <button class="btn btn-sm ${bookmarked ? 'btn-warning' : 'btn-outline-warning'}" onclick="toggleBookmark('${law.id}'); bootstrap.Modal.getInstance(document.getElementById('pasalModal')).hide();">
            <i class="fas fa-bookmark"></i> ${bookmarked ? 'Batalkan bookmark' : 'Bookmark'}
          </button>
          <button class="btn btn-sm btn-outline-info" onclick="editNote('${law.id}'); bootstrap.Modal.getInstance(document.getElementById('pasalModal')).hide();">
            <i class="fas fa-pen"></i> Catatan
          </button>
        </div>
        ${note ? `<div class="alert alert-info mt-3"><i class="fas fa-sticky-note"></i> Catatan: ${note}</div>` : ''}
      `;
      new bootstrap.Modal(document.getElementById('pasalModal')).show();
    }

    // ----- MENAMPILKAN DETAIL SKRIPSI DI MODAL -----
    function showSkripsiDetail(id) {
      let skripsi = null;
      for (const year in skripsiData) {
        const found = skripsiData[year].find(s => s.id === id);
        if (found) {
          skripsi = found;
          break;
        }
      }
      if (!skripsi) return;
      
      const modalBody = document.getElementById('pasalModalBody');
      modalBody.innerHTML = `
        <h5 class="text-primary">${skripsi.title}</h5>
        <h6 class="text-info">Penulis: ${skripsi.author}</h6>
        <hr>
        <div class="mt-3">
          <p><strong>Abstrak:</strong></p>
          <p class="text-justify">${skripsi.abstract}</p>
        </div>
      `;
      new bootstrap.Modal(document.getElementById('pasalModal')).show();
    }

    // ----- DASHBOARD (halaman awal) -----
    function showDashboard() {
      currentView = 'dashboard';
      const html = `
        <div class="dashboard-card">
          <div class="dashboard-icon">
            <i class="fas fa-gavel"></i>
          </div>
          <div class="dashboard-title">Aplikasi dalam Pengembangan</div>
          <div class="dashboard-text">
            Portal Hukum untuk Mahasiswa Prodi Hukum sedang disempurnakan.<br>
            Silakan gunakan menu di samping untuk mengakses KUHP Perdata, Pidana,<br>
            Materi Kuliah, dan Koleksi Skripsi.
          </div>
          <div class="text-muted">
            <i class="fas fa-bookmark me-1"></i> Bookmark · 
            <i class="fas fa-pen me-1 ms-2"></i> Catatan · 
            <i class="fas fa-sync-alt me-1 ms-2"></i> Update Simulasi
          </div>
        </div>
      `;
      document.getElementById('viewContent').innerHTML = html;
    }

    // ----- FUNGSI MENAMPILKAN DAFTAR PASAL -----
    function renderPasalList(pasalArray, title = 'Daftar Pasal') {
      let html = `<h5 class="fw-bold mb-3"><i class="fas fa-list me-2 text-primary"></i>${title}</h5>`;
      if (pasalArray.length === 0) {
        html += '<p class="text-secondary">Tidak ada pasal.</p>';
      } else {
        html += '<div class="list-group">';
        pasalArray.forEach(law => {
          html += `
            <div class="list-group-item list-group-item-action d-flex justify-content-between align-items-center law-card" onclick="showPasalDetail('${law.id}')">
              <div>
                <span class="badge badge-kuhp">${law.category}</span> <strong>Pasal ${law.number}</strong> - ${law.title}
                <p class="mb-0 text-secondary small">${law.content.substring(0, 80)}…</p>
              </div>
              <div>
                <i class="fas fa-bookmark bookmark-icon ${isBookmarked(law.id) ? 'active' : ''}" onclick="event.stopPropagation(); toggleBookmark('${law.id}')"></i>
                ${notes[law.id] ? '<i class="fas fa-sticky-note ms-1 text-info" title="Ada catatan"></i>' : ''}
              </div>
            </div>
          `;
        });
        html += '</div>';
      }
      document.getElementById('viewContent').innerHTML = html;
    }

    // ----- MENAMPILKAN KATEGORI PASAL -----
    function showCategoryPasal(category) {
      window.currentCategory = category;
      const filtered = lawsData.filter(l => l.category === category);
      renderPasalList(filtered, `Kategori: ${category}`);
      document.querySelectorAll('#sidebarAccordion .list-group-item').forEach(el => {
        el.classList.remove('active');
        if (el.getAttribute('data-category') === category) {
          el.classList.add('active');
        }
      });
      currentView = 'category';
    }

    function selectCategory(cat) {
      showCategoryPasal(cat);
      document.getElementById('searchInput').value = '';
    }

    // ----- PENCARIAN -----
    function searchPasal() {
      const query = document.getElementById('searchInput').value.toLowerCase().trim();
      if (!query) {
        renderPasalList([]);
        return;
      }
      const results = lawsData.filter(law => 
        law.content.toLowerCase().includes(query) || 
        law.title.toLowerCase().includes(query) || 
        law.number.toLowerCase().includes(query) ||
        law.category.toLowerCase().includes(query)
      );
      renderPasalList(results, `Hasil pencarian: "${query}"`);
      currentView = 'search';
    }

    // ----- VIEW BOOKMARK & CATATAN -----
    function renderBookmarksView() {
      const bookmarkedLaws = lawsData.filter(l => bookmarks.includes(l.id));
      renderPasalList(bookmarkedLaws, 'Bookmark Saya');
      currentView = 'bookmarks';
    }
    function renderNotesView() {
      const notedIds = Object.keys(notes);
      const notedLaws = lawsData.filter(l => notedIds.includes(l.id));
      let html = '<h5 class="fw-bold mb-3"><i class="fas fa-pen me-2 text-info"></i>Catatan Saya</h5>';
      if (notedLaws.length === 0) {
        html += '<p class="text-secondary">Belum ada catatan.</p>';
      } else {
        html += '<div class="list-group">';
        notedLaws.forEach(law => {
          html += `
            <div class="list-group-item list-group-item-action" onclick="showPasalDetail('${law.id}')">
              <div class="d-flex justify-content-between">
                <span class="badge badge-kuhp">${law.category}</span>
                <i class="fas fa-bookmark ${isBookmarked(law.id) ? 'text-warning' : 'text-secondary'}" onclick="event.stopPropagation(); toggleBookmark('${law.id}')"></i>
              </div>
              <strong>Pasal ${law.number}</strong> - ${law.title}
              <div class="alert alert-light mt-2 p-2 small" style="background-color:#2a2f38; color:#b0c4de;">📝 ${notes[law.id]}</div>
            </div>
          `;
        });
        html += '</div>';
      }
      document.getElementById('viewContent').innerHTML = html;
      currentView = 'notes';
    }
    function showBookmarksView() { renderBookmarksView(); }
    function showNotesView() { renderNotesView(); }

    // ----- FUNGSI UNTUK MATA KULIAH (PENYIMPANAN PERMANEN) -----
    function showMataKuliah(mkName) {
      currentMK = mkName;
      if (!mkData[mkName]) {
        mkData[mkName] = []; // inisialisasi array kosong
        saveMKData();
      }
      renderMKView(mkName);
      currentView = 'mk';
    }

    // Helper: mengubah teks dengan newline menjadi paragraf
    function formatContent(text) {
      if (!text) return '';
      const lines = text.split('\n');
      const paragraphs = lines.filter(line => line.trim() !== '').map(line => `<p>${line}</p>`);
      return paragraphs.join('');
    }

    function renderMKView(mkName) {
      const items = mkData[mkName] || [];
      let html = `
        <h5 class="fw-bold mb-3"><i class="fas fa-graduation-cap me-2 text-info"></i>${mkName}</h5>
        <button class="btn btn-primary mb-3" onclick="showAddMKItem('${mkName}')"><i class="fas fa-plus"></i> Tambah Materi</button>
      `;
      if (items.length === 0) {
        html += '<p class="text-secondary">Belum ada materi. Klik "Tambah Materi" untuk mulai.</p>';
      } else {
        html += '<div class="list-group">';
        items.forEach((item) => {
          html += `
            <div class="list-group-item mk-card">
              <div class="d-flex justify-content-between align-items-start">
                <div style="flex:1;">
                  <h6 class="fw-bold">${item.title}</h6>
                  <div class="mk-content">${formatContent(item.content)}</div>
                </div>
                <div class="mk-actions">
                  <button class="btn btn-sm btn-outline-warning" onclick="editMKItem('${mkName}', ${item.id})"><i class="fas fa-edit"></i></button>
                  <button class="btn btn-sm btn-outline-danger" onclick="deleteMKItem('${mkName}', ${item.id})"><i class="fas fa-trash"></i></button>
                </div>
              </div>
            </div>
          `;
        });
        html += '</div>';
      }
      document.getElementById('viewContent').innerHTML = html;
    }

    // Modal handling untuk tambah/edit materi MK
    let currentMKForModal = null;
    let currentEditId = null;

    function showAddMKItem(mkName) {
      currentMKForModal = mkName;
      currentEditId = null;
      document.getElementById('mkTitle').value = '';
      document.getElementById('mkContent').value = '';
      document.getElementById('mkModalLabel').innerText = 'Tambah Materi';
      new bootstrap.Modal(document.getElementById('mkModal')).show();
    }

    function editMKItem(mkName, id) {
      currentMKForModal = mkName;
      currentEditId = id;
      const item = mkData[mkName].find(i => i.id === id);
      if (item) {
        document.getElementById('mkTitle').value = item.title;
        document.getElementById('mkContent').value = item.content;
        document.getElementById('mkModalLabel').innerText = 'Edit Materi';
        new bootstrap.Modal(document.getElementById('mkModal')).show();
      }
    }

    function deleteMKItem(mkName, id) {
      if (confirm('Hapus materi ini?')) {
        mkData[mkName] = mkData[mkName].filter(i => i.id !== id);
        saveMKData();
        renderMKView(mkName);
      }
    }

    function saveMKItem() {
      const title = document.getElementById('mkTitle').value.trim();
      const content = document.getElementById('mkContent').value.trim();
      if (!title || !content) {
        alert('Judul dan konten harus diisi!');
        return;
      }
      if (!currentMKForModal) return;

      if (currentEditId) {
        // edit
        const index = mkData[currentMKForModal].findIndex(i => i.id === currentEditId);
        if (index !== -1) {
          mkData[currentMKForModal][index].title = title;
          mkData[currentMKForModal][index].content = content;
        }
      } else {
        // tambah baru
        const newId = Date.now();
        mkData[currentMKForModal].push({ id: newId, title, content });
      }
      saveMKData();
      // tutup modal
      bootstrap.Modal.getInstance(document.getElementById('mkModal')).hide();
      renderMKView(currentMKForModal);
    }

    // ----- FUNGSI UNTUK SKRIPSI (data dari repository) -----
    function showSkripsi(year) {
      currentSkripsiYear = year;
      renderSkripsiView(year);
      currentView = 'skripsi';
    }

    function renderSkripsiView(year) {
      const items = skripsiData[year] || [];
      let html = `
        <h5 class="fw-bold mb-3"><i class="fas fa-file-alt me-2 text-info"></i>Skripsi Mahasiswa ${year}</h5>
      `;
      if (items.length === 0) {
        html += '<p class="text-secondary">Belum ada data skripsi untuk tahun ini.</p>';
      } else {
        html += '<div class="list-group">';
        items.forEach((item) => {
          html += `
            <div class="list-group-item skripsi-card" onclick="showSkripsiDetail('${item.id}')">
              <div class="d-flex justify-content-between align-items-start">
                <div style="flex:1;">
                  <h6 class="fw-bold">${item.title}</h6>
                  <div class="skripsi-meta">Penulis: ${item.author}</div>
                  <div class="skripsi-content small">${item.abstract.substring(0, 150)}…</div>
                </div>
              </div>
            </div>
          `;
        });
        html += '</div>';
      }
      document.getElementById('viewContent').innerHTML = html;
    }

    // refresh tampilan saat ini (misal setelah toggle bookmark)
    function refreshCurrentView() {
      if (currentView === 'dashboard') showDashboard();
      else if (currentView === 'bookmarks') renderBookmarksView();
      else if (currentView === 'notes') renderNotesView();
      else if (currentView === 'category' && window.currentCategory) {
        showCategoryPasal(window.currentCategory);
      } else if (currentView === 'search') {
        const query = document.getElementById('searchInput').value.trim();
        if (query) searchPasal(); else showDashboard();
      } else if (currentView === 'mk' && currentMK) {
        renderMKView(currentMK);
      } else if (currentView === 'skripsi' && currentSkripsiYear) {
        renderSkripsiView(currentSkripsiYear);
      } else {
        showDashboard();
      }
    }

    // Inisialisasi awal: tampilkan dashboard
    window.onload = function() {
      showDashboard();
    };
  </script>

  <!-- footer small -->
  <footer class="text-center footer-note mt-3">
    <span>Terintegrasi dengan sumber hukum Indonesia (simulasi update otomatis). Data KUHP Perdata, Pidana Lama & Baru.</span>
  </footer>
</body>
</html>
