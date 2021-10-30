#APLIKASI INPUT DATA MAHASISWA 


import os
import sys

class Mahasiswa:
        nim= "212370090"
        nama= "Asri Nurhasanah Putri Solin"

pilih = 0
dataSiswa = []

def Menu () : 
    os.system ('clear');
    print("Menu Aplikasi Data Siswa")
    print("-----------------------------------------")
    print("1. Input Data Siswa")
    print("2. Tampilkan Data Siswa")
    print("3. Update Data Siswa")
    print("4. Hapus Data Siswa")
    print("5. Author")
    print("6. Keluar Aplikasi")
    pilih = int(input("Masukkan Pilihan Anda : "))
if pilih == 1 :
    tampil()
    Menu()
elif pilih == 2 :
    tampil()
    input("Kembali Ke Menu Utama")
    Menu()
elif pilih == 3 :
    index_update=-1
    tampil()
    id_edit = int(input("Input Nim Yang Akan Di Update "))
    for a in range (0, len(dataSiswa)):
        if id_edit == dataSiswa[a].Nim:
            index_update = a 
            break
    if(index_update > -1):
        print("INPUT DATA SISWA YANG AKAN DI UPDATE ")
        siswa = MAHASISWA()
        siswa.Nim = (int(input("Masukkan Nim : ")))
        siswa.nama = (input("Masukkan Nama Siswa : "))
        dataSiswa[index_update] = siswa
        print("Berhasil Update Data Siswa")
    else : print("Nim Tidak Ditemukan")
    input("Kembali Ke Menu Utama")
    Menu()
elif pilih == 4 :
    os.system('clear')
    tampil()
    index_delete=-1
    id_hapus = int(input("Input Nim yang di hapus : "))
    for a in range(0, len(dataSiswa)):
        if id_edit == dataSiswa[a].Nim:
                    index_update = a
                    break
    if(index_delete > -1):
        del dataSiswa[index_delete]
        print("Data Telah Di Hapus")
    else : print ("Data Telah Di Hapus")
    input("Kembali Menu Utama")
    Menu()
elif pilih == 5 : 
    Author()
    input("\n\n Kembali Ke Menu Utama")
    Menu()
elif pilih == 6 :
    sys.exit()
    
def tampil():
    os.system('clear');
    print("DATA MAHASISWA")
    for Data in dataSiswa:
        print("Nim : "+str(siswa.Nim))
        print("Nama : "+ siswa.Nama)
        print("----------------------------")
    
def Author():    
    os.system('clear');
    print("Asri Nurhasanah Putri Solin")
    print("UNHAR")

def pilih1():
    ulang = 'Y'
    while ulang in("y", "Y"):
        os.system('clear');
        siswaBaru = MAHASISWA()
        print("Input Data Mahasiswa ")
        siswaBaru.Nim = (int(Input("Masukkan Nim : ")))
        siswaBaru.Nama = (Input("Masukkan Nama Siswa : "))
        dataSiswa.append(siswaBaru)
        ulang = input ("Apakah Anda Ingin Mengulang (Y/T)? ")

Menu()
