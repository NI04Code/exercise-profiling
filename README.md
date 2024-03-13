<h1>Screenshots</h1> 

## Before Optimization Result
### Before Optimization
`Summary of 3 method`
![Results Table /summary](https://cdn.discordapp.com/attachments/804005958534823978/1217425797296558090/Screen_Shot_2024-03-13_at_12.14.39_AM.png?ex=6603fb20&is=65f18620&hm=e521dc27605436f0ce3b31dc969025d72e46b8fcf56d375fd991b562b72e995a&)

### Semi Optimize
`/all-student`
![Results Table /all-student](https://cdn.discordapp.com/attachments/804005958534823978/1217421276117995520/Screen_Shot_2024-03-13_at_11.43.03_AM.png?ex=6603f6ea&is=65f181ea&hm=5152e9244b609607bedb88da1aa854453170d22e0a09862c23e9e095b51dee85&)
----------
`/all-student-name`
![Results Table /all-student-name](https://cdn.discordapp.com/attachments/804005958534823978/1217421276965109830/Screen_Shot_2024-03-13_at_11.43.17_AM.png?ex=6603f6eb&is=65f181eb&hm=e5fe88552f0a74319d53cb51538588e84e8d43acce4f083c781ce0439f19d846&)

----------
`/highest-gpa`
![Results Table /highest-gpa](https://cdn.discordapp.com/attachments/804005958534823978/1217421277287940126/Screen_Shot_2024-03-13_at_11.43.57_AM.png?ex=6603f6eb&is=65f181eb&hm=a45625c67be5f6bcde7c0fcffc0d96fc941793168dfb7e25af98017f5e4619e4&)

----------
`jtl-files`
![Results Table /jtl file](https://cdn.discordapp.com/attachments/804005958534823978/1217421290445733958/Screen_Shot_2024-03-13_at_3.45.06_PM.png?ex=6603f6ee&is=65f181ee&hm=bef33e7ef1c8767ba4a65acc5ac780a249f2f0745091fa5d07336f656cc70ce1&)
----------
## After Optimization Result

`/all-student`
![Results After Optimization /all-student](https://cdn.discordapp.com/attachments/804005958534823978/1217421277548253266/Screen_Shot_2024-03-13_at_11.51.49_AM.png?ex=6603f6eb&is=65f181eb&hm=0607900997aa83c67fa1cb358b1353c89e5b04f124495a19238ec61dd74edeb3&)
#### Saya berhasil mereduce waktu eksekusi program sekitar ~50-60% 

----------
`/all-student-name`
![Results After Optimization /all-student-name](https://cdn.discordapp.com/attachments/804005958534823978/1217421277799776346/Screen_Shot_2024-03-13_at_11.52.03_AM.png?ex=6603f6eb&is=65f181eb&hm=45a8056599619cd42ab102364fa9a45aa43cc05633b389a739404b29c051b1e8&)
#### Saya berhasil mereduce waktu eksekusi program sekitar ~20%

----------
`highest-gpa`
![Results After Optimization /highest-gpa](https://cdn.discordapp.com/attachments/804005958534823978/1217421278143844382/Screen_Shot_2024-03-13_at_11.52.19_AM.png?ex=6603f6eb&is=65f181eb&hm=3c42df6cc776951af2a5e1f217a592ca179e31410d31c9e868a41fd81ddefcbf&)
#### Saya berhasil mereduce waktu eksekusi program sekitar ~30-40%

----------
`jtl-files`
![Results Table /jtl file](https://cdn.discordapp.com/attachments/804005958534823978/1217421290860974130/Screen_Shot_2024-03-13_at_12.03.07_PM.png?ex=6603f6ee&is=65f181ee&hm=71cecaecbc8979223020084e442d2bbef872d7c1bb78bd2108768d52876e11e8&)

## Analisis Before & After Optimize
Dapat dilihat bahwa setelah dioptimize performance testing yang dilakukan oleh jmeter semakin cepat, tidak hanya itu saat sebelum optimize beberapa dari status pada sample saya memiliki status: warning, namun setelah dioptimie semua sample memiliki status success. Optimisasi yang paling signifikan terjadi pada `/all-student` dapat dilihat dalam jti sebelum optimizte latency mencapai 26000an dan setelah optimize berhasil turun ke 7000an.

<h1>Reflection</h1>

### 1. What is the difference between the approach of performance testing with JMeter and profiling with IntelliJ Profiler in the context of optimizing application performance?
JMeter dapat berguna jika kita ingin menguji kinerja keseluruhan aplikasi kita, sementara Profiler IntelliJ dapat berguna untuk menganalisis detail kinerja aplikasi dengan fokus pada kode yang memakan waktu paling banyak.

### 2. How does the profiling process help you in identifying and understanding the weak points in your application?
Melalui proses profiler yang mengidentifikasi method yang memakan waktu paling banyak untuk dieksekusi, kita dapat mengidentifikasi bagian dari kode aplikasi yang perlu dioptimalkan atau direfactor.

### 3. Do you think IntelliJ Profiler is effective in assisting you to analyze and identify bottlenecks in your application code?
Ya, karena kita dapat melihat berapa banyak waktu yang dibutuhkan oleh setiap fungsi atau metode dalam waktu eksekusi keseluruhan aplikasi kita.

### 4. What are the main challenges you face when conducting performance testing and profiling, and how do you overcome these challenges?
Tantangan saya adalah dalam membaca informasi yang disimpulkan oleh jmeter ataupun Intellij Profiler, saya perlu banyak googling untuk mengetahui representasi dari setiap informasi

### 5. What are the main benefits you gain from using IntelliJ Profiler for profiling your application code?
Benefits yang paling terasa adalah kita dapat mengetahui method mana yang paling banyak memakan waktu sehingga kita dapat dengan mudah mengidentifikasi bagian tertentu dari code yang dapat di refactor.

### 6. How do you handle situations where the results from profiling with IntelliJ Profiler are not entirely consistent with findings from performance testing using JMeter?
Perbedaan hasil antara Profiler IntelliJ dan JMeter mungkin disebabkan oleh fakta bahwa Profiler memantau waktu eksekusi secara langsung sedangkan JMeter hanya menguji kinerja keseluruhan aplikasi. Saya rasa dalam menangani hal semacam ini kita bisa melakukan testing beberapa kali untuk memastikan range dari hasil performance testing antara jmeter dan profiler

### 7. What strategies do you implement in optimizing application code after analyzing results from performance testing and profiling? How do you ensure the changes you make do not affect the application's functionality?
Strategi saya dalam melakukan optimisasi adalah dengan menggunakan tools yang lebih cepat seperti string builder, saya juga melakukan akses ke database langsung untuk highest gpa, dan mengurangi for loop yang tidak diperlukan untuk all-student. Saya memastikan optimisasi dari code tidak mengubah fungsionalitas dari aplikasi dengan memastikan logic yang berjalan tetap sama dan mengisolasi tiap tiap perubahan yang saya buat.