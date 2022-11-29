# Nama : Tiara Putri
# NIM : 312210064
# Kelas : TI.22.A1

# Latihan

Buat Dictionary daftar kontak
- Nama sebagai key, dan nomor sebagai value
- Tampilkan kontaknya Ari
- Tambah kontak baru dengan nama Riko, nomor 087654544
- Ubah kontak Dina dengan nomor baru 088999776
- Tampilkan semua Nama
- Tampilkan semua Nomor
- Tampilkan daftar Nama dan nomornya
- Hapus kontak Dina

    
      daftarKontak = {"Nama":"Nomer Telpon"}
      kontak       = {'Ari':'081267888', 'Dina' : '087677776'}

      #print
      print(30*"═")
      print("    Nama    |  Nomor Telepon  ") #prinr daftarkontak
      print(30*"-")
      print("   # Ari    | ", kontak['Ari']) #print kontak Ari
      print("   # Dina   | ", kontak['Dina']) #print kontak Dina
      print(30*"═")

      #Tampilkan kontaknya Ari
      print("Tampilkan kontaknya Ari")
      print("    Ari     | ", kontak['Ari']) #print kontak Ari
      print(30*"═")
      #Tambah kontak baru dengan nama Riko, nomor 087654544
      print("Tambah kontak baru dengan nama Riko, nomor 087654544")
      kontak['Riko'] = '087654544'
      print("    Riko    | ", kontak['Riko'])
      print(30*"═")

      #Ubah kontak Dina dengan nomor baru 088999776
      print("Ubah kontak Dina dengan nomor baru 088999776")
      kontak['Dina'] = '088999776'
      print("    Dina    | ", kontak['Dina'])
      print(30*"═")

      #Tampilkan semua Nama
      print("Tampilkan semua Nama")
      print(kontak.keys())
      print(30*"═")

      #Tampilkan semua Nomor
      print("Tampilkan semua Nomor")
      print(kontak.values())
      print(30*"═")

      #Tampilkan daftar Nama dan nomornya
      print("Tampilkan daftar Nama dan nomornya")
      print(kontak.items())
      print(30*"═")

      #MengHapus kontak Dina
      print("Hapus kontak Dina")
      kontak.pop('Dina')
      print(kontak.items())
      print(30*"═")

![2022-11-28 (5)](https://user-images.githubusercontent.com/115775237/204419952-305ed67a-4c76-442f-9185-4ce6e3532558.png)

# hasil Run

![2022-11-28 (6)](https://user-images.githubusercontent.com/115775237/204420173-a72b6127-c50d-49f5-9513-a9ca53599b41.png)

# Praktikum 5

      print("====================================")
      print("======>  Program Input Nilai  <======")
      print("====================================")
      data = {}
      while True:
          print("")
          m = input("===>> (L)ihat, (T)ambah, (U)bah, (H)apus, (C)ari, (K)eluar : <=== ")
          print("================================================================")
          print("| NO |  Nama     |   Nim    |  Tugas  |  UTS  |  UAS  |   Akir |")
          print("================================================================")
          print(">>>>>>>>>>>>>>>>>>>>>>>> TIDAK ADA DATA <<<<<<<<<<<<<<<<<<<<<<<<")
          if m.lower() == 'k':
              break

          elif m.lower() == 'l':
              print("----- DAFTAR NILAI -----")
              print("==================================================================================")
              print("| NO |   NAMA     |   NIM        |  TUGAS   |   UTS     |   UAS      |  AKHIR    |")
              print("==================================================================================")
              i = 0
              for x in data.items():
                  i += 1
                  print("|  1 |{0:9}   |{1:9}     |{2:9} |{3:9}  |{4:9}   |{5:9}  |" .format(x[0], x[1][0],
                                                                                             x[1][1], x[1][2], x[1][3],
                                                                                             x[1][4], i))

              else:
                  print("====================>>>>>>>>>>>>> Tidak Ada Data <<<<<<<<<<<<<====================")

          elif m.lower() == 't':
              print("--------------- Tambah Data ---------------")
              nama = input("Nama                  : ")
              nim = input("Nim                   : ")
              tugas = float(input("Masukan Nilai Tugas   : "))
              uts = float(input("Masukan Nilai UTS     : "))
              uas = float(input("Masukan Nilai UAS     : "))
              akhir = (int(tugas) * .30) + (int(uts) * .35) + (int(uas) * .35)
              data[nama] = nim, tugas, uts, uas, akhir

          elif m.lower() == 'u':
              print("----- Ubah Data Mahasiswa -----")
              nama = input("Nama  : ")
              if nama in data.keys():
                  nim = input("Nim : ")
                  tugas = float(input("masukan nilai tugas : "))
                  uts = float(input("masukan nilai Uts : "))
                  uas = float(input("masukan nilai uas : "))
                  akhir = (int(tugas) * .30) + (int(uts) * .35) + (int(uas) * .35)
                  data[nama] = nim, tugas, uts, uas, akhir

              else:
                  print("Tidak Ada data")

          elif m.lower() == 'h':
              print("Hapus Data Mahasiswa")
              nama = input("nama : ")
              if nama in data.keys():
                  print("Datanya", nama, "adalah {0}".format(data[nama]))
              else:
                  print("Tidaak Ada Data")

          else:
              print("Pilih menu yang tersedia")
              
![2022-11-28 (3)](https://user-images.githubusercontent.com/115775237/204420339-5f494790-adec-48dd-b816-f9d00888ed11.png)
 
# Hasil Run
 
![2022-11-28 (10)](https://user-images.githubusercontent.com/115775237/204420424-b801d906-e8ef-47d1-b3c0-1dbf3e1a7288.png)
 
# Flowchart
 
![WhatsApp Image 2022-11-28 at 20 08 58](https://user-images.githubusercontent.com/115775237/204420538-4f9ca456-fbb7-4cfe-ab34-02f30ed9cd2b.jpeg)
 
# Penjelasan
 
1. Buatlah Dictionary berupa Nama, NIM, Nilai Tugas, Nilai UTS, Nilai UAS
2. Lalu inputlah menu pilihan berupa Lihat, Tambah, Ubah, Hapus, Cari, Keluar
3. Gunakanlah perulangan for, dengan perintah for i in range(len(Nama)):. Fungsi "len" ialah untuk mengembalikan panjang (jumlah anggota) dari suatu objek.
4. Lalu inputlah Nama, NIM, Nilai Tugas, Nilai UTS, Nilai UAS
5. Lalu mencari nilai akhir dengan perhitungan nilai tugas 30%, nilai uts 35% dan uas 35% , dengan perintah float
6. Jika ingin melihat dictionary data ketik "L", jika ingin menambah data ketik "T", jika ingin mengubah data ketik "U", jika ingin menghapus ketik "H", jika ingin mencari data ketik "C" dan jika ingin keluar dari data ketik "K"
7. Lalu cetak dengan perintah print ("Pilih menu yang tersedia")
8. Selesai

 




