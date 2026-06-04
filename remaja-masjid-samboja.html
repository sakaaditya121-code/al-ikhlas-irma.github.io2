import { useState, useEffect, useCallback } from "react";

// ─── MOCK DATA ───────────────────────────────────────────────────────────────
const MOCK_USERS = [
  { id: 1, username: "admin", password: "admin123", role: "admin", name: "Ust. Ahmad Fauzi", email: "admin@remajamasjid.id", phone: "081234567890", jabatan: "Pembina Utama", avatar: "AF" },
  { id: 2, username: "pembina1", password: "pass123", role: "pembina", name: "Ibu Siti Rahayu", email: "siti@remajamasjid.id", phone: "081298765432", jabatan: "Pembina Putri", avatar: "SR" },
  { id: 3, username: "anggota1", password: "pass123", role: "anggota", name: "Muhammad Rizki", email: "rizki@email.com", phone: "085612345678", jabatan: "Anggota", avatar: "MR", divisi: "Dakwah", angkatan: "2022" },
  { id: 4, username: "anggota2", password: "pass123", role: "anggota", name: "Fatimah Azzahra", email: "fatimah@email.com", phone: "087712345678", jabatan: "Anggota", avatar: "FA", divisi: "Sosial", angkatan: "2023" },
];

const INIT_ANGGOTA = [
  { id: 1, nama: "Muhammad Rizki", nik: "3271010101020001", ttl: "Jakarta, 01-01-2002", alamat: "Jl. Mawar No. 1, Jakarta", telepon: "085612345678", email: "rizki@email.com", divisi: "Dakwah", angkatan: "2022", status: "Aktif", avatar: "MR", gender: "L", userId: 3 },
  { id: 2, nama: "Fatimah Azzahra", nik: "3271015505030002", ttl: "Jakarta, 15-05-2003", alamat: "Jl. Melati No. 5, Jakarta", telepon: "087712345678", email: "fatimah@email.com", divisi: "Sosial", angkatan: "2023", status: "Aktif", avatar: "FA", gender: "P", userId: 4 },
  { id: 3, nama: "Abdullah Hasan", nik: "3271012202010003", ttl: "Depok, 22-02-2001", alamat: "Jl. Anggrek No. 3, Depok", telepon: "089912345678", email: "abdullah@email.com", divisi: "Olahraga", angkatan: "2021", status: "Aktif", avatar: "AH", gender: "L", userId: null },
  { id: 4, nama: "Khadijah Nur", nik: "3271011010040004", ttl: "Bogor, 10-10-2004", alamat: "Jl. Cempaka No. 7, Bogor", telepon: "082212345678", email: "khadijah@email.com", divisi: "Dakwah", angkatan: "2023", status: "Aktif", avatar: "KN", gender: "P", userId: null },
  { id: 5, nama: "Umar Faruk", nik: "3271010303000005", ttl: "Jakarta, 03-03-2000", alamat: "Jl. Flamboyan No. 9, Jakarta", telepon: "083312345678", email: "umar@email.com", divisi: "Seni", angkatan: "2020", status: "Alumni", avatar: "UF", gender: "L", userId: null },
];

const INIT_KEGIATAN = [
  { id: 1, nama: "Kajian Tafsir Al-Quran", tanggal: "2025-07-10", waktu: "19:30", lokasi: "Masjid Al-Ikhlas Lt. 2", deskripsi: "Kajian rutin mingguan membahas tafsir juz 30", kategori: "Kajian", status: "Akan Datang", pembina: "Ust. Ahmad Fauzi" },
  { id: 2, nama: "Bakti Sosial Ramadhan", tanggal: "2025-03-15", waktu: "08:00", lokasi: "Kelurahan Cempaka", deskripsi: "Pembagian sembako kepada warga kurang mampu", kategori: "Sosial", status: "Selesai", pembina: "Ibu Siti Rahayu" },
  { id: 3, nama: "Rapat Pengurus Bulanan", tanggal: "2025-07-01", waktu: "16:00", lokasi: "Sekretariat REMAS", deskripsi: "Evaluasi kegiatan bulan lalu & perencanaan", kategori: "Rapat", status: "Selesai", pembina: "Ust. Ahmad Fauzi" },
  { id: 4, nama: "Lomba Seni Islami", tanggal: "2025-08-17", waktu: "09:00", lokasi: "Aula Masjid", deskripsi: "Lomba kaligrafi, nasyid, dan busana muslim", kategori: "Seni", status: "Akan Datang", pembina: "Ibu Siti Rahayu" },
  { id: 5, nama: "Pesantren Kilat", tanggal: "2025-06-20", waktu: "07:00", lokasi: "Masjid Al-Ikhlas", deskripsi: "Kegiatan intensif belajar agama selama 3 hari", kategori: "Kajian", status: "Selesai", pembina: "Ust. Ahmad Fauzi" },
];

const INIT_ABSENSI = [
  { id: 1, kegiatanId: 2, anggotaId: 1, status: "Hadir", waktuAbsen: "08:05", keterangan: "" },
  { id: 2, kegiatanId: 2, anggotaId: 2, status: "Hadir", waktuAbsen: "08:10", keterangan: "" },
  { id: 3, kegiatanId: 2, anggotaId: 3, status: "Izin", waktuAbsen: "-", keterangan: "Sakit" },
  { id: 4, kegiatanId: 2, anggotaId: 4, status: "Hadir", waktuAbsen: "08:00", keterangan: "" },
  { id: 5, kegiatanId: 3, anggotaId: 1, status: "Hadir", waktuAbsen: "16:05", keterangan: "" },
  { id: 6, kegiatanId: 3, anggotaId: 3, status: "Hadir", waktuAbsen: "16:00", keterangan: "" },
  { id: 7, kegiatanId: 5, anggotaId: 1, status: "Hadir", waktuAbsen: "07:10", keterangan: "" },
  { id: 8, kegiatanId: 5, anggotaId: 2, status: "Hadir", waktuAbsen: "07:15", keterangan: "" },
  { id: 9, kegiatanId: 5, anggotaId: 4, status: "Alpha", waktuAbsen: "-", keterangan: "" },
];

const INIT_PRESTASI = [
  { id: 1, anggotaId: 1, nama: "Juara 1 MTQ Tingkat Kecamatan", tanggal: "2024-08-20", kategori: "Keagamaan", tingkat: "Kecamatan", keterangan: "Cabang Tilawah Putra" },
  { id: 2, anggotaId: 2, nama: "Juara 2 Kaligrafi Islami", tanggal: "2024-10-05", kategori: "Seni", tingkat: "Kota", keterangan: "Kategori Naskah" },
  { id: 3, anggotaId: 3, nama: "Peserta Terbaik Diklat Kepemimpinan", tanggal: "2025-01-15", kategori: "Kepemimpinan", tingkat: "Provinsi", keterangan: "FORMAS Jakarta" },
  { id: 4, anggotaId: 1, nama: "Hafiz Quran 10 Juz", tanggal: "2025-03-10", kategori: "Keagamaan", tingkat: "Nasional", keterangan: "Bimbingan Ust. Ahmad" },
];

const DIVISI_LIST = ["Dakwah", "Sosial", "Olahraga", "Seni", "Pendidikan", "Humas"];
const KATEGORI_KEGIATAN = ["Kajian", "Sosial", "Rapat", "Seni", "Olahraga", "Lainnya"];

