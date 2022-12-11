# Nama  : Naza Sefti Prianita

# NIM   : 312210306

# Kelas : TI.22.A3

# TUGAS PRAKTIKUM 8

![image](https://user-images.githubusercontent.com/115772516/206904687-593a0ba8-57cf-4ac1-9992-9e077c0b5341.png)

. Untuk memanggil fungsi dengan nama "os".

import os

. Membuat class data_mhsw dengan atributnya, yaitu nama, nim, tugas, uts, dan uas.

class data_mhsw:
    nama=""
    nim=""
    tugas=""
    uts=""
    uas=""
    
. Membuat variabel data = [] untuk menampung list dari data_mhsw.

data = []

. Membuat fungsi tambahan jika diperlukan fungsi tersebut akan dipanggil oleh program.

def no_data():
    print("DAFTAR NILAI MAHASISWA")
    print("----------------------")
    print()
    print(" - TIDAK ADA DATA - ")
    print()
    
. Menampilkan data (lihat())

. Jika belum menginput data, maka akan memanggil fungsi no_data()

. Jika sebelumnya sudah menginput data, maka data sudah diinputkan akan di tampilkan oleh program.

def lihat():
    os.system("cls")
    if len(data) <=0:
        no_data()
    else:
        for a in data:
            print("DAFTAR NILAI MAHASISWA")
            print("-----------------------")
            print("Nama Mahasiswa\t: "+a.nama)
            print("NIM Mahasiswa\t: "+str(a.nim))
            print("Nilai Tugas\t: "+str(a.tugas))
            print("Nilai UTS\t: "+str(a.uts))
            print("Nilai UAS\t: "+str(a.uas))
            print("Nilai Akhir\t: "+str(a.akhir))
            print()
     
. Menambahkan data (Tambah())

. Menginput NIM, NAMA, Nilai Tugas, Nilai UTS, Nilai UAS.

. Jika data yang sudah diinput akan ditambahkan ke dalam variabel data.

def tambah():
    os.system("cls")
    b = data_mhsw()
    print("TAMBAH DATA")
    print("------------")
    b.nama = (input("Nama Mahasiswa\t: "))
    b.nim = (int(input("NIM Mahasiswa\t: ")))
    b.tugas = (int(input("Nilai Tugas\t: ")))
    b.uts = (int(input("Nilai UTS\t: ")))
    b.uas = (int(input("Nilai UAS\t: ")))
    b.akhir = (b.tugas*30/100) + (b.uts*35/100) + (b.uas*35/100)
    data.append(b)
    print()
    
. Mengubah data (Ubah())

. Menginput Nama, kemudian input data yang ingin di ubah.

def ubah():
    os.system("cls")
    if len(data) <=0:
        no_data()
    else:
        nama = data_mhsw()
        print("UBAH DATA")
        print("---------")
        nama = (input("Nama Mahasiswa\t: "))
        for nama in data:
            nama.tugas = (int(input("Nilai Tugas\t: ")))
            nama.uts = (int(input("Nilai UTS\t: ")))
            nama.uas = (int(input("Nilai UAS\t: ")))
            akhir = (nama.tugas*30/100) + (nama.uts*35/100) + (nama.uas*35/100)
        print()
        
. Menghapus data (Hapus())

. Menginput Nama, setelah Nama yang diinputkan maka data yang lainnya akan ikut terhapus sesuai dengan nama yang diinputkan.

def hapus():
    os.system("cls")
    if len(data) <=0:
        no_data()
    else:
        nama = data_mhsw()
        print("HAPUS DATA")
        print("----------")
        nama = (input("Nama Mahasiswa\t: "))
        for nama in data:
            data.remove(nama)
        print()
        
. Menggunakan Perulangan uncountable, yang artinya selama statement bernilai True maka program akan terus berjalan. Jika statementnya False maka program akan terhenti.

Loop = True
while Loop:
    print("Pilih Menu")
    print("----------")
    tanya = input("[(L)ihat, (T)ambah, (U)bah, (H)apus, (K)eluar] : ")
    print()
    if tanya == "l" or tanya == "L":
        lihat()

    elif tanya == "t" or tanya == "T":
        tambah()

    elif tanya == "u" or tanya == "U":
        ubah()

    elif tanya == "h" or tanya == "H":
        hapus()

    elif tanya == "k" or tanya == "K":
        print("Program Selesai")
        Loop = False
        
# Hasil Output

