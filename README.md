# Cara menggunakan / membuat bot whatsapp dari client ini

> Sebelumnya, module dari @adiwajshing/Balieys telah dihapus, namun kita dapat menggunakannya [@whiskeysocket/baileys](https://github.com/WhiskeySockets/Baileys)

## 📍 Informasi

Sebelumnya, kamu harus menginstall beberapa package / aplikasi seperti nodejs, selain itu kamu dapat gunakan yarn sebagai ganti npm untuk menginstall module

## 🍃 Tahap instalasi

Buat folder untuk menjadi tempat project kamu

```bash
mkdir your-whatsapp-bot
cd your-whatsapp-bot
```

Lalu kamu gunakan perintah dibawah ini untuk menginstall modules

```bash
# Jika Kamu Menggunakan NPM
npm i @whiskeysockets/baileys qrcode-terminal
```

```bash
# Jika kamu Menggunakan Yarn
yarn add @whiskeysockets/baileys qrcode-terminal
```

Jika kamu sudah menginstall modulenya, sekarang kamu install client untuk menjadi lebih mudah dalam membuat bot.

> Install wget dan unzip terlebih dahulu untuk memudahkan mengunduh file zip client yang ingin kita inginkan

```bash
# Unduh file zip client
wget https://github.com/ernestoyoofi/mzea-wa-client.public/raw/main/wa-mzea-client.zip
# Buka file zip ke folder
unzip wa-mzea-client.zip
# Hapus file zip client
rm -rf wa-mzea-client.zip
```

## ⚒️ Cara penggunaanya

Pertama tama kamu masukan setup socketnya terlebih dahulu

```js
// Buat file main.js
const { WhatsAppSetup } = require("./wa/main")

// Setup Class Function
const wa = new WhatsAppSetup()

// Ini Setup Agar Dapat Berjalan
wa.start_run()

wa.on("call", async (e) => {
  // Panggilan Suara / Video
})
wa.on("message", async (e) => {
  // Pesan masuk / notifikasi
})
wa.on("groups.participants", (e) => {
  // Member masuk / keluar dari grup
})
wa.on("groups", (e) => {
  // Grup update
})
```