// ─── STYLES ──────────────────────────────────────────────────────────────────
const css = `
  @import url('https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&family=Amiri:wght@400;700&display=swap');
  
  *{box-sizing:border-box;margin:0;padding:0;}
  body{font-family:'Plus Jakarta Sans',sans-serif;background:#f8f7ff;}
  
  :root{
    --purple-50:#f3f0ff;--purple-100:#ede8ff;--purple-200:#d4ccff;
    --purple-300:#b8aaff;--purple-400:#9d87ff;--purple-500:#7c5cbf;
    --purple-600:#6741d9;--purple-700:#5a35b8;--purple-800:#4c2d9c;
    --purple-900:#3b2080;
    --grad:linear-gradient(135deg,#7c5cbf 0%,#9d87ff 50%,#b8aaff 100%);
    --grad2:linear-gradient(135deg,#6741d9 0%,#9d87ff 100%);
    --shadow-sm:0 1px 3px rgba(100,65,200,.08);
    --shadow-md:0 4px 16px rgba(100,65,200,.12);
    --shadow-lg:0 8px 32px rgba(100,65,200,.18);
  }

  .app-wrap{display:flex;height:100vh;overflow:hidden;}
  
  /* Sidebar */
  .sidebar{width:256px;background:var(--grad);display:flex;flex-direction:column;flex-shrink:0;overflow-y:auto;}
  .sidebar-logo{padding:28px 20px 20px;border-bottom:1px solid rgba(255,255,255,.15);}
  .sidebar-logo-icon{width:44px;height:44px;background:rgba(255,255,255,.2);border-radius:12px;display:flex;align-items:center;justify-content:center;font-family:'Amiri',serif;font-size:22px;color:#fff;margin-bottom:10px;}
  .sidebar-logo h1{font-size:13px;font-weight:700;color:#fff;line-height:1.3;}
  .sidebar-logo p{font-size:11px;color:rgba(255,255,255,.7);margin-top:2px;}
  .sidebar-nav{padding:16px 12px;flex:1;}
  .sidebar-section{font-size:10px;font-weight:600;color:rgba(255,255,255,.5);letter-spacing:.08em;text-transform:uppercase;padding:8px 8px 4px;}
  .nav-item{display:flex;align-items:center;gap:10px;padding:10px 12px;border-radius:10px;cursor:pointer;transition:all .2s;color:rgba(255,255,255,.8);font-size:13.5px;font-weight:500;margin-bottom:2px;}
  .nav-item:hover{background:rgba(255,255,255,.15);color:#fff;}
  .nav-item.active{background:rgba(255,255,255,.25);color:#fff;font-weight:600;}
  .nav-item svg{width:18px;height:18px;flex-shrink:0;}
  .sidebar-footer{padding:16px;border-top:1px solid rgba(255,255,255,.15);}
  .user-card{display:flex;align-items:center;gap:10px;padding:10px;background:rgba(255,255,255,.12);border-radius:10px;}
  .avatar{width:36px;height:36px;border-radius:50%;background:rgba(255,255,255,.3);display:flex;align-items:center;justify-content:center;font-size:12px;font-weight:700;color:#fff;flex-shrink:0;}
  .avatar.lg{width:52px;height:52px;font-size:16px;}
  .avatar.xl{width:64px;height:64px;font-size:20px;}
  .user-card-info{flex:1;min-width:0;}
  .user-card-info .name{font-size:12.5px;font-weight:600;color:#fff;white-space:nowrap;overflow:hidden;text-overflow:ellipsis;}
  .user-card-info .role{font-size:11px;color:rgba(255,255,255,.65);}

  /* Main */
  .main{flex:1;display:flex;flex-direction:column;overflow:hidden;}
  .topbar{height:60px;background:#fff;border-bottom:1px solid #ede8ff;display:flex;align-items:center;padding:0 24px;gap:16px;flex-shrink:0;box-shadow:var(--shadow-sm);}
  .topbar h2{font-size:18px;font-weight:700;color:#3b2080;flex:1;}
  .content{flex:1;overflow-y:auto;padding:24px;background:#f8f7ff;}

  /* Cards */
  .card{background:#fff;border-radius:16px;box-shadow:var(--shadow-sm);border:1px solid #ede8ff;}
  .card-header{padding:18px 20px;border-bottom:1px solid #f3f0ff;display:flex;align-items:center;justify-content:space-between;}
  .card-header h3{font-size:15px;font-weight:700;color:#3b2080;}
  .card-body{padding:20px;}

  /* Stat cards */
  .stats-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));gap:16px;margin-bottom:24px;}
  .stat-card{background:#fff;border-radius:16px;padding:20px;border:1px solid #ede8ff;box-shadow:var(--shadow-sm);display:flex;align-items:flex-start;gap:14px;}
  .stat-icon{width:48px;height:48px;border-radius:12px;display:flex;align-items:center;justify-content:center;flex-shrink:0;}
  .stat-icon.purple{background:#ede8ff;}
  .stat-icon.green{background:#e6f9f0;}
  .stat-icon.orange{background:#fff3e0;}
  .stat-icon.blue{background:#e3f0ff;}
  .stat-val{font-size:28px;font-weight:800;color:#3b2080;line-height:1;}
  .stat-label{font-size:12px;color:#888;margin-top:4px;}
  .stat-sub{font-size:11.5px;color:#7c5cbf;margin-top:6px;font-weight:500;}

  /* Table */
  .table-wrap{overflow-x:auto;}
  table{width:100%;border-collapse:collapse;font-size:13.5px;}
  th{background:#f8f7ff;font-size:11.5px;font-weight:600;color:#7c5cbf;text-transform:uppercase;letter-spacing:.05em;padding:10px 14px;text-align:left;border-bottom:1px solid #ede8ff;}
  td{padding:12px 14px;border-bottom:1px solid #f8f7ff;color:#333;vertical-align:middle;}
  tr:last-child td{border-bottom:none;}
  tr:hover td{background:#faf9ff;}

  /* Badge */
  .badge{display:inline-flex;align-items:center;padding:3px 10px;border-radius:20px;font-size:11.5px;font-weight:600;}
  .badge.active,.badge.hadir{background:#e6f9f0;color:#15803d;}
  .badge.alumni{background:#f3f0ff;color:#6741d9;}
  .badge.izin{background:#fff8e1;color:#b45309;}
  .badge.alpha{background:#fef2f2;color:#dc2626;}
  .badge.selesai{background:#e6f9f0;color:#15803d;}
  .badge.akan-datang{background:#ede8ff;color:#6741d9;}
  .badge.kajian{background:#ede8ff;color:#6741d9;}
  .badge.sosial{background:#e6f9f0;color:#15803d;}
  .badge.rapat{background:#fff8e1;color:#b45309;}
  .badge.seni{background:#fce7f3;color:#9d174d;}
  .badge.olahraga{background:#e0f2fe;color:#0369a1;}
  .badge.lainnya{background:#f3f4f6;color:#4b5563;}
  .badge.nasional{background:#fef3c7;color:#92400e;}
  .badge.provinsi{background:#ede9fe;color:#5b21b6;}
  .badge.kota{background:#dbeafe;color:#1e40af;}
  .badge.kecamatan{background:#d1fae5;color:#065f46;}

  /* Buttons */
  .btn{display:inline-flex;align-items:center;gap:6px;padding:8px 16px;border-radius:9px;font-size:13px;font-weight:600;cursor:pointer;border:none;transition:all .18s;}
  .btn-primary{background:var(--grad2);color:#fff;box-shadow:0 2px 8px rgba(103,65,217,.3);}
  .btn-primary:hover{opacity:.9;transform:translateY(-1px);}
  .btn-outline{background:#fff;color:#6741d9;border:1.5px solid #d4ccff;}
  .btn-outline:hover{background:#f3f0ff;}
  .btn-danger{background:#fef2f2;color:#dc2626;border:1px solid #fecaca;}
  .btn-danger:hover{background:#fee2e2;}
  .btn-sm{padding:5px 11px;font-size:12px;}
  .btn-icon{padding:7px;border-radius:8px;}

  /* Form */
  .form-group{margin-bottom:16px;}
  .form-group label{display:block;font-size:12.5px;font-weight:600;color:#4c2d9c;margin-bottom:6px;}
  .form-control{width:100%;padding:9px 13px;border:1.5px solid #d4ccff;border-radius:9px;font-size:13.5px;color:#333;outline:none;transition:border .18s;background:#fff;font-family:inherit;}
  .form-control:focus{border-color:#7c5cbf;box-shadow:0 0 0 3px rgba(124,92,191,.12);}
  select.form-control{cursor:pointer;}
  .form-row{display:grid;grid-template-columns:1fr 1fr;gap:14px;}

  /* Modal */
  .modal-overlay{position:fixed;inset:0;background:rgba(60,30,130,.35);z-index:1000;display:flex;align-items:center;justify-content:center;padding:20px;}
  .modal{background:#fff;border-radius:20px;width:100%;max-width:540px;box-shadow:var(--shadow-lg);max-height:90vh;overflow-y:auto;}
  .modal-header{padding:20px 24px;border-bottom:1px solid #f3f0ff;display:flex;align-items:center;justify-content:space-between;}
  .modal-header h3{font-size:16px;font-weight:700;color:#3b2080;}
  .modal-body{padding:20px 24px;}
  .modal-footer{padding:16px 24px;border-top:1px solid #f3f0ff;display:flex;justify-content:flex-end;gap:10px;}

  /* Login */
  .login-page{min-height:100vh;background:var(--grad);display:flex;align-items:center;justify-content:center;padding:20px;}
  .login-card{background:#fff;border-radius:24px;padding:40px;width:100%;max-width:420px;box-shadow:var(--shadow-lg);}
  .login-logo{text-align:center;margin-bottom:28px;}
  .login-logo .icon{width:72px;height:72px;background:var(--grad);border-radius:20px;display:flex;align-items:center;justify-content:center;font-family:'Amiri',serif;font-size:36px;color:#fff;margin:0 auto 12px;}
  .login-logo h1{font-size:22px;font-weight:800;color:#3b2080;}
  .login-logo p{font-size:13px;color:#888;margin-top:4px;}

  /* Search */
  .search-wrap{position:relative;}
  .search-wrap svg{position:absolute;left:11px;top:50%;transform:translateY(-50%);color:#9d87ff;}
  .search-input{width:100%;padding:8px 12px 8px 36px;border:1.5px solid #d4ccff;border-radius:9px;font-size:13px;outline:none;background:#f8f7ff;font-family:inherit;}
  .search-input:focus{border-color:#7c5cbf;background:#fff;}

  /* Notification */
  .notif-dot{width:8px;height:8px;background:#ef4444;border-radius:50%;position:absolute;top:6px;right:6px;}
  .notif-panel{position:absolute;right:0;top:44px;width:320px;background:#fff;border-radius:14px;box-shadow:var(--shadow-lg);border:1px solid #ede8ff;z-index:100;overflow:hidden;}
  .notif-item{padding:14px 16px;border-bottom:1px solid #f8f7ff;cursor:pointer;}
  .notif-item:hover{background:#faf9ff;}
  .notif-item:last-child{border-bottom:none;}
  .notif-item .notif-title{font-size:13px;font-weight:600;color:#3b2080;}
  .notif-item .notif-msg{font-size:12px;color:#666;margin-top:2px;}
  .notif-item .notif-time{font-size:11px;color:#9d87ff;margin-top:4px;}
  .notif-item.unread{background:#faf8ff;}

  /* Progress bar */
  .progress-bar{height:8px;background:#ede8ff;border-radius:99px;overflow:hidden;}
  .progress-fill{height:100%;background:var(--grad2);border-radius:99px;transition:width .5s ease;}

  /* Absensi grid */
  .absensi-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(200px,1fr));gap:12px;}
  .absensi-card{background:#fff;border:1.5px solid #ede8ff;border-radius:12px;padding:14px;display:flex;align-items:center;gap:12px;}
  .absensi-card.hadir{border-color:#86efac;}
  .absensi-card.izin{border-color:#fcd34d;}
  .absensi-card.alpha{border-color:#fca5a5;}
  .absensi-name{font-size:13px;font-weight:600;color:#3b2080;flex:1;}
  .absensi-status{display:flex;gap:4px;}
  .status-btn{padding:4px 8px;border-radius:6px;font-size:11px;font-weight:600;border:none;cursor:pointer;transition:all .15s;}
  .status-btn.h{background:#dcfce7;color:#16a34a;}.status-btn.h:hover,.status-btn.h.active{background:#16a34a;color:#fff;}
  .status-btn.i{background:#fef9c3;color:#ca8a04;}.status-btn.i:hover,.status-btn.i.active{background:#ca8a04;color:#fff;}
  .status-btn.a{background:#fee2e2;color:#dc2626;}.status-btn.a:hover,.status-btn.a.active{background:#dc2626;color:#fff;}

  /* Dashboard charts */
  .chart-bar-wrap{display:flex;flex-direction:column;gap:10px;}
  .chart-bar-row{display:flex;align-items:center;gap:10px;}
  .chart-bar-label{font-size:12px;color:#666;width:80px;flex-shrink:0;text-align:right;}
  .chart-bar-outer{flex:1;height:10px;background:#f3f0ff;border-radius:99px;overflow:hidden;}
  .chart-bar-inner{height:100%;background:var(--grad2);border-radius:99px;}
  .chart-bar-val{font-size:12px;font-weight:600;color:#6741d9;width:30px;text-align:right;}

  /* Divisi colors */
  .divisi-dakwah{background:#ede8ff;color:#6741d9;}
  .divisi-sosial{background:#e6f9f0;color:#15803d;}
  .divisi-olahraga{background:#e0f2fe;color:#0369a1;}
  .divisi-seni{background:#fce7f3;color:#9d174d;}
  .divisi-pendidikan{background:#fff8e1;color:#b45309;}
  .divisi-humas{background:#f3f4f6;color:#4b5563;}

  .tooltip-wrap{position:relative;}
  .empty-state{text-align:center;padding:48px 20px;color:#aaa;}
  .empty-state svg{width:48px;height:48px;margin:0 auto 12px;opacity:.4;}
  .empty-state p{font-size:14px;}

  .tag-role-admin{background:#fce7f3;color:#9d174d;border-radius:6px;padding:2px 8px;font-size:11px;font-weight:600;}
  .tag-role-pembina{background:#ede8ff;color:#6741d9;border-radius:6px;padding:2px 8px;font-size:11px;font-weight:600;}
  .tag-role-anggota{background:#e6f9f0;color:#15803d;border-radius:6px;padding:2px 8px;font-size:11px;font-weight:600;}

  .alert{padding:10px 14px;border-radius:9px;font-size:13px;margin-bottom:12px;display:flex;align-items:center;gap:8px;}
  .alert-success{background:#e6f9f0;color:#15803d;border:1px solid #86efac;}
  .alert-error{background:#fef2f2;color:#dc2626;border:1px solid #fca5a5;}
  .alert-info{background:#ede8ff;color:#6741d9;border:1px solid #b8aaff;}

  .back-btn{display:inline-flex;align-items:center;gap:6px;font-size:13px;color:#6741d9;cursor:pointer;font-weight:600;margin-bottom:16px;}
  .back-btn:hover{color:#4c2d9c;}

  @media(max-width:768px){
    .sidebar{width:200px;}
    .form-row{grid-template-columns:1fr;}
    .stats-grid{grid-template-columns:1fr 1fr;}
  }
  @media(max-width:600px){
    .sidebar{display:none;}
    .stats-grid{grid-template-columns:1fr;}
  }
`;

