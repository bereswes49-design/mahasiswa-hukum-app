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
    /* ===== TEMA MERAH PREMIUM ===== */
    :root {
      --bg-body: #0b0f15;
      --sidebar-bg: #8B0000;        /* merah marun */
      --sidebar-hover: #A52A2A;      /* merah kecoklatan */
      --main-bg: #1a1e24;
      --main-text: #f0f4fa;
      --card-bg: #2a2f38;
      --text-light: #f0f4fa;
      --text-muted: #a0b3cc;
      --primary-accent: #B22222;     /* merah firebrick */
      --warning-accent: #ffb347;
      --info-accent: #5fa7e7;
      --border-dark: #5a2a2a;        /* merah gelap */
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
    /* Tombol login/registrasi */
    .navbar .btn-outline-light {
      color: #ffffff;
      border-color: #ffffff;
    }
    .navbar .btn-outline-light:hover {
      background-color: #ffffff;
      color: #0a1424;
    }

    /* Sidebar kiri (merah) */
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
      background-color: #A52A2A;      /* merah hover */
      color: white;
      border: none;
      box-shadow: none;
      padding: 0.75rem 1rem;
      border-radius: 0.5rem !important;
      font-weight: 500;
    }
    .accordion-button:not(.collapsed) {
      background-color: #B22222;      /* merah lebih terang */
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
      color: #ffe0e0;
      border: none;
      padding: 0.5rem 1rem;
      border-radius: 0.3rem;
      margin-bottom: 0.1rem;
    }
    .list-group-flush .list-group-item:hover {
      background-color: #A52A2A;
      color: white;
    }
    .list-group-flush .list-group-item.active {
      background-color: #B22222;
      color: white;
    }

    /* Main panel (gelap) */
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
      background-color: #B22222;
      color: white;
      font-weight: 500;
    }

    /* hasil pencarian, bookmark, catatan di panel utama */
    .list-group-item {
      background-color: var(--card-bg);
      border: 1px solid #5a2a2a;
      color: var(--main-text);
    }
    .list-group-item-action:hover {
      background-color: #6a2a2a;
      color: white;
    }
    .list-group-item .badge-kuhp {
      background-color: #B22222;
      color: white;
    }

    /* modal */
    .modal-content {
      background-color: #1e2b3c;
      color: #eef4ff;
      border: 1px solid #5a2a2a;
    }
    .modal-header, .modal-footer {
      border-color: #5a2a2a;
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
      border-color: #5a2a2a;
      color: white;
    }
    .form-control:focus {
      background-color: #243447;
      color: white;
      border-color: #B22222;
      box-shadow: 0 0 0 0.2rem rgba(178, 34, 34, 0.25);
    }
    .input-group-text {
      color: #a0b3cc;
    }
    .btn-primary {
      background-color: #B22222;
      border-color: #B22222;
    }
    .btn-primary:hover {
      background-color: #8B0000;
      border-color: #8B0000;
    }

    /* scrollbar premium untuk sidebar */
    .sidebar::-webkit-scrollbar {
      width: 6px;
    }
    .sidebar::-webkit-scrollbar-track {
      background: #8B0000;
    }
    .sidebar::-webkit-scrollbar-thumb {
      background: #B22222;
      border-radius: 10px;
    }
    .sidebar::-webkit-scrollbar-thumb:hover {
      background: #ff4d4d;
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
    .mk-card, .skripsi-card, .pasal-card {
      border-left: 4px solid #B22222;
      margin-bottom: 1rem;
    }
    .mk-actions, .skripsi-actions, .pasal-actions {
      display: flex;
      gap: 0.5rem;
    }
    .mk-content, .skripsi-content, .pasal-content {
      line-height: 1.7;
      text-align: justify;
      margin-top: 0.5rem;
    }
    .mk-content p, .skripsi-content p, .pasal-content p {
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
      color: #B22222;
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

    /* Style untuk tampilan skripsi seperti dokumen formal */
    .skripsi-dokumen {
      background: white;
      color: black;
      padding: 2cm 1.5cm;
      margin: 0;
      font-family: 'Times New Roman', serif;
      font-size: 12pt;
      line-height: 1.5;
      text-align: justify;
      max-width: 210mm; /* A4 width */
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }
    .skripsi-dokumen .judul {
      font-size: 14pt;
      font-weight: bold;
      text-align: center;
      margin-bottom: 1cm;
    }
    .skripsi-dokumen .penulis {
      text-align: center;
      margin-bottom: 1cm;
    }
    .skripsi-dokumen .abstrak {
      margin-top: 1cm;
      margin-bottom: 1cm;
    }
    .skripsi-dokumen .abstrak h6 {
      font-weight: bold;
    }
    .skripsi-dokumen .konten {
      margin-top: 1cm;
    }
  </style>
</head>
<body>

  <!-- Navbar (gelap) dengan form pencarian selalu tampil dan tombol login/registrasi -->
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

      <!-- Tombol toggle untuk menu bookmark, catatan, update, login -->
      <button class="navbar-toggler order-2 order-lg-3" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="collapse navbar-collapse order-4 order-lg-4" id="navbarNav">
        <div class="d-flex gap-2 ms-auto">
          <button class="btn btn-outline-warning" onclick="showBookmarksView()"><i class="fas fa-bookmark me-1"></i>Bookmark</button>
          <button class="btn btn-outline-info" onclick="showNotesView()"><i class="fas fa-pen me-1"></i>Catatan</button>
          <button class="btn btn-outline-success" onclick="simulateUpdate()"><i class="fas fa-sync-alt me-1"></i>Update</button>
          <!-- Tombol Login & Registrasi -->
          <button class="btn btn-outline-light" onclick="alert('Fitur login dalam pengembangan')">Login</button>
          <button class="btn btn-outline-light" onclick="alert('Fitur registrasi dalam pengembangan')">Registrasi</button>
        </div>
      </div>
    </div>
  </nav>

  <!-- Main Content -->
  <div class="container-fluid px-4 py-3">
    <div class="row g-3">
      <!-- SIDEBAR KIRI: Folder Kategori (merah) -->
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
                    <a href="#" class="list-group-item list-group-item-action" data-category="KUH PERDATA" onclick="selectCategory('KUH PERDATA')">KUH PERDATA</a>
                    <a href="#" class="list-group-item list-group-item-action" data-category="KUHP LAMA" onclick="selectCategory('KUHP LAMA')">KUHP LAMA</a>
                    <a href="#" class="list-group-item list-group-item-action" data-category="KUHP BARU" onclick="selectCategory('KUHP BARU')">KUHP BARU</a>
                    <a href="#" class="list-group-item list-group-item-action" data-category="KUHAP BARU" onclick="selectCategory('KUHAP BARU')">KUHAP BARU</a>
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
                    <a href="#" class="list-group-item list-group-item-action" onclick="showSkripsiList()">Daftar Skripsi</a>
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
          <h5 class="modal-title" id="pasalModalLabel">Detail</h5>
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

  <!-- Modal untuk Tambah/Edit Pasal -->
  <div class="modal fade" id="pasalModalEdit" tabindex="-1" aria-labelledby="pasalModalEditLabel" aria-hidden="true">
    <div class="modal-dialog">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title" id="pasalModalEditLabel">Tambah/Ubah Pasal</h5>
          <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
        </div>
        <div class="modal-body">
          <form id="pasalForm">
            <input type="hidden" id="pasalEditId" value="">
            <input type="hidden" id="pasalCategory" value="">
            <div class="mb-3">
              <label for="pasalNumber" class="form-label">Nomor Pasal</label>
              <input type="text" class="form-control" id="pasalNumber" required>
            </div>
            <div class="mb-3">
              <label for="pasalTitle" class="form-label">Judul Pasal</label>
              <input type="text" class="form-control" id="pasalTitle" required>
            </div>
            <div class="mb-3">
              <label for="pasalContent" class="form-label">Konten (gunakan baris baru untuk paragraf)</label>
              <textarea class="form-control" id="pasalContent" rows="8" required></textarea>
            </div>
          </form>
        </div>
        <div class="modal-footer">
          <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Batal</button>
          <button type="button" class="btn btn-primary" onclick="savePasalItem()">Simpan</button>
        </div>
      </div>
    </div>
  </div>

  <!-- Modal untuk Tambah/Edit Skripsi -->
  <div class="modal fade" id="skripsiModal" tabindex="-1" aria-labelledby="skripsiModalLabel" aria-hidden="true">
    <div class="modal-dialog modal-lg">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title" id="skripsiModalLabel">Tulis Skripsi</h5>
          <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
        </div>
        <div class="modal-body">
          <form id="skripsiForm">
            <input type="hidden" id="skripsiEditId" value="">
            <div class="mb-3">
              <label for="skripsiJudul" class="form-label">Judul Skripsi</label>
              <input type="text" class="form-control" id="skripsiJudul" required>
            </div>
            <div class="mb-3">
              <label for="skripsiPenulis" class="form-label">Penulis</label>
              <input type="text" class="form-control" id="skripsiPenulis" required>
            </div>
            <div class="mb-3">
              <label for="skripsiAbstrak" class="form-label">Abstrak</label>
              <textarea class="form-control" id="skripsiAbstrak" rows="4" required></textarea>
            </div>
            <div class="mb-3">
              <label for="skripsiIsi" class="form-label">Isi Skripsi (gunakan baris baru untuk paragraf)</label>
              <textarea class="form-control" id="skripsiIsi" rows="12" required></textarea>
            </div>
            <div class="text-muted small">* Format tampilan akan menyesuaikan aturan skripsi: margin A4, Times New Roman 12pt, spasi 1.5, dll.</div>
          </form>
        </div>
        <div class="modal-footer">
          <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Batal</button>
          <button type="button" class="btn btn-primary" onclick="saveSkripsiItem()">Simpan</button>
        </div>
      </div>
    </div>
  </div>

  <!-- Bootstrap JS & Popper -->
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"></script>
  
  <script>
    // ----- STATE APLIKASI -----
    let currentView = 'dashboard';        // 'dashboard', 'bookmarks', 'notes', 'category', 'mk', 'skripsiList'
    let currentCategory = null;            // kategori pasal yang sedang dibuka
    let currentMK = null;                 // mata kuliah yang sedang dibuka
    let bookmarks = JSON.parse(localStorage.getItem('lawBookmarks')) || [];      // array of id (untuk pasal)
    let notes = JSON.parse(localStorage.getItem('lawNotes')) || {};              // object id -> text (untuk pasal)

    // Data pasal manual (per kategori) - menggantikan lawsData statis
    let pasalData = JSON.parse(localStorage.getItem('pasalData')) || {
      'KUH PERDATA': [],
      'KUHP LAMA': [],
      'KUHP BARU': [],
      'KUHAP BARU': []
    };

    // Data mata kuliah
    let mkData = JSON.parse(localStorage.getItem('mkData')) || {};

    // Data skripsi - baru
    let skripsiData = JSON.parse(localStorage.getItem('skripsiData')) || [];

    // Simpan perubahan ke localStorage
    function saveBookmarks() {
      localStorage.setItem('lawBookmarks', JSON.stringify(bookmarks));
    }
    function saveNotes() {
      localStorage.setItem('lawNotes', JSON.stringify(notes));
    }
    function savePasalData() {
      localStorage.setItem('pasalData', JSON.stringify(pasalData));
    }
    function saveMKData() {
      localStorage.setItem('mkData', JSON.stringify(mkData));
    }
    function saveSkripsiData() {
      localStorage.setItem('skripsiData', JSON.stringify(skripsiData));
    }

    // ----- FUNGSI UPDATE OTOMATIS (SIMULASI) -----
    function simulateUpdate() {
      alert('Update otomatis: data terintegrasi dengan sumber hukum (simulasi).');
    }

    // ----- BOOKMARK TOGGLE (untuk pasal) -----
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

    // ----- CATATAN (untuk pasal) -----
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
      // Cari pasal di semua kategori
      let law = null;
      for (const cat in pasalData) {
        const found = pasalData[cat].find(p => p.id === id);
        if (found) {
          law = found;
          break;
        }
      }
      if (!law) return;
      const bookmarked = isBookmarked(id);
      const note = notes[id] || '';
      const contentFormatted = law.content.replace(/\n/g, '<br>');
      const modalBody = document.getElementById('pasalModalBody');
      modalBody.innerHTML = `
        <h5 class="text-primary">${law.category} - ${law.number}</h5>
        <h6>${law.title}</h6>
        <p class="mt-3">${contentFormatted}</p>
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

    // ----- DASHBOARD -----
    function showDashboard() {
      currentView = 'dashboard';
      const html = `
        <div style="position: relative; height: 100%; background-image: url('https://images.unsplash.com/photo-1589829545856-d10d557cf95f?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80'); background-size: cover; background-position: center; border-radius: 0.5rem; overflow: hidden;">
          <div style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; background-color: rgba(0,0,0,0.6);"></div>
          <div style="position: relative; z-index: 2; display: flex; flex-direction: column; justify-content: center; align-items: center; height: 100%; text-align: center; color: white; padding: 2rem;">
            <h1 style="font-size: 3rem; font-weight: 700; margin-bottom: 1rem;">PRODI HUKUM</h1>
            <marquee style="width: 100%; font-size: 2rem; margin-bottom: 2rem; background: rgba(0,0,0,0.3); padding: 0.5rem;">SELAMAT DATANG DI APLIKASI PRODI HUKUM</marquee>
            <p style="font-size: 1.2rem; max-width: 600px;">Aplikasi ini menyediakan akses ke KUH Perdata, KUHP Lama, KUHP Baru, KUHAP, materi kuliah, dan koleksi skripsi mahasiswa. Gunakan menu di samping untuk mulai.</p>
            <div style="margin-top: 2rem;">
              <button class="btn btn-primary btn-lg me-2" onclick="alert('Fitur login dalam pengembangan')">Login</button>
              <button class="btn btn-outline-light btn-lg" onclick="alert('Fitur registrasi dalam pengembangan')">Registrasi</button>
            </div>
          </div>
        </div>
      `;
      document.getElementById('viewContent').innerHTML = html;
    }

    // ----- FUNGSI UNTUK MENAMPILKAN DAFTAR PASAL PER KATEGORI -----
    function renderPasalList(category) {
      const items = pasalData[category] || [];
      let html = `
        <h5 class="fw-bold mb-3"><i class="fas fa-list me-2 text-primary"></i>Kategori: ${category}</h5>
        <button class="btn btn-primary mb-3" onclick="showAddPasalItem('${category}')"><i class="fas fa-plus"></i> Tambah Pasal</button>
      `;
      if (items.length === 0) {
        html += '<p class="text-secondary">Belum ada pasal. Klik "Tambah Pasal" untuk mulai.</p>';
      } else {
        html += '<div class="list-group">';
        items.forEach((item) => {
          // Buat cuplikan pendek
          const snippet = item.content.replace(/\n/g, ' ').substring(0, 100) + '…';
          html += `
            <div class="list-group-item list-group-item-action d-flex justify-content-between align-items-center pasal-card" onclick="showPasalDetail('${item.id}')">
              <div style="flex:1;">
                <span class="badge badge-kuhp">${item.number}</span> <strong>${item.title}</strong>
                <p class="mb-0 text-secondary small">${snippet}</p>
              </div>
              <div>
                <i class="fas fa-bookmark bookmark-icon ${isBookmarked(item.id) ? 'active' : ''}" onclick="event.stopPropagation(); toggleBookmark('${item.id}')"></i>
                ${notes[item.id] ? '<i class="fas fa-sticky-note ms-1 text-info" title="Ada catatan"></i>' : ''}
                <button class="btn btn-sm btn-outline-warning ms-2" onclick="event.stopPropagation(); editPasalItem('${category}', '${item.id}')"><i class="fas fa-edit"></i></button>
                <button class="btn btn-sm btn-outline-danger" onclick="event.stopPropagation(); deletePasalItem('${category}', '${item.id}')"><i class="fas fa-trash"></i></button>
              </div>
            </div>
          `;
        });
        html += '</div>';
      }
      document.getElementById('viewContent').innerHTML = html;
    }

    // ----- FUNGSI UNTUK MATA KULIAH (sama seperti sebelumnya) -----
    function showMataKuliah(mkName) {
      currentMK = mkName;
      if (!mkData[mkName]) {
        mkData[mkName] = [];
        saveMKData();
      }
      renderMKView(mkName);
      currentView = 'mk';
    }

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

    // Modal handling untuk MK
    let currentMKForModal = null;
    let currentMKEditId = null;

    function showAddMKItem(mkName) {
      currentMKForModal = mkName;
      currentMKEditId = null;
      document.getElementById('mkTitle').value = '';
      document.getElementById('mkContent').value = '';
      document.getElementById('mkModalLabel').innerText = 'Tambah Materi';
      new bootstrap.Modal(document.getElementById('mkModal')).show();
    }

    function editMKItem(mkName, id) {
      currentMKForModal = mkName;
      currentMKEditId = id;
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

      if (currentMKEditId) {
        // edit
        const index = mkData[currentMKForModal].findIndex(i => i.id === currentMKEditId);
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
      bootstrap.Modal.getInstance(document.getElementById('mkModal')).hide();
      renderMKView(currentMKForModal);
    }

    // ----- FUNGSI UNTUK PASAL (manual) -----
    function showAddPasalItem(category) {
      document.getElementById('pasalEditId').value = '';
      document.getElementById('pasalCategory').value = category;
      document.getElementById('pasalNumber').value = '';
      document.getElementById('pasalTitle').value = '';
      document.getElementById('pasalContent').value = '';
      document.getElementById('pasalModalEditLabel').innerText = 'Tambah Pasal';
      new bootstrap.Modal(document.getElementById('pasalModalEdit')).show();
    }

    function editPasalItem(category, id) {
      const item = pasalData[category].find(i => i.id === id);
      if (!item) return;
      document.getElementById('pasalEditId').value = id;
      document.getElementById('pasalCategory').value = category;
      document.getElementById('pasalNumber').value = item.number;
      document.getElementById('pasalTitle').value = item.title;
      document.getElementById('pasalContent').value = item.content;
      document.getElementById('pasalModalEditLabel').innerText = 'Edit Pasal';
      new bootstrap.Modal(document.getElementById('pasalModalEdit')).show();
    }

    function deletePasalItem(category, id) {
      if (confirm('Hapus pasal ini?')) {
        pasalData[category] = pasalData[category].filter(i => i.id !== id);
        savePasalData();
        renderPasalList(category);
      }
    }

    function savePasalItem() {
      const category = document.getElementById('pasalCategory').value;
      const number = document.getElementById('pasalNumber').value.trim();
      const title = document.getElementById('pasalTitle').value.trim();
      const content = document.getElementById('pasalContent').value.trim();
      if (!number || !title || !content) {
        alert('Nomor, judul, dan konten harus diisi!');
        return;
      }
      const editId = document.getElementById('pasalEditId').value;
      if (editId) {
        // edit
        const index = pasalData[category].findIndex(i => i.id === editId);
        if (index !== -1) {
          pasalData[category][index].number = number;
          pasalData[category][index].title = title;
          pasalData[category][index].content = content;
        }
      } else {
        // tambah baru
        const newId = 'pasal-' + Date.now() + '-' + Math.random().toString(36).substr(2, 9);
        pasalData[category].push({ id: newId, category, number, title, content });
      }
      savePasalData();
      bootstrap.Modal.getInstance(document.getElementById('pasalModalEdit')).hide();
      renderPasalList(category);
    }

    function selectCategory(cat) {
      currentCategory = cat;
      renderPasalList(cat);
      document.getElementById('searchInput').value = '';
      currentView = 'category';
    }

    // ----- PENCARIAN (di semua pasal) -----
    function searchPasal() {
      const query = document.getElementById('searchInput').value.toLowerCase().trim();
      if (!query) {
        // jika query kosong, kembali ke dashboard
        showDashboard();
        return;
      }
      // Kumpulkan semua pasal dari semua kategori
      const allPasal = [];
      for (const cat in pasalData) {
        allPasal.push(...pasalData[cat]);
      }
      const results = allPasal.filter(item => 
        item.content.toLowerCase().includes(query) || 
        item.title.toLowerCase().includes(query) || 
        item.number.toLowerCase().includes(query) ||
        item.category.toLowerCase().includes(query)
      );
      // Tampilkan hasil pencarian
      let html = `<h5 class="fw-bold mb-3"><i class="fas fa-search me-2 text-primary"></i>Hasil pencarian: "${query}"</h5>`;
      if (results.length === 0) {
        html += '<p class="text-secondary">Tidak ditemukan pasal yang cocok.</p>';
      } else {
        html += '<div class="list-group">';
        results.forEach(law => {
          const snippet = law.content.replace(/\n/g, ' ').substring(0, 100) + '…';
          html += `
            <div class="list-group-item list-group-item-action d-flex justify-content-between align-items-center law-card" onclick="showPasalDetail('${law.id}')">
              <div>
                <span class="badge badge-kuhp">${law.category}</span> <strong>${law.number}</strong> - ${law.title}
                <p class="mb-0 text-secondary small">${snippet}</p>
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
      currentView = 'search';
    }

    // ----- VIEW BOOKMARK & CATATAN (untuk pasal) -----
    function renderBookmarksView() {
      // Kumpulkan semua pasal
      const allPasal = [];
      for (const cat in pasalData) {
        allPasal.push(...pasalData[cat]);
      }
      const bookmarkedLaws = allPasal.filter(l => bookmarks.includes(l.id));
      let html = '<h5 class="fw-bold mb-3"><i class="fas fa-bookmark me-2 text-warning"></i>Bookmark Saya</h5>';
      if (bookmarkedLaws.length === 0) {
        html += '<p class="text-secondary">Belum ada pasal yang di-bookmark.</p>';
      } else {
        html += '<div class="list-group">';
        bookmarkedLaws.forEach(law => {
          const snippet = law.content.replace(/\n/g, ' ').substring(0, 100) + '…';
          html += `
            <div class="list-group-item list-group-item-action d-flex justify-content-between align-items-center law-card" onclick="showPasalDetail('${law.id}')">
              <div>
                <span class="badge badge-kuhp">${law.category}</span> <strong>${law.number}</strong> - ${law.title}
                <p class="mb-0 text-secondary small">${snippet}</p>
              </div>
              <div>
                <i class="fas fa-bookmark bookmark-icon active" onclick="event.stopPropagation(); toggleBookmark('${law.id}')"></i>
                ${notes[law.id] ? '<i class="fas fa-sticky-note ms-1 text-info" title="Ada catatan"></i>' : ''}
              </div>
            </div>
          `;
        });
        html += '</div>';
      }
      document.getElementById('viewContent').innerHTML = html;
      currentView = 'bookmarks';
    }

    function renderNotesView() {
      const notedIds = Object.keys(notes);
      // Kumpulkan semua pasal
      const allPasal = [];
      for (const cat in pasalData) {
        allPasal.push(...pasalData[cat]);
      }
      const notedLaws = allPasal.filter(l => notedIds.includes(l.id));
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
              <strong>${law.number}</strong> - ${law.title}
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

    // ----- FUNGSI UNTUK SKRIPSI -----
    function showSkripsiList() {
      currentView = 'skripsiList';
      renderSkripsiList();
    }

    function renderSkripsiList() {
      let html = `
        <h5 class="fw-bold mb-3"><i class="fas fa-file-alt me-2 text-info"></i>Daftar Skripsi</h5>
        <button class="btn btn-primary mb-3" onclick="showAddSkripsi()"><i class="fas fa-plus"></i> Tulis Skripsi Baru</button>
      `;
      if (skripsiData.length === 0) {
        html += '<p class="text-secondary">Belum ada skripsi. Klik "Tulis Skripsi Baru" untuk mulai.</p>';
      } else {
        html += '<div class="list-group">';
        skripsiData.forEach((item) => {
          html += `
            <div class="list-group-item list-group-item-action skripsi-card" onclick="showSkripsiDetail('${item.id}')">
              <div class="d-flex justify-content-between align-items-start">
                <div style="flex:1;">
                  <h6 class="fw-bold">${item.judul}</h6>
                  <div class="skripsi-meta">Penulis: ${item.penulis}</div>
                  <div class="skripsi-content small">${item.abstrak.substring(0, 150)}…</div>
                </div>
                <div class="skripsi-actions">
                  <button class="btn btn-sm btn-outline-warning" onclick="event.stopPropagation(); editSkripsi('${item.id}')"><i class="fas fa-edit"></i></button>
                  <button class="btn btn-sm btn-outline-danger" onclick="event.stopPropagation(); deleteSkripsi('${item.id}')"><i class="fas fa-trash"></i></button>
                </div>
              </div>
            </div>
          `;
        });
        html += '</div>';
      }
      document.getElementById('viewContent').innerHTML = html;
    }

    function showAddSkripsi() {
      document.getElementById('skripsiEditId').value = '';
      document.getElementById('skripsiJudul').value = '';
      document.getElementById('skripsiPenulis').value = '';
      document.getElementById('skripsiAbstrak').value = '';
      document.getElementById('skripsiIsi').value = '';
      document.getElementById('skripsiModalLabel').innerText = 'Tulis Skripsi Baru';
      new bootstrap.Modal(document.getElementById('skripsiModal')).show();
    }

    function editSkripsi(id) {
      const item = skripsiData.find(s => s.id === id);
      if (!item) return;
      document.getElementById('skripsiEditId').value = id;
      document.getElementById('skripsiJudul').value = item.judul;
      document.getElementById('skripsiPenulis').value = item.penulis;
      document.getElementById('skripsiAbstrak').value = item.abstrak;
      document.getElementById('skripsiIsi').value = item.isi;
      document.getElementById('skripsiModalLabel').innerText = 'Edit Skripsi';
      new bootstrap.Modal(document.getElementById('skripsiModal')).show();
    }

    function deleteSkripsi(id) {
      if (confirm('Hapus skripsi ini?')) {
        skripsiData = skripsiData.filter(s => s.id !== id);
        saveSkripsiData();
        renderSkripsiList();
      }
    }

    function saveSkripsiItem() {
      const judul = document.getElementById('skripsiJudul').value.trim();
      const penulis = document.getElementById('skripsiPenulis').value.trim();
      const abstrak = document.getElementById('skripsiAbstrak').value.trim();
      const isi = document.getElementById('skripsiIsi').value.trim();
      if (!judul || !penulis || !abstrak || !isi) {
        alert('Semua field harus diisi!');
        return;
      }
      const editId = document.getElementById('skripsiEditId').value;
      if (editId) {
        // edit
        const index = skripsiData.findIndex(s => s.id === editId);
        if (index !== -1) {
          skripsiData[index].judul = judul;
          skripsiData[index].penulis = penulis;
          skripsiData[index].abstrak = abstrak;
          skripsiData[index].isi = isi;
        }
      } else {
        // tambah baru
        const newId = 'skripsi-' + Date.now() + '-' + Math.random().toString(36).substr(2, 9);
        skripsiData.push({ id: newId, judul, penulis, abstrak, isi });
      }
      saveSkripsiData();
      bootstrap.Modal.getInstance(document.getElementById('skripsiModal')).hide();
      renderSkripsiList();
    }

    function showSkripsiDetail(id) {
      const item = skripsiData.find(s => s.id === id);
      if (!item) return;
      // Format isi dengan paragraf
      const isiFormatted = item.isi.split('\n').filter(p => p.trim() !== '').map(p => `<p>${p}</p>`).join('');
      const modalBody = document.getElementById('pasalModalBody');
      modalBody.innerHTML = `
        <div class="skripsi-dokumen" style="background: white; color: black; padding: 2cm; margin: 0; font-family: 'Times New Roman', serif; font-size: 12pt; line-height: 1.5; text-align: justify;">
          <h4 class="judul" style="text-align: center; font-size: 14pt; font-weight: bold;">${item.judul}</h4>
          <p class="penulis" style="text-align: center;">${item.penulis}</p>
          <div class="abstrak">
            <h6 style="font-weight: bold;">Abstrak</h6>
            <p>${item.abstrak}</p>
          </div>
          <div class="konten">
            ${isiFormatted}
          </div>
        </div>
      `;
      new bootstrap.Modal(document.getElementById('pasalModal')).show();
    }

    // ----- REFRESH TAMPILAN SAAT INI -----
    function refreshCurrentView() {
      if (currentView === 'dashboard') showDashboard();
      else if (currentView === 'bookmarks') renderBookmarksView();
      else if (currentView === 'notes') renderNotesView();
      else if (currentView === 'category' && currentCategory) {
        renderPasalList(currentCategory);
      } else if (currentView === 'search') {
        const query = document.getElementById('searchInput').value.trim();
        if (query) searchPasal(); else showDashboard();
      } else if (currentView === 'mk' && currentMK) {
        renderMKView(currentMK);
      } else if (currentView === 'skripsiList') {
        renderSkripsiList();
      } else {
        showDashboard();
      }
    }

    // Inisialisasi awal
    window.onload = function() {
      showDashboard();
    };
  </script>

  <!-- footer small -->
  <footer class="text-center footer-note mt-3">
    <span>Terintegrasi dengan sumber hukum Indonesia (simulasi update otomatis). Data ditulis manual oleh pengguna.</span>
  </footer>
</body>
</html>
