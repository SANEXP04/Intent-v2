# App-Intent-V2
Nama &nbsp; &nbsp;: Ihsan Hadimulya<br>
NIM&nbsp; &nbsp; &nbsp; : 312210047<br>
Kelas&ensp; &nbsp; : TI.22.A1<br>
Dosen &nbsp; : Donny Maulana, S.Kom., M.M.S.I.<br><br>
*Aplikasi intent versi kedua, dengan perubahan tombol text menjadi ICON*

## Perintah Tugas
Buatlah tampilan menu Versi 02 dari project-project yang sudah dibuat sebelumnya

dengan tampilan sebagai berikut :<br>
<img width="342" alt="Launcher_logo_versi-02" src="https://github.com/DYRHEEEN/App-Intent-V2/assets/151630441/288fc6f5-86ac-46fd-a894-7439ee08a00a">

## Tahapan Pengerjaan
- Yang pertama, buat dulu sebuah drawable resource file. Saya beri nama file nya *backgroundicon.xml*, dengan root elementnya adalah shape.<br>
  ![ezgif com-video-to-gif (1)](https://github.com/DYRHEEEN/App-Intent-V2/assets/151630441/3666be86-98c9-4cd2-97bf-39fbb2d651fc)<br>
  - Didalam backgroundicon.xml kita tambahkan code berikut:<br>
  ```
  <?xml version="1.0" encoding="utf-8"?>
  <shape xmlns:android="http://schemas.android.com/apk/res/android">
    <solid android:color="@color/colorPrimaryDark"/>
    <corners android:radius="80dp"/>
    <size android:width="80dp" android:height="80dp"/>
  </shape>
  ```
  > Untuk warna dan ukuran kalian bisa sesuaikan dengan keinginan masing-masing.<br>
  
- Untuk icon, kita bisa menggunakan icon yang kita punya, atau jika ingin lebih mudah kita bisa pakai icon yang sudah disediakan oleh android studio. Disini, Saya menggunakan icon yang sudah ada di android studio. Caranya adalah dengan menambah vector asset pada drawable file.<br>
  ![ezgif com-video-to-gif (2)](https://github.com/DYRHEEEN/App-Intent-V2/assets/151630441/3dc5df9e-3570-4fc5-b41b-41fab5aaa60e)<br>
  > Sesuaikan nama, ukuran, dan warnanya. Dengan kebutuhan nya.<br>

- Jika semua hal diatas sudah selesai, selanjutnya kita akan edit acitivy_main.xml nya, untuk mengganti tombol yang awal nya button menjadi image button, yang bertujuan untuk merubah dari tombol teks menjadi icon. Disini kita diharuskan menghapus terlebih dulu semua button *kecuali imageview untuk background*, namun lebih baik salin code button sebelumnya karena akan dipakai lagi nantinya. Langsung saja, masuk ke tahap pengeditan.
  - Pertama, kita tambahkan dulu linear layout dengan orientasi vertical untuk dasar dari penempatan tombol.
    ```
    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:orientation="vertical"
        android:gravity="center_horizontal">
    
    </LinearLayout>
    ```
  - Kedua, didalam LinearLayout vertical ini. Kita tambahkan lagi LinearLayout, tetapi dengan orentasi horizontal agar tombol berjejer kesamping.
    ```
    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:orientation="vertical"
        android:gravity="center_horizontal">

        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:orientation="horizontal"
            android:gravity="center">

        </LinearLayout>
    </LinearLayout>
    ```
  - Ketiga, disini kita tambahkan terlebih hanya sebanyak tiga button, agar buttonnya sesuai dengan apa yang diperintahkan, yaitu tiga buah berjajar kesamping.
    ```
    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:orientation="vertical"
        android:gravity="center_horizontal">

        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:orientation="horizontal"
            android:gravity="center">

            <ImageButton
                android:id="@+id/btnHelloWorld"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_margin="20dp"
                android:background="@drawable/backgroundicon"
                android:onClick="btnHelloWorld"
                android:src="@drawable/icon_hello"
                tools:ignore="UsingOnClickInXml,SpeakableTextPresentCheck" />

            <ImageButton
                android:id="@+id/btnProjectCount"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_margin="20dp"
                android:background="@drawable/backgroundicon"
                android:onClick="btnCount"
                android:src="@drawable/icon_count"
                tools:ignore="UsingOnClickInXml,SpeakableTextPresentCheck" />

            <ImageButton
                android:id="@+id/btnProjectSianida"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_margin="20dp"
                android:background="@drawable/backgroundicon"
                android:onClick="btnSianida"
                android:src="@drawable/icon_sianida"
                tools:ignore="UsingOnClickInXml,SpeakableTextPresentCheck" />
    
        </LinearLayout>
    </LinearLayout>
    ```
    > Tujuan salin code tadi ada disini, jadi kita tidak serta merta menghapus code lalu membuat ulang, tapi hanya mengeditnya saja menjadi ImageButton.
    > Masukkan juga background dan icon yang sudah kita buat dan tambahkan tadi, pada setiap buttonnya.<br>
    
  - Terakhir, kita tambahkan lagi sebuah LinearLayout Horizontal, untuk tombol yang tersisa.
    ```
    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:orientation="vertical"
        android:gravity="center_horizontal">

        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:orientation="horizontal"
            android:gravity="center">

            <ImageButton
                android:id="@+id/btnHelloWorld"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_margin="20dp"
                android:background="@drawable/backgroundicon"
                android:onClick="btnHelloWorld"
                android:src="@drawable/icon_hello"
                tools:ignore="UsingOnClickInXml,SpeakableTextPresentCheck" />

            <ImageButton
                android:id="@+id/btnProjectCount"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_margin="20dp"
                android:background="@drawable/backgroundicon"
                android:onClick="btnCount"
                android:src="@drawable/icon_count"
                tools:ignore="UsingOnClickInXml,SpeakableTextPresentCheck" />

            <ImageButton
                android:id="@+id/btnProjectSianida"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_margin="20dp"
                android:background="@drawable/backgroundicon"
                android:onClick="btnSianida"
                android:src="@drawable/icon_sianida"
                tools:ignore="UsingOnClickInXml,SpeakableTextPresentCheck" />
        </LinearLayout>

        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:orientation="horizontal"
            android:gravity="center">

            <ImageButton
                android:id="@+id/btnTwoActivity"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_margin="20dp"
                android:background="@drawable/backgroundicon"
                android:onClick="btnTwoActivity"
                android:src="@drawable/icon_twoact"
                tools:ignore="UsingOnClickInXml, SpeakableTextPresentCheck" />

            <ImageButton
                android:id="@+id/btnSetAlarm"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_margin="20dp"
                android:background="@drawable/backgroundicon"
                android:onClick="btnSetAlarm"
                android:src="@drawable/icon_alarm"
                tools:ignore="UsingOnClickInXml,SpeakableTextPresentCheck" />

            <ImageButton
                android:id="@+id/btnshowMap"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_margin="20dp"
                android:background="@drawable/backgroundicon"
                android:onClick="btnshowMap"
                android:src="@drawable/icon_maps"
                tools:ignore="UsingOnClickInXml,SpeakableTextPresentCheck" />
        </LinearLayout>
    </LinearLayout>
    ```
    > Saya menambahkan sebuah button baru, yaitu button untuk membuka maps.
    
  - Dengan semua ini, kita akan mendapatkan tampilan desain seperti ini :<br>
    <img width="342" alt="Launcher_logo_versi-02" src="https://github.com/SANEXP04/Intent-v2/assets/115678077/fa5aabae-81b1-4d30-8799-36416d231c19">

- Tampilan desain activity_main.xml sudah selesai, saatnya kita mengedit MainActivity.java. Dan juga, karena kemarin diperintahkan untuk membuat tombol untuk membuka maps, maka disini Saya tambahkan lagi code implicit intent untuk membuka mapsnya. Tambahkan code berikut dibawah setContentView :
  ```
  ImageButton btnshowMap = findViewById(R.id.btnshowMap);
        btnshowMap.setOnClickListener(v -> {
            Intent map = new Intent(Intent.ACTION_VIEW, Uri.parse("geo:-6.324307,107.169273"));
            map.setPackage("com.google.android.apps.maps");
            startActivity(map);
        });
  ```
- Selesai, semua code sudah berhasil ditambah dan diedit.

## Hasil RUN
https://github.com/SANEXP04/Intent-v2/assets/115678077/cd559c01-802f-4e14-b6da-ae1d69aad30f