// ─── SVG ICONS ───────────────────────────────────────────────────────────────
const Icon = {
  dashboard: <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2"><rect x="3" y="3" width="7" height="7" rx="1"/><rect x="14" y="3" width="7" height="7" rx="1"/><rect x="14" y="14" width="7" height="7" rx="1"/><rect x="3" y="14" width="7" height="7" rx="1"/></svg>,
  users: <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2"><path d="M17 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2"/><circle cx="9" cy="7" r="4"/><path d="M23 21v-2a4 4 0 0 0-3-3.87"/><path d="M16 3.13a4 4 0 0 1 0 7.75"/></svg>,
  calendar: <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2"><rect x="3" y="4" width="18" height="18" rx="2"/><line x1="16" y1="2" x2="16" y2="6"/><line x1="8" y1="2" x2="8" y2="6"/><line x1="3" y1="10" x2="21" y2="10"/></svg>,
  check: <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2"><polyline points="20 6 9 17 4 12"/></svg>,
  star: <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2"><polygon points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"/></svg>,
  bell: <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2"><path d="M18 8A6 6 0 0 0 6 8c0 7-3 9-3 9h18s-3-2-3-9"/><path d="M13.73 21a2 2 0 0 1-3.46 0"/></svg>,
  search: <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2"><circle cx="11" cy="11" r="8"/><line x1="21" y1="21" x2="16.65" y2="16.65"/></svg>,
  plus: <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2.5"><line x1="12" y1="5" x2="12" y2="19"/><line x1="5" y1="12" x2="19" y2="12"/></svg>,
  edit: <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2"><path d="M11 4H4a2 2 0 0 0-2 2v14a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2v-7"/><path d="M18.5 2.5a2.121 2.121 0 0 1 3 3L12 15l-4 1 1-4 9.5-9.5z"/></svg>,
  trash: <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2"><polyline points="3 6 5 6 21 6"/><path d="M19 6v14a2 2 0 0 1-2 2H7a2 2 0 0 1-2-2V6m3 0V4a1 1 0 0 1 1-1h4a1 1 0 0 1 1 1v2"/></svg>,
  eye: <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2"><path d="M1 12s4-8 11-8 11 8 11 8-4 8-11 8-11-8-11-8z"/><circle cx="12" cy="12" r="3"/></svg>,
  x: <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2"><line x1="18" y1="6" x2="6" y2="18"/><line x1="6" y1="6" x2="18" y2="18"/></svg>,
  logout: <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2"><path d="M9 21H5a2 2 0 0 1-2-2V5a2 2 0 0 1 2-2h4"/><polyline points="16 17 21 12 16 7"/><line x1="21" y1="12" x2="9" y2="12"/></svg>,
  download: <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2"><path d="M21 15v4a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-4"/><polyline points="7 10 12 15 17 10"/><line x1="12" y1="15" x2="12" y2="3"/></svg>,
  back: <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2"><line x1="19" y1="12" x2="5" y2="12"/><polyline points="12 19 5 12 12 5"/></svg>,
  report: <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2"><path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"/><polyline points="14 2 14 8 20 8"/><line x1="16" y1="13" x2="8" y2="13"/><line x1="16" y1="17" x2="8" y2="17"/><polyline points="10 9 9 9 8 9"/></svg>,
  settings: <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2"><circle cx="12" cy="12" r="3"/><path d="M19.4 15a1.65 1.65 0 0 0 .33 1.82l.06.06a2 2 0 0 1-2.83 2.83l-.06-.06a1.65 1.65 0 0 0-1.82-.33 1.65 1.65 0 0 0-1 1.51V21a2 2 0 0 1-4 0v-.09A1.65 1.65 0 0 0 9 19.4a1.65 1.65 0 0 0-1.82.33l-.06.06a2 2 0 0 1-2.83-2.83l.06-.06A1.65 1.65 0 0 0 4.68 15a1.65 1.65 0 0 0-1.51-1H3a2 2 0 0 1 0-4h.09A1.65 1.65 0 0 0 4.6 9a1.65 1.65 0 0 0-.33-1.82l-.06-.06a2 2 0 0 1 2.83-2.83l.06.06A1.65 1.65 0 0 0 9 4.68a1.65 1.65 0 0 0 1-1.51V3a2 2 0 0 1 4 0v.09a1.65 1.65 0 0 0 1 1.51 1.65 1.65 0 0 0 1.82-.33l.06-.06a2 2 0 0 1 2.83 2.83l-.06.06A1.65 1.65 0 0 0 19.4 9a1.65 1.65 0 0 0 1.51 1H21a2 2 0 0 1 0 4h-.09a1.65 1.65 0 0 0-1.51 1z"/></svg>,
  map: <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2"><path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0 1 18 0z"/><circle cx="12" cy="10" r="3"/></svg>,
  clock: <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2"><circle cx="12" cy="12" r="10"/><polyline points="12 6 12 12 16 14"/></svg>,
  shield: <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2"><path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"/></svg>,
};

// ─── HELPERS ─────────────────────────────────────────────────────────────────
function getBadgeClass(val) {
  const map = { Aktif:"active", Alumni:"alumni", Hadir:"hadir", Izin:"izin", Alpha:"alpha", Selesai:"selesai", "Akan Datang":"akan-datang", Kajian:"kajian", Sosial:"sosial", Rapat:"rapat", Seni:"seni", Olahraga:"olahraga", Lainnya:"lainnya", Nasional:"nasional", Provinsi:"provinsi", Kota:"kota", Kecamatan:"kecamatan" };
  return map[val] || "";
}
function getDivisiClass(d) {
  return `divisi-${d?.toLowerCase()}`;
}
function formatDate(d) {
  if (!d) return "-";
  const [y, m, dd] = d.split("-");
  const months = ["Jan","Feb","Mar","Apr","Mei","Jun","Jul","Agu","Sep","Okt","Nov","Des"];
  return `${dd} ${months[parseInt(m)-1]} ${y}`;
}
function toast(setToasts, msg, type = "success") {
  const id = Date.now();
  setToasts(t => [...t, { id, msg, type }]);
  setTimeout(() => setToasts(t => t.filter(x => x.id !== id)), 3000);
}

// ─── TOAST ───────────────────────────────────────────────────────────────────
function Toasts({ toasts }) {
  return (
    <div style={{ position:"fixed", bottom:24, right:24, zIndex:9999, display:"flex", flexDirection:"column", gap:8 }}>
      {toasts.map(t => (
        <div key={t.id} className={`alert alert-${t.type}`} style={{ minWidth:260, boxShadow:"0 4px 16px rgba(0,0,0,.12)", animation:"fadeIn .25s" }}>
          {t.type==="success" ? "✓" : t.type==="error" ? "✕" : "ℹ"} {t.msg}
        </div>
      ))}
    </div>
  );
}

// ─── MODAL ───────────────────────────────────────────────────────────────────
function Modal({ title, onClose, children, footer }) {
  return (
    <div className="modal-overlay" onClick={e => e.target === e.currentTarget && onClose()}>
      <div className="modal">
        <div className="modal-header">
          <h3>{title}</h3>
          <button className="btn btn-icon btn-outline" onClick={onClose}>{Icon.x}</button>
        </div>
        <div className="modal-body">{children}</div>
        {footer && <div className="modal-footer">{footer}</div>}
      </div>
    </div>
  );
}

// ─── LOGIN PAGE ───────────────────────────────────────────────────────────────
function LoginPage({ onLogin }) {
  const [form, setForm] = useState({ username:"", password:"" });
  const [error, setError] = useState("");
  const [loading, setLoading] = useState(false);
  const handleLogin = () => {
    setError("");
    setLoading(true);
    setTimeout(() => {
      const user = MOCK_USERS.find(u => u.username === form.username && u.password === form.password);
      if (user) onLogin(user);
      else setError("Username atau password salah.");
      setLoading(false);
    }, 700);
  };
  return (
    <div className="login-page">
      <style>{css}</style>
      <div className="login-card">
        <div className="login-logo">
          <div className="icon">☾</div>
          <h1>REMAS Al-Ikhlas</h1>
          <p>Sistem Manajemen Remaja Masjid</p>
        </div>
        {error && <div className="alert alert-error">{error}</div>}
        <div className="form-group">
          <label>Username</label>
          <input className="form-control" placeholder="Masukkan username" value={form.username} onChange={e => setForm({...form, username:e.target.value})} onKeyDown={e => e.key==="Enter" && handleLogin()} />
        </div>
        <div className="form-group">
          <label>Password</label>
          <input type="password" className="form-control" placeholder="Masukkan password" value={form.password} onChange={e => setForm({...form, password:e.target.value})} onKeyDown={e => e.key==="Enter" && handleLogin()} />
        </div>
        <button className="btn btn-primary" style={{width:"100%", justifyContent:"center", padding:"11px", fontSize:"14px", marginTop:4}} onClick={handleLogin} disabled={loading}>
          {loading ? "Memverifikasi..." : "Masuk"}
        </button>
        <div style={{marginTop:20, padding:"14px", background:"#f8f7ff", borderRadius:10, fontSize:12.5, color:"#666"}}>
          <p style={{fontWeight:600, color:"#6741d9", marginBottom:6}}>Demo Akun:</p>
          <p>Admin: <b>admin</b> / admin123</p>
          <p>Pembina: <b>pembina1</b> / pass123</p>
          <p>Anggota: <b>anggota1</b> / pass123</p>
        </div>
      </div>
    </div>
  );
}

