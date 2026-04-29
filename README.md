📊 Laporan Praktikum Data Analysis (RFM & Sales Analysis)

🧠 Business Question

- Analisis ini bertujuan untuk menjawab beberapa pertanyaan bisnis utama:
- Siapa pelanggan terbaik berdasarkan perilaku pembelian (RFM)?
- Faktor apa yang paling mempengaruhi total penjualan?
- Bagaimana tren penjualan setiap bulan?
- Apakah harga (UnitPrice) berpengaruh terhadap total penjualan?

🧹 Data Wrangling

Beberapa proses pembersihan dan transformasi data yang dilakukan:
- Mengubah kolom InvoiceDate menjadi format datetime
- Membuat kolom baru:

month → untuk analisis bulanan
total_sales → hasil dari:
total_sales = Quantity × UnitPrice
Menghapus/menghindari nilai kosong (missing value)
- Melakukan agregasi data:
     Penjualan per bulan
     Penjualan per customer (RFM)
- Membuat fitur RFM:
     Recency → terakhir belanja
     Frequency → jumlah transaksi
     Monetary → total pengeluaran
- Scoring RFM menggunakan pd.qcut menjadi 1–5

📊 Insights
1. Korelasi Antar Variabel

Dari heatmap:
Quantity vs Total Sales → 0.89 (Sangat kuat positif)
👉 Artinya semakin banyak barang dibeli, semakin tinggi penjualan
UnitPrice vs Total Sales → -0.16 (Lemah negatif)
👉 Harga tidak terlalu berpengaruh besar ke total penjualan
Quantity vs UnitPrice → hampir 0
👉 Jumlah beli tidak dipengaruhi harga secara signifikan

📌 Kesimpulan:
Penjualan lebih dipengaruhi oleh jumlah barang yang dibeli dibanding harga.

2. Tren Penjualan Bulanan
- Penjualan cenderung stabil di awal tahun
- Terjadi kenaikan signifikan di bulan September–November
- Puncak penjualan terjadi di November
- Penurunan drastis di Desember (kemungkinan data belum lengkap)

📌 Kesimpulan:
Ada pola musiman (seasonality), kemungkinan karena event akhir tahun / promo.

3. Analisis RFM (Customer Behavior)
- Customer dengan:
       Recency kecil → baru belanja → lebih bernilai
       Frequency tinggi → sering beli → loyal
       Monetary tinggi → banyak belanja → high value
- Digabung menjadi RFM Score (contoh: 555 = pelanggan terbaik)

📌 Kesimpulan:
Perusahaan bisa mengelompokkan customer:
- VIP / loyal customer
- Customer biasa
- Customer yang sudah tidak aktif

🚀 Recommendation

Berdasarkan analisis:

1. Fokus ke Quantity (Jumlah Pembelian)
- Buat promo seperti:
     "Beli 2 gratis 1"
      Diskon pembelian banyak
- Karena quantity paling berpengaruh ke sales

2. Manfaatkan Momentum Bulan Tinggi
- Maksimalkan penjualan di:
       September – November
- Strategi:
       Campaign besar
       Flash sale
Promo akhir tahun

3. Segmentasi Customer (RFM)
- Targetkan:
      High RFM → kasih reward / loyalty program
      Low RFM → re-engagement (diskon, email marketing)

4. Harga Bukan Faktor Utama
- Tidak perlu terlalu fokus menurunkan harga
- Lebih baik:
        Tingkatkan bundling produk
        Tambahkan value (bonus, paket hemat)

📌 Kesimpulan Akhir
- Faktor utama penjualan adalah jumlah barang (Quantity)
- Ada pola musiman dalam penjualan
- RFM efektif untuk mengidentifikasi pelanggan terbaik
- Strategi bisnis harus fokus pada:
        meningkatkan volume pembelian
        mempertahankan pelanggan loyal
