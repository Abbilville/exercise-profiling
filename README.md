#### Nama: Abbilhaidar Farras Zulfikar
#### NPM: 2206026012
#### Kelas: Adpro A
---
## Tutorial 5
**Sebelum dioptimasi**
1. all-student request
   ![image](https://github.com/Abbilville/exercise-profiling/assets/119837732/0b1db4d9-8fff-4265-99be-d5a0ba71cea4)
   ![image](https://github.com/Abbilville/exercise-profiling/assets/119837732/a967fc14-be63-4f02-b674-3ef6617f2f2f)
2. all-student-name request
   ![image](https://github.com/Abbilville/exercise-profiling/assets/119837732/f6aa61ee-eac4-4140-9122-3cc3c4b1721f)
   ![image](https://github.com/Abbilville/exercise-profiling/assets/119837732/36e5b9f4-7085-4457-8053-934deddc31ca)
3. highest-gpa request
   ![image](https://github.com/Abbilville/exercise-profiling/assets/119837732/c6900334-7591-4c12-8a10-058f85ab6639)
   ![image](https://github.com/Abbilville/exercise-profiling/assets/119837732/45864a8c-6263-403c-8351-fa1864cc7e0c)

**Sesudah dioptimasi**
1. all-student request
   ![image](https://github.com/Abbilville/exercise-profiling/assets/119837732/1632820a-b9f9-4c56-a30e-1890ddac42cc)
   ![image](https://github.com/Abbilville/exercise-profiling/assets/119837732/ba3e993a-ba82-461f-9fca-d55d2dc83cb5)
2. all-student-name request
   ![image](https://github.com/Abbilville/exercise-profiling/assets/119837732/918696e0-15fa-4f1f-85fd-cb3418c2ca1e)
   ![image](https://github.com/Abbilville/exercise-profiling/assets/119837732/60160994-8c11-4746-902c-75e2a52576e5)
3. highest-gpa request
   ![image](https://github.com/Abbilville/exercise-profiling/assets/119837732/aaf85834-c4d6-4587-9bf7-fe1189731abe)
   ![image](https://github.com/Abbilville/exercise-profiling/assets/119837732/bd5ff4ef-3472-4409-a9dc-05d977f1499c)

Dapat dilihat bahwa sesudah method method yang berhubungan dengan endpoint tersebut dioptimisasi, sample time dan latencynya sangat berkurang drastis. Misalnya saja pada path /all-student sample time dan latency nya mencapai 400k, namun setelah dioptimisasi sample timenya dan latencynya berkurang menjadi 26k saja, yang mana lebih cepat 93,5 persen.

### Refleksi
1. **What is the difference between the approach of performance testing with JMeter and profiling with IntelliJ Profiler in the context of optimizing application performance?** <br>
    JMeter berfokus pada pengukuran performa aplikasi dengan mensimulasikan beban kerja tinggi pada sistem (misalnya, menguji seberapa baik aplikasi menangani banyak pengguna secara bersamaan), sementara IntelliJ Profiler difokuskan pada identifikasi titik-titik lemah yang memengaruhi performa aplikasi secara spesifik.
    
2. **How does the profiling process help you in identifying and understanding the weak points in your application?** <br>
  Proses profiling sangat penting dalam menemukan kelemahan dalam aplikasi yang dapat mempengaruhi performa. Dalam proses ini, profiler mengumpulkan dan menganalisis data untuk mengidentifikasi area yang memperlambat eksekusi aplikasi, seperti penggunaan CPU, alokasi memori, aktivitas pengumpulan sampah (garbage collection), dan konkurensi thread.

3. **Do you think IntelliJ Profiler is effective in assisting you to analyze and identify bottlenecks in your application code?** <br>
IntelliJ Profiler terbukti efektif dalam menemukan kelemahan dalam aplikasi dengan menyediakan visualisasi seperti _flame graph_ yang memperlihatkan area yang memakan waktu eksekusi. Selain itu, informasi tentang waktu eksekusi setiap metode juga disediakan, memungkinkan pengembang untuk melihat dampak dari optimisasi yang dilakukan.

4. **What are the main challenges you face when conducting performance testing and profiling, and how do you overcome these challenges?** <br>
Tantangan yang mungkin dihadapi dalam melakukan pengujian kinerja dan profilisasi termasuk pemahaman yang mendalam terhadap hasil profiling, serta kesulitan dalam melakukan optimisasi kode setelah menemukan kelemahannya. Hal ini membutuhkan pengetahuan mengenai software development yang kuat.

5. **What are the main benefits you gain from using IntelliJ Profiler for profiling your application code?** <br>
Manfaat menggunakan IntelliJ Profiler adalah ketersediaan alat profilisasi yang terintegrasi dalam lingkungan pengembangan IntelliJ IDEA, yang mengurangi kebutuhan akan perangkat lunak tambahan dan menyederhanakan proses pengaturan.

6. **How do you handle situations where the results from profiling with Inte	lliJ Profiler are not entirely consistent with findings from performance testing using JMeter?** <br>
Dalam kasus inkonsistensi antara hasil profilisasi dengan IntelliJ Profiler dan pengujian kinerja menggunakan JMeter, penting untuk memeriksa konfigurasi dan metode pengujian dari kedua alat tersebut. Jika masih terdapat inkonsistensi, korelasi antara data dari kedua alat tersebut perlu dievaluasi lebih lanjut.

7. **What strategies do you implement in optimizing application code after analyzing results from performance testing and profiling? How do you ensure the changes you make do not affect the application's functionality?** <br>
Strategi yang dapat diterapkan dalam optimisasi kode aplikasi termasuk pengurangan pemanggilan database, perbaikan struktur data untuk mengurangi alokasi memori yang tidak perlu, dan optimisasi query untuk meningkatkan efisiensi operasi database. Penting untuk memastikan bahwa perubahan yang dilakukan tidak memengaruhi fungsionalitas aplikasi dengan melakukan pengujian regresi sebelum dan setelah implementasi perubahan.