// ─── DASHBOARD ───────────────────────────────────────────────────────────────
function Dashboard({ anggota, kegiatan, absensi, prestasi, user }) {
  const totalAnggota = anggota.filter(a => a.status === "Aktif").length;
  const kegiatanBulanIni = kegiatan.filter(k => k.tanggal.startsWith("2025")).length;
  const totalHadir = absensi.filter(a => a.status === "Hadir").length;
  const totalAbsensi = absensi.length;
  const participasiRate = totalAbsensi > 0 ? Math.round((totalHadir / totalAbsensi) * 100) : 0;

  const divisiStats = DIVISI_LIST.map(d => ({
    nama: d,
    count: anggota.filter(a => a.divisi === d && a.status === "Aktif").length
  })).filter(d => d.count > 0);

  const maxDivisi = Math.max(...divisiStats.map(d => d.count), 1);

  const kegiatanMendatang = kegiatan.filter(k => k.status === "Akan Datang").slice(0, 3);

  return (
    <div>
      <div className="stats-grid">
        <div className="stat-card">
          <div className="stat-icon purple">{Icon.users}</div>
          <div><div className="stat-val">{totalAnggota}</div><div className="stat-label">Anggota Aktif</div><div className="stat-sub">+{anggota.filter(a=>a.angkatan==="2023").length} angkatan 2023</div></div>
        </div>
        <div className="stat-card">
          <div className="stat-icon green">{Icon.calendar}</div>
          <div><div className="stat-val">{kegiatanBulanIni}</div><div className="stat-label">Total Kegiatan 2025</div><div className="stat-sub">{kegiatan.filter(k=>k.status==="Akan Datang").length} akan datang</div></div>
        </div>
        <div className="stat-card">
          <div className="stat-icon orange">{Icon.check}</div>
          <div><div className="stat-val">{participasiRate}%</div><div className="stat-label">Tingkat Partisipasi</div><div className="stat-sub">{totalHadir} dari {totalAbsensi} absensi</div></div>
        </div>
        <div className="stat-card">
          <div className="stat-icon blue">{Icon.star}</div>
          <div><div className="stat-val">{prestasi.length}</div><div className="stat-label">Prestasi</div><div className="stat-sub">{prestasi.filter(p=>p.tingkat==="Nasional").length} tingkat nasional</div></div>
        </div>
      </div>

      <div style={{display:"grid", gridTemplateColumns:"1fr 1fr", gap:16}}>
        <div className="card">
          <div className="card-header"><h3>Distribusi Anggota per Divisi</h3></div>
          <div className="card-body">
            <div className="chart-bar-wrap">
              {divisiStats.map(d => (
                <div key={d.nama} className="chart-bar-row">
                  <div className="chart-bar-label">{d.nama}</div>
                  <div className="chart-bar-outer"><div className="chart-bar-inner" style={{width:`${(d.count/maxDivisi)*100}%`}}/></div>
                  <div className="chart-bar-val">{d.count}</div>
                </div>
              ))}
            </div>
          </div>
        </div>

        <div className="card">
          <div className="card-header"><h3>Kegiatan Mendatang</h3></div>
          <div className="card-body">
            {kegiatanMendatang.length === 0 ? (
              <div className="empty-state"><p>Tidak ada kegiatan mendatang</p></div>
            ) : kegiatanMendatang.map(k => (
              <div key={k.id} style={{display:"flex", gap:12, marginBottom:14, paddingBottom:14, borderBottom:"1px solid #f8f7ff"}}>
                <div style={{width:44, height:44, background:"#ede8ff", borderRadius:10, display:"flex", alignItems:"center", justifyContent:"center", flexShrink:0}}>{Icon.calendar}</div>
                <div style={{flex:1}}>
                  <p style={{fontSize:13.5, fontWeight:600, color:"#3b2080"}}>{k.nama}</p>
                  <p style={{fontSize:12, color:"#888", marginTop:2}}>{formatDate(k.tanggal)} · {k.waktu}</p>
                  <p style={{fontSize:12, color:"#9d87ff", marginTop:2}}>📍 {k.lokasi}</p>
                </div>
                <span className={`badge ${getBadgeClass(k.kategori)}`}>{k.kategori}</span>
              </div>
            ))}
          </div>
        </div>

        <div className="card">
          <div className="card-header"><h3>Tingkat Partisipasi Kegiatan</h3></div>
          <div className="card-body">
            {kegiatan.filter(k=>k.status==="Selesai").map(k => {
              const absenKegiatan = absensi.filter(a => a.kegiatanId === k.id);
              const hadir = absenKegiatan.filter(a => a.status === "Hadir").length;
              const pct = absenKegiatan.length > 0 ? Math.round((hadir/absenKegiatan.length)*100) : 0;
              return (
                <div key={k.id} style={{marginBottom:14}}>
                  <div style={{display:"flex", justifyContent:"space-between", marginBottom:5}}>
                    <span style={{fontSize:12.5, color:"#444", fontWeight:500}}>{k.nama}</span>
                    <span style={{fontSize:12.5, fontWeight:700, color:"#6741d9"}}>{pct}%</span>
                  </div>
                  <div className="progress-bar"><div className="progress-fill" style={{width:`${pct}%`}}/></div>
                </div>
              );
            })}
          </div>
        </div>

        <div className="card">
          <div className="card-header"><h3>Prestasi Terbaru</h3></div>
          <div className="card-body">
            {prestasi.slice(0,4).map(p => {
              const a = anggota.find(a => a.id === p.anggotaId);
              return (
                <div key={p.id} style={{display:"flex", gap:10, marginBottom:12, alignItems:"center"}}>
                  <div className="avatar" style={{background:"var(--grad)", width:34, height:34, fontSize:11}}>{a?.avatar||"?"}</div>
                  <div style={{flex:1}}>
                    <p style={{fontSize:13, fontWeight:600, color:"#333"}}>{p.nama}</p>
                    <p style={{fontSize:12, color:"#888"}}>{a?.nama} · {formatDate(p.tanggal)}</p>
                  </div>
                  <span className={`badge ${getBadgeClass(p.tingkat)}`}>{p.tingkat}</span>
                </div>
              );
            })}
          </div>
        </div>
      </div>
    </div>
  );
}

