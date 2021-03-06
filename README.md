# CockroachDB

CockhroachDB adalah database SQL terdistribusi yang di desain untuk skalabilitas, konsistensi, dan survivabilitas yang kuat.

### Skalabilitas

1. CockroachDB dapat menambahkan lebih banyak node untuk meningkatkan kapasitas cluster dengan jumlah penyimpanan pada setiap node.
2. Query dapat dikirim ke node manapun di cluster, dan query dapat
   beroperasi secara independent (w/o conflicts). Yang berarti bahwa
   keseluruhan throughput adalah faktor linier dari jumlah node dalam
   cluster.
3. SQL Distributed, query dapat di distribusikan sehingga keseluruhan
   throughput query tunggal dapat ditingkatkan dengan menambahkan node
   lebih banyak node.
   
### Konsistensi

1. menggunakan distributed consensus protocol untuk replikasi data sinkron
   dalam setiap key value range. Dan menggunakan aligoritma Raft
   consensus algorithm.
2. CockroachDB menggunakan distributed commit protocol non-locking
   yang efisien

### Survivabilitas

Beberapa replika dapat digabungkan dalam satu data center untuk replikasi latensi rendah



### Menjalankan CockroachDB di  Local Cluster (Insecure)

menjalankan CockroachDB
<img src="https://github.com/nauticas/CockroachDB/blob/master/img/run.png" width="70%">

##### 1. Menjalankan node pertama

<img src="https://github.com/nauticas/CockroachDB/blob/master/img/st1.png">

perintah ini untuk membuat node pada mode tidak aman

##### 2. menambahkan node kedua dan ketiga pada cluster

<img src="https://github.com/nauticas/CockroachDB/blob/master/img/st2.png">

buka terminal baru kemudian buat node ke 3:
<img src="https://github.com/nauticas/CockroachDB/blob/master/img/st22.png">

untuk menghubungkan antar node maka dibutuhkan parameter --join 

##### 3. Uji cluster dengan membuat databse dan tabel kemudian memasukan data

<img src="https://github.com/nauticas/CockroachDB/blob/master/img/st3.png"> 

<img src="https://github.com/nauticas/CockroachDB/blob/master/img/st33.png">


##### Memamntau cluster

Akses UI Admin untuk custer dengan membuka browser pada alamat `http://localhost:8080`

<img src="https://github.com/nauticas/CockroachDB/blob/master/img/st4.png">
