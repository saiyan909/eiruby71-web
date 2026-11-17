# Panduan Publish Web Eiruby71 Tanpa Server Sendiri

Halo! Karena kamu sudah terbiasa koding, konsep publish web modern tanpa server fisik sendiri (Serverless / Static Hosting) ini dijamin bakal terasa jauh lebih simpel dibanding setup server kantor (tanpa perlu repot Nginx, Docker, SSH, firewall, atau maintain VM).

File website ini bersifat **Static Site** (HTML, CSS Tailwind CDN, JS) yang super cepat, ringan, dan aman.

Berikut 3 cara termudah untuk publish ke publik **100% GRATIS**:

---

## Cara 1: Netlify Drop (Paling Instan — 30 Detik Tanpa Terminal)

1. Buka browser dan login/daftar di [app.netlify.com](https://app.netlify.com/).
2. Buka tab **Sites**, lalu cari area **"Drag and drop your site folder here"** (atau langsung ke [app.netlify.com/drop](https://app.netlify.com/drop)).
3. Tarik folder `eiruby71-web` ini langsung dari file explorer laptop kamu ke browser.
4. Selesai! Netlify langsung generate link publik (contoh: `https://brave-motor-123.netlify.app`).
5. Kamu bisa masuk ke **Site configuration** -> **Change site name** menjadi `eiruby71.netlify.app`.

---

## Cara 2: GitHub Pages (Standar Developer)

Jika kamu biasa menggunakan Git & GitHub:

1. Buat repository baru di GitHub (misal: `eiruby71`).
2. Di laptop kamu, inisialisasi git dan push:
   ```bash
   cd eiruby71-web
   git init
   git add .
   git commit -m "feat: initial landing page Eiruby71"
   git branch -M main
   git remote add origin https://github.com/USERNAME-KAMU/eiruby71.git
   git push -u origin main
   ```
3. Buka repo GitHub kamu -> **Settings** -> **Pages**.
4. Di bagian **Build and deployment**, pilih branch `main` dan folder `/ (root)`, lalu klik **Save**.
5. Tunggu 1 menit, web kamu sudah live di:
   `https://USERNAME-KAMU.github.io/eiruby71`

---

## Cara 3: Vercel (Paling Populer di Kalangan Web Dev)

Jika kamu punya Node.js di laptop:
```bash
cd eiruby71-web
npx vercel
```
Ikuti prompt di terminal (tinggal tekan Enter untuk default). Dalam 15 detik web langsung live di `https://eiruby71.vercel.app`.

---

## Mau Pakai Domain Sendiri? (Misal: `eiruby71.com`)

Kalau nanti om kamu mau alamatnya terlihat lebih profesional:
1. Beli domain di penyedia lokal (seperti Niagahoster, Domainesia, Rumahweb) seharga ~Rp 130.000 - 150.000 per tahun.
2. Di dashboard Netlify / Vercel / GitHub Pages, buka menu **Custom Domains** dan masukkan `eiruby71.com`.
3. Tambahkan DNS Record (CNAME / A Record) sesuai instruksi yang ditampilkan.
4. **SSL (HTTPS)** akan otomatis dibuatkan gratis (via Let's Encrypt).
5. Kamu tetap **Rp 0** untuk biaya server/hosting selamanya!