// ─── ANGGOTA PAGE ─────────────────────────────────────────────────────────────
function AnggotaPage({ anggota, setAnggota, isAdmin, setToasts }) {
  const [search, setSearch] = useState("");
  const [filterDivisi, setFilterDivisi] = useState("");
  const [filterStatus, setFilterStatus] = useState("");
  const [modal, setModal] = useState(null);
  const [form, setForm] = useState({});
  const [viewDetail, setViewDetail] = useState(null);

  const filtered = anggota.filter(a =>
    (a.nama.toLowerCase().includes(search.toLowerCase()) || a.email.toLowerCase().includes(search.toLowerCase())) &&
    (filterDivisi === "" || a.divisi === filterDivisi) &&
    (filterStatus === "" || a.status === filterStatus)
  );

  const openAdd = () => { setForm({ nama:"", nik:"", ttl:"", alamat:"", telepon:"", email:"", divisi:"Dakwah", angkatan:"2025", status:"Aktif", gender:"L", avatar:"" }); setModal("add"); };
  const openEdit = a => { setForm({...a}); setModal("edit"); };
  const handleSave = () => {
    if (!form.nama) { toast(setToasts,"Nama wajib diisi","error"); return; }
    if (modal === "add") {
      const newA = {...form, id:Date.now(), avatar:form.nama.split(" ").slice(0,2).map(w=>w[0]).join("").toUpperCase()};
      setAnggota(a => [...a, newA]);
      toast(setToasts, "Anggota berhasil ditambahkan");
    } else {
      setAnggota(a => a.map(x => x.id === form.id ? form : x));
      toast(setToasts, "Data anggota diperbarui");
    }
    setModal(null);
  };
  const handleDelete = id => {
    setAnggota(a => a.filter(x => x.id !== id));
    toast(setToasts, "Anggota dihapus");
  };

  if (viewDetail) {
    const a = viewDetail;
    return (
      <div>
        <div className="back-btn" onClick={() => setViewDetail(null)}>{Icon.back} Kembali ke Daftar Anggota</div>
        <div className="card">
          <div className="card-body">
            <div style={{display:"flex", gap:24, alignItems:"flex-start", flexWrap:"wrap"}}>
              <div className="avatar xl" style={{background:"var(--grad)"}}>{a.avatar}</div>
              <div style={{flex:1}}>
                <h2 style={{fontSize:22, fontWeight:800, color:"#3b2080"}}>{a.nama}</h2>
                <div style={{display:"flex", gap:8, marginTop:6, flexWrap:"wrap"}}>
                  <span className={`badge ${getDivisiClass(a.divisi)}`}>{a.divisi}</span>
                  <span className={`badge ${getBadgeClass(a.status)}`}>{a.status}</span>
                  <span style={{fontSize:12, color:"#888"}}>Angkatan {a.angkatan}</span>
                </div>
                <div style={{marginTop:16, display:"grid", gridTemplateColumns:"1fr 1fr", gap:"8px 24px"}}>
                  {[["NIK", a.nik], ["TTL", a.ttl], ["Telepon", a.telepon], ["Email", a.email], ["Alamat", a.alamat], ["Gender", a.gender==="L"?"Laki-laki":"Perempuan"]].map(([k,v]) => (
                    <div key={k}>
                      <p style={{fontSize:11, color:"#9d87ff", fontWeight:600}}>{k}</p>
                      <p style={{fontSize:13.5, color:"#333", marginTop:2}}>{v||"-"}</p>
                    </div>
                  ))}
                </div>
              </div>
              {isAdmin && <button className="btn btn-outline btn-sm" onClick={() => { setViewDetail(null); openEdit(a); }}>{Icon.edit} Edit</button>}
            </div>
          </div>
        </div>
      </div>
    );
  }

  return (
    <div>
      <div className="card">
        <div className="card-header">
          <h3>Data Anggota ({filtered.length})</h3>
          <div style={{display:"flex", gap:8}}>
            {isAdmin && <button className="btn btn-primary btn-sm" onClick={openAdd}>{Icon.plus} Tambah</button>}
          </div>
        </div>
        <div className="card-body" style={{paddingTop:12}}>
          <div style={{display:"flex", gap:10, marginBottom:16, flexWrap:"wrap"}}>
            <div className="search-wrap" style={{flex:1, minWidth:200}}>
              {Icon.search}
              <input className="search-input" placeholder="Cari anggota..." value={search} onChange={e=>setSearch(e.target.value)} />
            </div>
            <select className="form-control" style={{width:"auto"}} value={filterDivisi} onChange={e=>setFilterDivisi(e.target.value)}>
              <option value="">Semua Divisi</option>
              {DIVISI_LIST.map(d=><option key={d} value={d}>{d}</option>)}
            </select>
            <select className="form-control" style={{width:"auto"}} value={filterStatus} onChange={e=>setFilterStatus(e.target.value)}>
              <option value="">Semua Status</option>
              <option value="Aktif">Aktif</option>
              <option value="Alumni">Alumni</option>
            </select>
          </div>
          <div className="table-wrap">
            <table>
              <thead>
                <tr><th>Anggota</th><th>Divisi</th><th>Kontak</th><th>Angkatan</th><th>Status</th><th>Aksi</th></tr>
              </thead>
              <tbody>
                {filtered.length === 0 ? (
                  <tr><td colSpan="6" style={{textAlign:"center", color:"#aaa", padding:32}}>Tidak ada data</td></tr>
                ) : filtered.map(a => (
                  <tr key={a.id}>
                    <td>
                      <div style={{display:"flex", alignItems:"center", gap:10}}>
                        <div className="avatar" style={{background:"var(--grad)"}}>{a.avatar}</div>
                        <div><p style={{fontWeight:600, color:"#3b2080"}}>{a.nama}</p><p style={{fontSize:11.5, color:"#888"}}>{a.gender==="L"?"Laki-laki":"Perempuan"}</p></div>
                      </div>
                    </td>
                    <td><span className={`badge ${getDivisiClass(a.divisi)}`}>{a.divisi}</span></td>
                    <td><p style={{fontSize:12.5}}>{a.telepon}</p><p style={{fontSize:12, color:"#888"}}>{a.email}</p></td>
                    <td style={{fontSize:13}}>{a.angkatan}</td>
                    <td><span className={`badge ${getBadgeClass(a.status)}`}>{a.status}</span></td>
                    <td>
                      <div style={{display:"flex", gap:4}}>
                        <button className="btn btn-icon btn-outline btn-sm" title="Lihat" onClick={()=>setViewDetail(a)}>{Icon.eye}</button>
                        {isAdmin && <>
                          <button className="btn btn-icon btn-outline btn-sm" title="Edit" onClick={()=>openEdit(a)}>{Icon.edit}</button>
                          <button className="btn btn-icon btn-danger btn-sm" title="Hapus" onClick={()=>handleDelete(a.id)}>{Icon.trash}</button>
                        </>}
                      </div>
                    </td>
                  </tr>
                ))}
              </tbody>
            </table>
          </div>
        </div>
      </div>

      {modal && (
        <Modal title={modal==="add"?"Tambah Anggota":"Edit Anggota"} onClose={()=>setModal(null)}
          footer={<><button className="btn btn-outline" onClick={()=>setModal(null)}>Batal</button><button className="btn btn-primary" onClick={handleSave}>Simpan</button></>}>
          <div className="form-row">
            <div className="form-group"><label>Nama Lengkap *</label><input className="form-control" value={form.nama||""} onChange={e=>setForm({...form,nama:e.target.value})} /></div>
            <div className="form-group"><label>NIK</label><input className="form-control" value={form.nik||""} onChange={e=>setForm({...form,nik:e.target.value})} /></div>
          </div>
          <div className="form-row">
            <div className="form-group"><label>Tempat, Tanggal Lahir</label><input className="form-control" value={form.ttl||""} onChange={e=>setForm({...form,ttl:e.target.value})} placeholder="Jakarta, 01-01-2000" /></div>
            <div className="form-group"><label>Gender</label>
              <select className="form-control" value={form.gender||"L"} onChange={e=>setForm({...form,gender:e.target.value})}>
                <option value="L">Laki-laki</option><option value="P">Perempuan</option>
              </select>
            </div>
          </div>
          <div className="form-group"><label>Alamat</label><textarea className="form-control" rows={2} value={form.alamat||""} onChange={e=>setForm({...form,alamat:e.target.value})} /></div>
          <div className="form-row">
            <div className="form-group"><label>Telepon</label><input className="form-control" value={form.telepon||""} onChange={e=>setForm({...form,telepon:e.target.value})} /></div>
            <div className="form-group"><label>Email</label><input className="form-control" value={form.email||""} onChange={e=>setForm({...form,email:e.target.value})} /></div>
          </div>
          <div className="form-row">
            <div className="form-group"><label>Divisi</label>
              <select className="form-control" value={form.divisi||"Dakwah"} onChange={e=>setForm({...form,divisi:e.target.value})}>
                {DIVISI_LIST.map(d=><option key={d} value={d}>{d}</option>)}
              </select>
            </div>
            <div className="form-group"><label>Angkatan</label>
              <select className="form-control" value={form.angkatan||"2025"} onChange={e=>setForm({...form,angkatan:e.target.value})}>
                {["2020","2021","2022","2023","2024","2025"].map(y=><option key={y} value={y}>{y}</option>)}
              </select>
            </div>
          </div>
          <div className="form-group"><label>Status</label>
            <select className="form-control" value={form.status||"Aktif"} onChange={e=>setForm({...form,status:e.target.value})}>
              <option value="Aktif">Aktif</option><option value="Alumni">Alumni</option>
            </select>
          </div>
        </Modal>
      )}
    </div>
  );
}

