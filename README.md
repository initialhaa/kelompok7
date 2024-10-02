# kelompok7


// Misalkan kita membaca file JSON menggunakan Node.js

const fs = require('fs');

// Membaca file data1.json
const jsonData1 = fs.readFileSync('data1.json', 'utf-8');

// Membaca file data2.json
const jsonData2 = fs.readFileSync('data2.json', 'utf-8');

// Mengonversi JSON string menjadi objek JavaScript
const obj1 = JSON.parse(jsonData1);
const obj2 = JSON.parse(jsonData2);

// Menggabungkan kedua objek
const mergedData = { ...obj1, ...obj2 };

// Mengonversi kembali ke format JSON
const jsonString = JSON.stringify(mergedData, null, 2);

// Menyimpan hasil ke file baru
fs.writeFileSync('mergedData.json', jsonString);

console.log('Data berhasil digabungkan ke mergedData.json');
