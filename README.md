Penjelasan Praktikum 5

Nama  : Dedi Aldiansyah
Nim   : 312210452
Kelas : TI22B2
Tugas : Bahasa Pemrograman

Pertama kita membuat beberapa deklarasi terlebih dahulu

```
nama = []
nim = []
tugas = []
uts = []
uas = []
```

![image](https://user-images.githubusercontent.com/48305171/202936863-9653f111-d609-4ea1-ab4d-f1f07e5a8062.png)


lalu kita buat program input "Tambah data (y/t)?" dengan menggunakan perintah while, jika anda menekan huruf t makan perintah while akan berhenti "break" dan akan lanjut ke perintah berikutnya, jika anda menekan y maka program akan mengeksekusi input yang anda masukan untuk dimasukan ke dalam List kosong tersebut menggunakan perintah "append", sesuai dengan variabel List yang terhubung dengan perintah input pada masing masing data tersebut, lalu program akan mengulang ke input.

```
while True:
    nama_input = input("Nama  : ")
    nim_input = input("Nim   : ")
    tugas_input = int(input("Tugas : "))
    uts_input = int(input("UTS   : "))
    uas_input = int(input("UAS   : "))
    tanya = input("Tambah data(y/t)? ")
    nama.append(nama_input)
    nim.append(nim_input)
    tugas.append(tugas_input)
    uts.append(uts_input)
    uas.append(uas_input)
    if tanya == 't':
        break
```

![image](https://user-images.githubusercontent.com/48305171/202937794-6219d473-7b3c-419b-9cbf-6ca3b8b5c681.png)

Dengan menggunakan for, program akan melakukan perulangan dan membuat baris berdasarkan berapa banyak input di "list nama" >>for i in range(len(nama)): .
Nilai i akan ditambah 1, dengan menghitung berapa banyak jumlah list di variabel "nama", jika anda menginputkan tiga buah nama, maka penambahan nilai i akan di ulang sebanyak tiga kali, sehingga menghasilkan deret angka 1,2,3 >>print("|",i+1,end="").

![image](https://user-images.githubusercontent.com/48305171/202937982-890e0ced-83f6-4059-947e-9da96866bc3f.png)

Selanjutnya program akan menampilkan semua nilai yang telah kaliam tambahkan tadi

Program akan memanggil data nama,nim,tugas,uts,uas.

Lalu program akan meletakan data tersebut pada baris berdasarkan variabel "i", jika kalian menginputkan dua buah nama maka akan tampil.

1 nama1 nim1

2 nama2 nim2

Begitu pula data yang lain.

Untuk menampilkan nilai Akhir, program akan mengambil nilai rata rata dari nilai tugas,uts,uas dengan cara menambahkan data-data sesuai dengan index dari variabel "i".

tugas1+uts1+uas1/3

tugas2+uts2+uas2/3

Lalu Program akan mengoutputkan semua data yang telah di olah dengan program

```
print("""
=====================================================================
| No |     Nama      |    NIM    |  Tugas  |  UTS  |  UAS  |  Akhir |
=====================================================================""")

for i in range(len(nama)):
    print("|", i + 1, end="")
    if i < 9:
        print("  |", end="")
    else:
        print(" |", end="")

    print(" " + nama[i], end="")
    for j in range(14 - len(nama[i])):
        print(" ", end="")

    print("|  " + nim[i], end="")
    for k in range(9 - len(nim[i])):
        print(" ", end="")

    print("|  " + str(tugas[i]), end="")
    for l in range(7 - len(str(tugas[i]))):
        print(" ", end="")

    print("|  " + str(uts[i]), end="")
    for m in range(5 - len(str(uts[i]))):
        print(" ", end="")

    print("|  " + str(uas[i]), end="")
    for n in range(5 - len(str(uas[i]))):
        print(" ", end="")

    akhir = round((float(tugas[i] * 0.3) + float(uts[i] * 0.35) + float(uas[i] * 0.35)), 2)

    print("|  " + str(akhir), end="")
    for o in range(6 - len(str(akhir))):
        print(" ", end="")

    print("|")

print("=====================================================================")
```

![image](https://user-images.githubusercontent.com/48305171/202944165-76db7c6b-5841-41c2-a446-db7968ac560d.png)

![image](https://user-images.githubusercontent.com/48305171/202944182-79777247-601b-4067-95d2-8b0a27cf68ee.png)

Hasil program

![image](https://user-images.githubusercontent.com/48305171/202945808-1a9e7433-b0c0-4c89-ad73-d910eb037106.png)


Flowchart program di atas

![image](https://user-images.githubusercontent.com/48305171/202943436-f760d930-9d1e-41f3-a092-28cbeedb0272.png)