// ─── KEGIATAN PAGE ────────────────────────────────────────────────────────────
function KegiatanPage({ kegiatan, setKegiatan, anggota, absensi, setAbsensi, isAdmin, setToasts, user }) {
  const [search, setSearch] = useState("");
  const [modal, setModal] = useState(null);
  const [form, setForm] = useState({});
  const [detailId, setDetailId] = useState(null);
  const [absenModal, setAbsenModal] = useState(false);
  const [absenMap, setAbsenMap] = useState({});

  const filtered = kegiatan.filter(k =>
    k.nama.toLowerCase().includes(search.toLowerCase()) ||
    k.kategori.toLowerCase().includes(search.toLowerCase())
  );

  const openAdd = () => { setForm({ nama:"", tanggal:"", waktu:"", lokasi:"", deskripsi:"", kategori:"Kajian", status:"Akan Datang", pembina:"" }); setModal("add"); };
  const openEdit = k => { setForm({...k}); setModal("edit"); };
  const handleSave = () => {
    if (!form.nama || !form.tanggal) { toast(setToasts,"Nama & tanggal wajib diisi","error"); return; }
    if (modal === "add") {
      setKegiatan(k => [...k, {...form, id:Date.now()}]);
      toast(setToasts, "Kegiatan berhasil ditambahkan");
    } else {
      setKegiatan(k => k.map(x => x.id === form.id ? form : x));
      toast(setToasts, "Kegiatan diperbarui");
    }
    setModal(null);
  };
  const handleDelete = id => { setKegiatan(k => k.filter(x => x.id !== id)); toast(setToasts, "Kegiatan dihapus"); };

  const openAbsensi = (k) => {
    setDetailId(k.id);
    const existing = {};
    absensi.filter(a => a.kegiatanId === k.id).forEach(a => { existing[a.anggotaId] = a.status; });
    const aktif = anggota.filter(a => a.status === "Aktif");
    const full = {};
    aktif.forEach(a => { full[a.id] = existing[a.id] || ""; });
    setAbsenMap(full);
    setAbsenModal(true);
  };

  const handleSimpanAbsensi = () => {
    const newAbsensi = absensi.filter(a => a.kegiatanId !== detailId);
    const entries = Object.entries(absenMap).filter(([,s]) => s !== "").map(([id, status]) => ({
      id: Date.now() + parseInt(id),
      kegiatanId: detailId,
      anggotaId: parseInt(id),
      status,
      waktuAbsen: status === "Hadir" ? new Date().toTimeString().slice(0,5) : "-",
      keterangan: ""
    }));
    setAbsensi([...newAbsensi, ...entries]);
    toast(setToasts, "Absensi berhasil disimpan");
    setAbsenModal(false);
  };

  const kegiatanDetail = kegiatan.find(k => k.id === detailId);

  return (
    <div>
      <div className="card">
        <div className="card-header">
          <h3>Manajemen Kegiatan ({filtered.length})</h3>
          {isAdmin && <button className="btn btn-primary btn-sm" onClick={openAdd}>{Icon.plus} Tambah Kegiatan</button>}
        </div>
        <div className="card-body" style={{paddingTop:12}}>
          <div style={{marginBottom:16}}>
            <div className="search-wrap">
              {Icon.search}
              <input className="search-input" placeholder="Cari kegiatan..." value={search} onChange={e=>setSearch(e.target.value)} />
            </div>
          </div>
          <div className="table-wrap">
            <table>
              <thead><tr><th>Kegiatan</th><th>Tanggal & Waktu</th><th>Lokasi</th><th>Pembina</th><th>Kategori</th><th>Status</th><th>Aksi</th></tr></thead>
              <tbody>
                {filtered.map(k => {
                  const absenKegiatan = absensi.filter(a => a.kegiatanId === k.id);
                  return (
                    <tr key={k.id}>
                      <td><p style={{fontWeight:600, color:"#3b2080"}}>{k.nama}</p><p style={{fontSize:12, color:"#aaa"}}>{k.deskripsi?.slice(0,40)}...</p></td>
                      <td><p style={{fontSize:13}}>{formatDate(k.tanggal)}</p><p style={{fontSize:12, color:"#888"}}>{k.waktu} WIB</p></td>
                      <td style={{fontSize:12.5}}>{k.lokasi}</td>
                      <td style={{fontSize:12.5}}>{k.pembina}</td>
                      <td><span className={`badge ${getBadgeClass(k.kategori)}`}>{k.kategori}</span></td>
                      <td><span className={`badge ${getBadgeClass(k.status)}`}>{k.status}</span></td>
                      <td>
                        <div style={{display:"flex", gap:4}}>
                          <button className="btn btn-outline btn-sm" onClick={() => openAbsensi(k)} title="Absensi">
                            {Icon.check} <span style={{fontSize:11}}>{absenKegiatan.length}</span>
                          </button>
                          {isAdmin && <>
                            <button className="btn btn-icon btn-outline btn-sm" onClick={()=>openEdit(k)}>{Icon.edit}</button>
                            <button className="btn btn-icon btn-danger btn-sm" onClick={()=>handleDelete(k.id)}>{Icon.trash}</button>
                          </>}
                        </div>
                      </td>
                    </tr>
                  );
                })}
              </tbody>
            </table>
          </div>
        </div>
      </div>

      {/* Modal Form Kegiatan */}
      {modal && (
        <Modal title={modal==="add"?"Tambah Kegiatan":"Edit Kegiatan"} onClose={()=>setModal(null)}
          footer={<><button className="btn btn-outline" onClick={()=>setModal(null)}>Batal</button><button className="btn btn-primary" onClick={handleSave}>Simpan</button></>}>
          <div className="form-group"><label>Nama Kegiatan *</label><input className="form-control" value={form.nama||""} onChange={e=>setForm({...form,nama:e.target.value})} /></div>
          <div className="form-row">
            <div className="form-group"><label>Tanggal *</label><input type="date" className="form-control" value={form.tanggal||""} onChange={e=>setForm({...form,tanggal:e.target.value})} /></div>
            <div className="form-group"><label>Waktu</label><input type="time" className="form-control" value={form.waktu||""} onChange={e=>setForm({...form,waktu:e.target.value})} /></div>
          </div>
          <div className="form-group"><label>Lokasi</label><input className="form-control" value={form.lokasi||""} onChange={e=>setForm({...form,lokasi:e.target.value})} /></div>
          <div className="form-group"><label>Deskripsi</label><textarea className="form-control" rows={2} value={form.deskripsi||""} onChange={e=>setForm({...form,deskripsi:e.target.value})} /></div>
          <div className="form-row">
            <div className="form-group"><label>Kategori</label>
              <select className="form-control" value={form.kategori||"Kajian"} onChange={e=>setForm({...form,kategori:e.target.value})}>
                {KATEGORI_KEGIATAN.map(k=><option key={k} value={k}>{k}</option>)}
              </select>
            </div>
            <div className="form-group"><label>Status</label>
              <select className="form-control" value={form.status||"Akan Datang"} onChange={e=>setForm({...form,status:e.target.value})}>
                <option value="Akan Datang">Akan Datang</option><option value="Selesai">Selesai</option>
              </select>
            </div>
          </div>
          <div className="form-group"><label>Pembina</label><input className="form-control" value={form.pembina||""} onChange={e=>setForm({...form,pembina:e.target.value})} /></div>
        </Modal>
      )}

      {/* Modal Absensi */}
      {absenModal && kegiatanDetail && (
        <Modal title={`Absensi: ${kegiatanDetail.nama}`} onClose={()=>setAbsenModal(false)}
          footer={<><button className="btn btn-outline" onClick={()=>setAbsenModal(false)}>Tutup</button>{isAdmin && <button className="btn btn-primary" onClick={handleSimpanAbsensi}>Simpan Absensi</button>}</>}>
          <div style={{background:"#f8f7ff", borderRadius:10, padding:"12px 14px", marginBottom:16, fontSize:13}}>
            <p><b style={{color:"#6741d9"}}>📅</b> {formatDate(kegiatanDetail.tanggal)} · {kegiatanDetail.waktu} WIB</p>
            <p style={{marginTop:4}}><b style={{color:"#6741d9"}}>📍</b> {kegiatanDetail.lokasi}</p>
          </div>
          <div style={{display:"flex", gap:8, marginBottom:12, fontSize:12}}>
            <span style={{background:"#dcfce7",color:"#16a34a",padding:"3px 10px",borderRadius:20,fontWeight:600}}>H = Hadir</span>
            <span style={{background:"#fef9c3",color:"#ca8a04",padding:"3px 10px",borderRadius:20,fontWeight:600}}>I = Izin</span>
            <span style={{background:"#fee2e2",color:"#dc2626",padding:"3px 10px",borderRadius:20,fontWeight:600}}>A = Alpha</span>
          </div>
          <div style={{maxHeight:340, overflowY:"auto"}}>
            {anggota.filter(a=>a.status==="Aktif").map(a => (
              <div key={a.id} className={`absensi-card ${absenMap[a.id]?.toLowerCase()||""}`} style={{marginBottom:8}}>
                <div className="avatar" style={{background:"var(--grad)", width:32, height:32, fontSize:11}}>{a.avatar}</div>
                <div className="absensi-name">{a.nama}</div>
                <div className="absensi-status">
                  {isAdmin ? (
                    <>
                      <button className={`status-btn h${absenMap[a.id]==="Hadir"?" active":""}`} onClick={()=>setAbsenMap(m=>({...m,[a.id]:"Hadir"}))}>H</button>
                      <button className={`status-btn i${absenMap[a.id]==="Izin"?" active":""}`} onClick={()=>setAbsenMap(m=>({...m,[a.id]:"Izin"}))}>I</button>
                      <button className={`status-btn a${absenMap[a.id]==="Alpha"?" active":""}`} onClick={()=>setAbsenMap(m=>({...m,[a.id]:"Alpha"}))}>A</button>
                    </>
                  ) : (
                    absenMap[a.id] ? <span className={`badge ${getBadgeClass(absenMap[a.id])}`}>{absenMap[a.id]}</span> : <span style={{fontSize:12,color:"#aaa"}}>Belum</span>
                  )}
                </div>
              </div>
            ))}
          </div>
        </Modal>
      )}
    </div>
  );
}

// ─── PRESTASI PAGE ─────────────────────────────────────────────────────────────
function PrestasiPage({ prestasi, setPrestasi, anggota, isAdmin, setToasts }) {
  const [modal, setModal] = useState(null);
  const [form, setForm] = useState({});
  const [search, setSearch] = useState("");

  const filtered = prestasi.filter(p => {
    const a = anggota.find(x => x.id === p.anggotaId);
    return p.nama.toLowerCase().includes(search.toLowerCase()) || a?.nama.toLowerCase().includes(search.toLowerCase());
  });

  const openAdd = () => { setForm({ anggotaId:"", nama:"", tanggal:"", kategori:"Keagamaan", tingkat:"Kecamatan", keterangan:"" }); setModal("add"); };
  const openEdit = p => { setForm({...p, anggotaId:String(p.anggotaId)}); setModal("edit"); };
  const handleSave = () => {
    if (!form.nama || !form.anggotaId) { toast(setToasts,"Nama dan anggota wajib diisi","error"); return; }
    const data = {...form, anggotaId:parseInt(form.anggotaId)};
    if (modal==="add") { setPrestasi(p=>[...p,{...data,id:Date.now()}]); toast(setToasts,"Prestasi ditambahkan"); }
    else { setPrestasi(p=>p.map(x=>x.id===data.id?data:x)); toast(setToasts,"Prestasi diperbarui"); }
    setModal(null);
  };
  const handleDelete = id => { setPrestasi(p=>p.filter(x=>x.id!==id)); toast(setToasts,"Prestasi dihapus"); };

  return (
    <div>
      <div className="card">
        <div className="card-header">
          <h3>Data Prestasi ({filtered.length})</h3>
          {isAdmin && <button className="btn btn-primary btn-sm" onClick={openAdd}>{Icon.plus} Tambah</button>}
        </div>
        <div className="card-body" style={{paddingTop:12}}>
          <div style={{marginBottom:16}}>
            <div className="search-wrap">
              {Icon.search}
              <input className="search-input" placeholder="Cari prestasi..." value={search} onChange={e=>setSearch(e.target.value)} />
            </div>
          </div>
          <div className="table-wrap">
            <table>
              <thead><tr><th>Prestasi</th><th>Anggota</th><th>Kategori</th><th>Tingkat</th><th>Tanggal</th><th>Keterangan</th>{isAdmin && <th>Aksi</th>}</tr></thead>
              <tbody>
                {filtered.map(p => {
                  const a = anggota.find(x=>x.id===p.anggotaId);
                  return (
                    <tr key={p.id}>
                      <td style={{fontWeight:600, color:"#3b2080"}}>{p.nama}</td>
                      <td>
                        <div style={{display:"flex", alignItems:"center", gap:8}}>
                          <div className="avatar" style={{background:"var(--grad)", width:28, height:28, fontSize:10}}>{a?.avatar}</div>
                          <span style={{fontSize:13}}>{a?.nama||"-"}</span>
                        </div>
                      </td>
                      <td><span className={`badge ${getBadgeClass(p.kategori)}`}>{p.kategori}</span></td>
                      <td><span className={`badge ${getBadgeClass(p.tingkat)}`}>{p.tingkat}</span></td>
                      <td style={{fontSize:13}}>{formatDate(p.tanggal)}</td>
                      <td style={{fontSize:12.5, color:"#666"}}>{p.keterangan||"-"}</td>
                      {isAdmin && (
                        <td>
                          <div style={{display:"flex",gap:4}}>
                            <button className="btn btn-icon btn-outline btn-sm" onClick={()=>openEdit(p)}>{Icon.edit}</button>
                            <button className="btn btn-icon btn-danger btn-sm" onClick={()=>handleDelete(p.id)}>{Icon.trash}</button>
                          </div>
                        </td>
                      )}
                    </tr>
                  );
                })}
              </tbody>
            </table>
          </div>
        </div>
      </div>

      {modal && (
        <Modal title={modal==="add"?"Tambah Prestasi":"Edit Prestasi"} onClose={()=>setModal(null)}
          footer={<><button className="btn btn-outline" onClick={()=>setModal(null)}>Batal</button><button className="btn btn-primary" onClick={handleSave}>Simpan</button></>}>
          <div className="form-group"><label>Nama Prestasi *</label><input className="form-control" value={form.nama||""} onChange={e=>setForm({...form,nama:e.target.value})} /></div>
          <div className="form-group"><label>Anggota *</label>
            <select className="form-control" value={form.anggotaId||""} onChange={e=>setForm({...form,anggotaId:e.target.value})}>
              <option value="">-- Pilih Anggota --</option>
              {anggota.filter(a=>a.status==="Aktif").map(a=><option key={a.id} value={a.id}>{a.nama}</option>)}
            </select>
          </div>
          <div className="form-row">
            <div className="form-group"><label>Kategori</label>
              <select className="form-control" value={form.kategori||"Keagamaan"} onChange={e=>setForm({...form,kategori:e.target.value})}>
                {["Keagamaan","Seni","Akademik","Olahraga","Kepemimpinan","Lainnya"].map(k=><option key={k} value={k}>{k}</option>)}
              </select>
            </div>
            <div className="form-group"><label>Tingkat</label>
              <select className="form-control" value={form.tingkat||"Kecamatan"} onChange={e=>setForm({...form,tingkat:e.target.value})}>
                {["Kecamatan","Kota","Provinsi","Nasional","Internasional"].map(t=><option key={t} value={t}>{t}</option>)}
              </select>
            </div>
          </div>
          <div className="form-group"><label>Tanggal</label><input type="date" className="form-control" value={form.tanggal||""} onChange={e=>setForm({...form,tanggal:e.target.value})} /></div>
          <div className="form-group"><label>Keterangan</label><textarea className="form-control" rows={2} value={form.keterangan||""} onChange={e=>setForm({...form,keterangan:e.target.value})} /></div>
        </Modal>
      )}
    </div>
  );
}

