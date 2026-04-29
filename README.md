📊 Analisis Data Penjualan & Efektivitas Iklan
Business Question
Analisis ini dilakukan untuk memahami performa penjualan dan perilaku pelanggan. Beberapa pertanyaan utama yang ingin dijawab:
- Siapa pelanggan terbaik berdasarkan pola transaksi?
- Apakah anggaran iklan berpengaruh terhadap penjualan?
- Kategori produk mana yang paling efisien?
- Produk mana yang memiliki performa rendah?

Data Wrangling
Data diolah dari file penjualan yang berisi informasi transaksi, produk, dan anggaran iklan.
Beberapa proses yang dilakukan:
- Mengubah kolom Order_Date ke format datetime
- Membuat kolom Total_Sales dari Quantity × Price_Per_Unit
- Membagi data menjadi dua kelompok:
       Iklan tinggi dan rendah berdasarkan median Ad_Budget
- Melakukan analisis RFM (Recency, Frequency, Monetary) untuk segmentasi pelanggan
- Menghitung efisiensi kategori produk dengan rasio:
       Efficiency = Total Sales / Ad Budget

Insights
📌 Pengaruh Anggaran Iklan terhadap Penjualan

Rata-rata penjualan antara kelompok iklan tinggi dan rendah tidak menunjukkan perbedaan yang signifikan. Selisihnya sangat kecil, sehingga dapat disimpulkan bahwa peningkatan anggaran iklan tidak secara langsung meningkatkan penjualan.
<img width="856" height="556" alt="download" src="https://github.com/user-attachments/assets/a3ee0547-3540-4dd0-8d48-791c1239dcf4" />

📌 Efisiensi Kategori Produk

Kategori Fashion memiliki efisiensi tertinggi, menunjukkan bahwa biaya iklan yang dikeluarkan menghasilkan penjualan yang optimal. Sebaliknya, Home Decor memiliki efisiensi paling rendah sehingga kurang efektif dalam penggunaan budget.
<img width="927" height="556" alt="download (1)" src="https://github.com/user-attachments/assets/87590138-dba6-476d-b02d-96cacac8a87e" />

📌 Distribusi RFM Pelanggan

Sebagian besar pelanggan memiliki frekuensi pembelian rendah dan nilai transaksi yang kecil. Hanya sedikit pelanggan yang tergolong aktif dan memberikan kontribusi besar terhadap total penjualan.
<img width="701" height="532" alt="download (2)" src="https://github.com/user-attachments/assets/a0c6f670-a593-41c3-95b2-296ed7e5f66b" />




