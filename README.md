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