// ─── LAPORAN PAGE ──────────────────────────────────────────────────────────────
function LaporanPage({ anggota, kegiatan, absensi, prestasi, setToasts }) {
  const handleBackup = () => {
    const data = { anggota, kegiatan, absensi, prestasi, exportedAt: new Date().toISOString() };
    const blob = new Blob([JSON.stringify(data, null, 2)], { type:"application/json" });
    const url = URL.createObjectURL(blob);
    const a = document.createElement("a");
    a.href = url; a.download = `backup-remas-${new Date().toISOString().slice(0,10)}.json`;
    a.click(); URL.revokeObjectURL(url);
    toast(setToasts, "Data berhasil dibackup!");
  };

  const kegiatanSelesai = kegiatan.filter(k=>k.status==="Selesai");
  const partisipasi = kegiatanSelesai.map(k => {
    const abs = absensi.filter(a=>a.kegiatanId===k.id);
    const hadir = abs.filter(a=>a.status==="Hadir").length;
    const izin = abs.filter(a=>a.status==="Izin").length;
    const alpha = abs.filter(a=>a.status==="Alpha").length;
    const pct = abs.length > 0 ? Math.round((hadir/abs.length)*100) : 0;
    return { ...k, hadir, izin, alpha, total:abs.length, pct };
  });

  const anggotaStat = anggota.filter(a=>a.status==="Aktif").map(a => {
    const myAbsen = absensi.filter(ab=>ab.anggotaId===a.id);
    const hadir = myAbsen.filter(ab=>ab.status==="Hadir").length;
    const pct = myAbsen.length > 0 ? Math.round((hadir/myAbsen.length)*100) : 0;
    return {...a, hadirCount:hadir, totalKegiatan:myAbsen.length, pct};
  }).sort((a,b) => b.pct - a.pct);

  return (
    <div>
      <div style={{display:"flex", justifyContent:"flex-end", marginBottom:16}}>
        <button className="btn btn-primary" onClick={handleBackup}>{Icon.download} Backup Data JSON</button>
      </div>

      <div className="card" style={{marginBottom:16}}>
        <div className="card-header"><h3>Laporan Partisipasi per Kegiatan</h3></div>
        <div className="card-body">
          <div className="table-wrap">
            <table>
              <thead><tr><th>Kegiatan</th><th>Tanggal</th><th>Hadir</th><th>Izin</th><th>Alpha</th><th>Total</th><th>Tingkat Partisipasi</th></tr></thead>
              <tbody>
                {partisipasi.map(k => (
                  <tr key={k.id}>
                    <td style={{fontWeight:600, color:"#3b2080"}}>{k.nama}</td>
                    <td style={{fontSize:13}}>{formatDate(k.tanggal)}</td>
                    <td><span className="badge hadir">{k.hadir}</span></td>
                    <td><span className="badge izin">{k.izin}</span></td>
                    <td><span className="badge alpha">{k.alpha}</span></td>
                    <td style={{fontSize:13, fontWeight:600}}>{k.total}</td>
                    <td style={{minWidth:160}}>
                      <div style={{display:"flex", alignItems:"center", gap:8}}>
                        <div className="progress-bar" style={{flex:1}}><div className="progress-fill" style={{width:`${k.pct}%`}}/></div>
                        <span style={{fontSize:13, fontWeight:700, color:"#6741d9", width:36}}>{k.pct}%</span>
                      </div>
                    </td>
                  </tr>
                ))}
              </tbody>
            </table>
          </div>
        </div>
      </div>

      <div className="card">
        <div className="card-header"><h3>Laporan Kehadiran per Anggota</h3></div>
        <div className="card-body">
          <div className="table-wrap">
            <table>
              <thead><tr><th>Anggota</th><th>Divisi</th><th>Kegiatan Diikuti</th><th>Hadir</th><th>Tingkat Kehadiran</th></tr></thead>
              <tbody>
                {anggotaStat.map((a, i) => (
                  <tr key={a.id}>
                    <td>
                      <div style={{display:"flex", alignItems:"center", gap:8}}>
                        <span style={{fontSize:11, color:"#aaa", width:20}}>{i+1}.</span>
                        <div className="avatar" style={{background:"var(--grad)", width:30, height:30, fontSize:10}}>{a.avatar}</div>
                        <span style={{fontWeight:600, color:"#3b2080"}}>{a.nama}</span>
                      </div>
                    </td>
                    <td><span className={`badge ${getDivisiClass(a.divisi)}`}>{a.divisi}</span></td>
                    <td style={{textAlign:"center", fontSize:13}}>{a.totalKegiatan}</td>
                    <td style={{textAlign:"center", fontSize:13, fontWeight:600, color:"#16a34a"}}>{a.hadirCount}</td>
                    <td style={{minWidth:160}}>
                      <div style={{display:"flex", alignItems:"center", gap:8}}>
                        <div className="progress-bar" style={{flex:1}}><div className="progress-fill" style={{width:`${a.pct}%`}}/></div>
                        <span style={{fontSize:13, fontWeight:700, color:"#6741d9", width:36}}>{a.pct}%</span>
                      </div>
                    </td>
                  </tr>
                ))}
              </tbody>
            </table>
          </div>
        </div>
      </div>
    </div>
  );
}

// ─── NOTIFIKASI PANEL ─────────────────────────────────────────────────────────
const NOTIFS = [
  { id:1, title:"Kajian Tafsir Besok", msg:"Jangan lupa kajian rutin besok malam pukul 19:30 di lantai 2.", time:"1 jam lalu", unread:true },
  { id:2, title:"Anggota Baru Terdaftar", msg:"Muhammad Rizki telah mendaftar sebagai anggota baru divisi Dakwah.", time:"3 jam lalu", unread:true },
  { id:3, title:"Absensi Bakti Sosial", msg:"Absensi kegiatan Bakti Sosial Ramadhan telah berhasil disimpan.", time:"2 hari lalu", unread:false },
  { id:4, title:"Prestasi Baru", msg:"Selamat! Abdullah Hasan meraih juara di tingkat Provinsi.", time:"1 minggu lalu", unread:false },
];

