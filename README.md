## Nama      : Muhammad Reza Khatami
## Kelas     : TI - 3C
## No. Absen : 13

BIG DATA - Chapter 3

## Hasil

## Accumulator

![1](https://user-images.githubusercontent.com/90266254/227842358-482ab5cd-7c28-4fc1-be4c-9357745336f8.png)

- SparkContext, disingkat menjadi "sc", adalah objek utama yang digunakan dalam pemrograman dengan Apache Spark. Dengan menggunakan SparkContext, kita dapat menginisialisasi aplikasi Spark dan membuat RDD (Resilient Distributed Datasets) yang mendukung komputasi paralel.

- Accumulator adalah objek shared variable yang digunakan dalam Apache Spark untuk mengumpulkan nilai secara asinkron dari beberapa executor (pekerja) di sepanjang sebuah job (tugas). Objek ini biasanya digunakan untuk menghitung statistik yang kompleks atau mengakumulasikan hasil dalam loop.

- Parallelize adalah sebuah method yang digunakan pada objek SparkContext untuk membuat RDD dari koleksi data yang ada dalam program. RDD ini akan didistribusikan secara paralel pada executor (pekerja) yang tersedia.

- Lambda adalah sebuah fungsi anonim yang sering digunakan dalam pemrograman fungsional dan pemrograman paralel. Fungsi ini biasanya digunakan untuk melakukan operasi yang sederhana dan terbatas pada sebuah data, sehingga sangat cocok untuk dijalankan di dalam RDD.

- Value adalah nilai dari suatu variabel bisa berupa Integer, String, DLL

## Broadcast

![2](https://user-images.githubusercontent.com/90266254/227842394-11c94df8-1cb3-4898-9bd1-e48824722f2a.png)

- Broadcast adalah sebuah fungsi dalam Spark yang memungkinkan pengguna untuk mendistribusikan variabel secara efisien ke setiap node dalam sebuah cluster. Dengan menggunakan broadcast, setiap node dapat mengakses variabel tersebut dengan cepat tanpa perlu menyalinnya berkali-kali.

- List adalah tipe data yang umum digunakan dalam bahasa pemrograman Python untuk menyimpan sejumlah nilai dalam satu variabel. List dapat berisi elemen-elemen dengan tipe data yang berbeda, dan dapat diakses menggunakan indeks. List ini sangat berguna dalam berbagai macam aplikasi dan dapat dimanipulasi dengan mudah menggunakan fungsi-fungsi built-in di Python.

- Range adalah sebuah fungsi dalam bahasa pemrograman Python yang digunakan untuk menghasilkan deret bilangan bulat secara berurutan. Fungsi ini dapat diberikan argumen untuk memulai, mengakhiri, dan menentukan langkah antar bilangan. Deret bilangan ini sering digunakan dalam skenario pemrograman seperti pengulangan for-loop, dan sangat efisien untuk digunakan dalam program yang membutuhkan kumpulan bilangan bulat berurutan.

## PairRDD

![pairRDD](https://user-images.githubusercontent.com/90266254/227842484-004bcf52-09e3-4c3c-9126-f393610c1d28.png)

- map: map adalah sebuah fungsi dalam Spark yang digunakan untuk melakukan transformasi pada setiap elemen dalam RDD dengan menggunakan sebuah fungsi yang diberikan sebagai argumen. Fungsi ini mengembalikan RDD baru yang berisi hasil transformasi tersebut.

- collect: collect adalah sebuah fungsi dalam Spark yang digunakan untuk mengambil semua elemen dalam sebuah RDD dan mengembalikan hasilnya sebagai list pada driver program. Fungsi ini tidak disarankan digunakan pada RDD yang sangat besar, karena dapat mengakibatkan out-of-memory error.

- len: len adalah sebuah fungsi dalam bahasa pemrograman Python yang digunakan untuk menghitung jumlah elemen dalam sebuah list atau tipe data lain yang dapat dihitung panjangnya.

- keys: keys adalah sebuah metode pada tipe data dictionary dalam bahasa pemrograman Python yang mengembalikan sebuah list yang berisi semua kunci (keys) dalam dictionary tersebut.

- values: values adalah sebuah metode pada tipe data dictionary dalam bahasa pemrograman Python yang mengembalikan sebuah list yang berisi semua nilai (values) dalam dictionary tersebut.

## SystemCommandsOutput

![7(1)](https://user-images.githubusercontent.com/90266254/227845150-f2f9b23f-c292-4286-8e61-7a29f45ba00d.png)

## SystemCommandsReturnCode

![8](https://user-images.githubusercontent.com/90266254/227845209-4af17b33-734b-4841-9921-a7b9b2d0ce68.png)

## UnderstandingRDDs

![RDDs(5)](https://user-images.githubusercontent.com/90266254/227842627-1818c5f5-f81e-49f0-82c9-caf87277f704.png)

- defaultParallelism: defaultParallelism adalah sebuah atribut dalam Spark yang menentukan jumlah partisi yang digunakan secara default saat membuat RDD baru. Nilai defaultnya adalah jumlah core yang tersedia di cluster.

- getNumPartitions: getNumPartitions adalah sebuah metode dalam Spark yang digunakan untuk mengambil jumlah partisi dalam sebuah RDD.

- mapPartitionsWithIndex: mapPartitionsWithIndex adalah sebuah fungsi dalam Spark yang mirip dengan fungsi map, namun berbeda dalam cara penggunaannya. Fungsi ini memungkinkan pengguna untuk mengakses indeks partisi RDD saat melakukan transformasi pada setiap partisinya.

- repartition: repartition adalah sebuah fungsi dalam Spark yang digunakan untuk mengubah jumlah partisi sebuah RDD menjadi jumlah yang diinginkan. Fungsi ini dapat menyebabkan pengiriman data melintasi jaringan dan dapat memakan waktu yang lama.

- coalesce: coalesce adalah sebuah fungsi dalam Spark yang digunakan untuk menggabungkan beberapa partisi dalam sebuah RDD menjadi satu partisi. Fungsi ini lebih efisien daripada repartition, karena tidak menyebabkan pengiriman data melintasi jaringan.

- toDebugString: toDebugString adalah sebuah metode dalam Spark yang digunakan untuk mengambil string representasi dari RDD yang berisi informasi tentang partisi-partisi dalam RDD, lokasi masing-masing partisi, dan transformasi yang telah dilakukan pada RDD tersebut.

## WordCount

![6](https://user-images.githubusercontent.com/90266254/227842680-1a3d104a-ac67-4b3c-95e6-2b79147a4b6a.png)

- flatMap: flatMap adalah sebuah fungsi dalam Spark yang mirip dengan fungsi map, namun berbeda dalam cara penggunaannya. Fungsi ini digunakan untuk menghasilkan nol atau lebih elemen dari setiap elemen dalam RDD yang diberikan sebagai argumen. Fungsi ini mengembalikan RDD baru yang berisi semua elemen yang dihasilkan.

- reduceByKey: reduceByKey adalah sebuah fungsi dalam Spark yang digunakan untuk menghitung agregasi nilai pada tiap kunci (key) dalam sebuah RDD. Fungsi ini mengelompokkan elemen berdasarkan kunci yang sama, dan menggabungkan nilai-nilai untuk setiap kunci menggunakan sebuah fungsi agregasi tertentu. Hasilnya adalah RDD baru yang berisi setiap kunci dengan nilai agregasi yang sesuai.

- split: split adalah sebuah fungsi dalam bahasa pemrograman Python yang digunakan untuk membagi sebuah string menjadi beberapa substring berdasarkan sebuah karakter pemisah (separator). Fungsi ini mengembalikan sebuah list dari substring-substring tersebut.