// ─── ARSITEKTUR PAGE ───────────────────────────────────────────────────────────
function ArsitekturPage() {
  const sections = [
    {
      title: "Struktur Folder Backend (Node.js + Express)",
      content: `remas-backend/
├── src/
│   ├── config/
│   │   ├── database.js      # Koneksi MySQL/PostgreSQL
│   │   └── env.js           # Environment variables
│   ├── controllers/
│   │   ├── authController.js
│   │   ├── anggotaController.js
│   │   ├── kegiatanController.js
│   │   ├── absensiController.js
│   │   └── prestasiController.js
│   ├── middleware/
│   │   ├── auth.js          # JWT verification
│   │   ├── roleCheck.js     # Admin/Pembina/Anggota guard
│   │   └── validate.js      # Request validation
│   ├── models/
│   │   ├── User.js
│   │   ├── Anggota.js
│   │   ├── Kegiatan.js
│   │   ├── Absensi.js
│   │   └── Prestasi.js
│   ├── routes/
│   │   ├── auth.routes.js
│   │   ├── anggota.routes.js
│   │   ├── kegiatan.routes.js
│   │   ├── absensi.routes.js
│   │   └── prestasi.routes.js
│   ├── services/
│   │   ├── emailService.js  # Nodemailer
│   │   └── backupService.js
│   └── app.js               # Express entry point
├── migrations/              # DB migrations
├── .env
└── package.json`
    },
    {
      title: "Skema Database (SQL)",
      content: `-- Tabel users (admin & pembina)
CREATE TABLE users (
  id INT PRIMARY KEY AUTO_INCREMENT,
  username VARCHAR(50) UNIQUE NOT NULL,
  password_hash VARCHAR(255) NOT NULL,
  role ENUM('admin','pembina','anggota') DEFAULT 'anggota',
  name VARCHAR(100) NOT NULL,
  email VARCHAR(100) UNIQUE NOT NULL,
  jabatan VARCHAR(100),
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

-- Tabel anggota
CREATE TABLE anggota (
  id INT PRIMARY KEY AUTO_INCREMENT,
  user_id INT REFERENCES users(id),
  nama VARCHAR(100) NOT NULL,
  nik VARCHAR(16) UNIQUE,
  ttl VARCHAR(100),
  alamat TEXT,
  telepon VARCHAR(20),
  email VARCHAR(100),
  divisi ENUM('Dakwah','Sosial','Olahraga','Seni','Pendidikan','Humas'),
  angkatan YEAR,
  status ENUM('Aktif','Alumni') DEFAULT 'Aktif',
  gender ENUM('L','P'),
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

-- Tabel kegiatan
CREATE TABLE kegiatan (
  id INT PRIMARY KEY AUTO_INCREMENT,
  nama VARCHAR(200) NOT NULL,
  tanggal DATE NOT NULL,
  waktu TIME,
  lokasi VARCHAR(200),
  deskripsi TEXT,
  kategori ENUM('Kajian','Sosial','Rapat','Seni','Olahraga','Lainnya'),
  status ENUM('Akan Datang','Selesai') DEFAULT 'Akan Datang',
  pembina_id INT REFERENCES users(id),
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

-- Tabel absensi (relasi many-to-many)
CREATE TABLE absensi (
  id INT PRIMARY KEY AUTO_INCREMENT,
  kegiatan_id INT NOT NULL REFERENCES kegiatan(id) ON DELETE CASCADE,
  anggota_id INT NOT NULL REFERENCES anggota(id) ON DELETE CASCADE,
  status ENUM('Hadir','Izin','Alpha') NOT NULL,
  waktu_absen TIME,
  keterangan TEXT,
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
  UNIQUE KEY unique_absen (kegiatan_id, anggota_id)  -- Cegah absensi ganda
);

-- Tabel prestasi
CREATE TABLE prestasi (
  id INT PRIMARY KEY AUTO_INCREMENT,
  anggota_id INT NOT NULL REFERENCES anggota(id) ON DELETE CASCADE,
  nama VARCHAR(200) NOT NULL,
  tanggal DATE,
  kategori VARCHAR(100),
  tingkat ENUM('Kecamatan','Kota','Provinsi','Nasional','Internasional'),
  keterangan TEXT,
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);`
    },
    {
      title: "API Endpoints",
      content: `# AUTH
POST   /api/auth/login          # Login & dapatkan JWT token
POST   /api/auth/logout         # Logout (invalidate token)
GET    /api/auth/me             # Data user saat ini

# ANGGOTA (Admin/Pembina only untuk CUD)
GET    /api/anggota             # Daftar semua anggota
POST   /api/anggota             # Tambah anggota baru [ADMIN]
GET    /api/anggota/:id         # Detail anggota
PUT    /api/anggota/:id         # Update data anggota [ADMIN]
DELETE /api/anggota/:id         # Hapus anggota [ADMIN]

# KEGIATAN
GET    /api/kegiatan            # Daftar kegiatan
POST   /api/kegiatan            # Buat kegiatan baru [ADMIN]
GET    /api/kegiatan/:id        # Detail kegiatan + daftar hadir
PUT    /api/kegiatan/:id        # Update kegiatan [ADMIN]
DELETE /api/kegiatan/:id        # Hapus kegiatan [ADMIN]
GET    /api/kegiatan/mendatang  # Kegiatan yang akan datang

# ABSENSI (Mencegah absensi ganda via UNIQUE constraint)
GET    /api/absensi/:kegiatanId # Daftar absensi per kegiatan
POST   /api/absensi             # Input absensi [ADMIN/PEMBINA]
PUT    /api/absensi/:id         # Update status absensi [ADMIN]
GET    /api/absensi/anggota/:id # Rekap kehadiran per anggota

# PRESTASI
GET    /api/prestasi            # Daftar prestasi
POST   /api/prestasi            # Tambah prestasi [ADMIN]
PUT    /api/prestasi/:id        # Edit prestasi [ADMIN]
DELETE /api/prestasi/:id        # Hapus prestasi [ADMIN]

# LAPORAN
GET    /api/laporan/partisipasi # Laporan tingkat partisipasi
GET    /api/laporan/kehadiran   # Rekap kehadiran per anggota
GET    /api/laporan/backup      # Export data JSON [ADMIN]`
    },
    {
      title: "Sample Controller: Absensi (validasi ganda)",
      content: `// controllers/absensiController.js
const db = require('../config/database');

// Input absensi (batch untuk 1 kegiatan)
exports.inputAbsensi = async (req, res) => {
  const { kegiatan_id, absensi_list } = req.body;
  // absensi_list: [{anggota_id, status, keterangan}, ...]

  const conn = await db.getConnection();
  await conn.beginTransaction();
  try {
    for (const item of absensi_list) {
      // INSERT ... ON DUPLICATE KEY UPDATE mencegah duplikasi
      await conn.query(\`
        INSERT INTO absensi (kegiatan_id, anggota_id, status, keterangan, waktu_absen)
        VALUES (?, ?, ?, ?, NOW())
        ON DUPLICATE KEY UPDATE
          status = VALUES(status),
          keterangan = VALUES(keterangan)
      \`, [kegiatan_id, item.anggota_id, item.status, item.keterangan || '']);
    }
    await conn.commit();
    res.json({ success: true, message: 'Absensi berhasil disimpan' });
  } catch (err) {
    await conn.rollback();
    res.status(500).json({ error: err.message });
  } finally {
    conn.release();
  }
};

// middleware/roleCheck.js
exports.adminOnly = (req, res, next) => {
  if (req.user.role !== 'admin') {
    return res.status(403).json({ error: 'Akses ditolak: hanya Admin' });
  }
  next();
};

exports.adminOrPembina = (req, res, next) => {
  if (!['admin', 'pembina'].includes(req.user.role)) {
    return res.status(403).json({ error: 'Akses ditolak' });
  }
  next();
};`
    }
  ];

  return (
    <div>
      <div className="alert alert-info" style={{marginBottom:20}}>
        ℹ️ Berikut adalah arsitektur backend lengkap untuk Sistem Manajemen Remaja Masjid
      </div>
      {sections.map((s, i) => (
        <div key={i} className="card" style={{marginBottom:16}}>
          <div className="card-header"><h3>{s.title}</h3></div>
          <div className="card-body">
            <pre style={{background:"#1e1b4b", color:"#c4b5fd", padding:16, borderRadius:10, fontSize:12, overflowX:"auto", lineHeight:1.7, fontFamily:"monospace"}}>
              {s.content}
            </pre>
          </div>
        </div>
      ))}
    </div>
  );
}

// ─── MAIN APP ─────────────────────────────────────────────────────────────────
export default function App() {
  const [user, setUser] = useState(null);
  const [page, setPage] = useState("dashboard");
  const [anggota, setAnggota] = useState(INIT_ANGGOTA);
  const [kegiatan, setKegiatan] = useState(INIT_KEGIATAN);
  const [absensi, setAbsensi] = useState(INIT_ABSENSI);
  const [prestasi, setPrestasi] = useState(INIT_PRESTASI);
  const [toasts, setToasts] = useState([]);
  const [showNotif, setShowNotif] = useState(false);
  const [notifRead, setNotifRead] = useState([]);

  const isAdmin = user?.role === "admin" || user?.role === "pembina";
  const unreadCount = NOTIFS.filter(n => n.unread && !notifRead.includes(n.id)).length;

  if (!user) return <LoginPage onLogin={u => { setUser(u); setPage("dashboard"); }} />;

  const navItems = [
    { id:"dashboard", label:"Dashboard", icon:Icon.dashboard, group:"Utama" },
    { id:"anggota", label:"Data Anggota", icon:Icon.users, group:"Utama" },
    { id:"kegiatan", label:"Kegiatan & Absensi", icon:Icon.calendar, group:"Utama" },
    { id:"prestasi", label:"Prestasi", icon:Icon.star, group:"Utama" },
    ...(isAdmin ? [
      { id:"laporan", label:"Laporan", icon:Icon.report, group:"Admin" },
      { id:"arsitektur", label:"Arsitektur & API", icon:Icon.shield, group:"Admin" },
    ] : []),
  ];

  const groups = [...new Set(navItems.map(n => n.group))];

  const pageTitle = {
    dashboard:"Dashboard",
    anggota:"Data Anggota",
    kegiatan:"Kegiatan & Absensi",
    prestasi:"Prestasi",
    laporan:"Laporan & Backup",
    arsitektur:"Arsitektur Backend & API",
  };

  return (
    <div className="app-wrap">
      <style>{css}</style>

      {/* Sidebar */}
      <div className="sidebar">
        <div className="sidebar-logo">
          <div className="sidebar-logo-icon">☾</div>
          <h1>REMAS Al-Ikhlas</h1>
          <p>Sistem Manajemen</p>
        </div>
        <div className="sidebar-nav">
          {groups.map(g => (
            <div key={g}>
              <div className="sidebar-section">{g}</div>
              {navItems.filter(n=>n.group===g).map(n => (
                <div key={n.id} className={`nav-item${page===n.id?" active":""}`} onClick={()=>setPage(n.id)}>
                  {n.icon}{n.label}
                </div>
              ))}
            </div>
          ))}
        </div>
        <div className="sidebar-footer">
          <div className="user-card">
            <div className="avatar">{user.avatar}</div>
            <div className="user-card-info">
              <div className="name">{user.name}</div>
              <div className="role"><span className={`tag-role-${user.role}`}>{user.role}</span></div>
            </div>
          </div>
          <button className="btn btn-outline btn-sm" style={{width:"100%", justifyContent:"center", marginTop:10, color:"rgba(255,255,255,.8)", borderColor:"rgba(255,255,255,.3)", background:"rgba(255,255,255,.1)"}} onClick={() => setUser(null)}>
            {Icon.logout} Keluar
          </button>
        </div>
      </div>

      {/* Main */}
      <div className="main">
        <div className="topbar">
          <h2>{pageTitle[page]}</h2>
          <div style={{position:"relative"}}>
            <button className="btn btn-outline btn-icon" style={{position:"relative"}} onClick={()=>{setShowNotif(v=>!v);setNotifRead(NOTIFS.map(n=>n.id));}}>
              {Icon.bell}
              {unreadCount > 0 && <span className="notif-dot"/>}
            </button>
            {showNotif && (
              <div className="notif-panel">
                <div style={{padding:"12px 16px", borderBottom:"1px solid #f3f0ff", fontWeight:700, color:"#3b2080", fontSize:14}}>Notifikasi</div>
                {NOTIFS.map(n => (
                  <div key={n.id} className={`notif-item${n.unread?" unread":""}`}>
                    <div className="notif-title">{n.title}</div>
                    <div className="notif-msg">{n.msg}</div>
                    <div className="notif-time">{n.time}</div>
                  </div>
                ))}
              </div>
            )}
          </div>
          <div style={{fontSize:13, color:"#888"}}>
            Selamat datang, <b style={{color:"#6741d9"}}>{user.name.split(" ")[0]}</b>
          </div>
        </div>

        <div className="content" onClick={()=>showNotif&&setShowNotif(false)}>
          {page==="dashboard" && <Dashboard anggota={anggota} kegiatan={kegiatan} absensi={absensi} prestasi={prestasi} user={user} />}
          {page==="anggota" && <AnggotaPage anggota={anggota} setAnggota={setAnggota} isAdmin={isAdmin} setToasts={setToasts} />}
          {page==="kegiatan" && <KegiatanPage kegiatan={kegiatan} setKegiatan={setKegiatan} anggota={anggota} absensi={absensi} setAbsensi={setAbsensi} isAdmin={isAdmin} setToasts={setToasts} user={user} />}
          {page==="prestasi" && <PrestasiPage prestasi={prestasi} setPrestasi={setPrestasi} anggota={anggota} isAdmin={isAdmin} setToasts={setToasts} />}
          {page==="laporan" && <LaporanPage anggota={anggota} kegiatan={kegiatan} absensi={absensi} prestasi={prestasi} setToasts={setToasts} />}
          {page==="arsitektur" && <ArsitekturPage />}
        </div>
      </div>

      <Toasts toasts={toasts} />
    </div>
  );
}
