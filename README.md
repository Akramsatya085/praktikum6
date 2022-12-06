# Nama: Akram Satya

NIM: 312210461

Kelas: TI.22.A4

Praktikum

dataMahasiswa = {}

print("=" * 65)
print("|\tPROGRAM INPUT NILAI MAHASISWA MENGGUNAKAN FUNGSI\t|")
print("=" * 65)

def tambah():
        nama = str(input("Masukan Nama : "))
        nim = int(input("Masukan Nim   : "))
        tugas = int(input("Masukan Nilai Tugas : "))
        uts = int(input("Masukan Nilai UTS     : "))
        uas = int(input("Masukan Nilai UAS     : "))
        akhir = (tugas / 3) + (uts / 3.5) + (uas / 3.5)
        dataMahasiswa[nama] = nim, tugas, uts, uas, akhir,
        print("\nDATA BERHASIL DI TAMBAHKAN!")
def tampilkan():
        print("=" * 69)
        print("|" + "\t" * 3 + "DAFTAR NILAI MAHASISWA" + "\t" * 3 +
                  "    |")
        print("=" * 69)
        print("| NO |   \tNAMA\t   |\tNIM \t| TUGAS | UTS | UAS | AKHIR |")
        print("=" * 69)
        for tampil in dataMahasiswa.items():
            no = 0
            no += 1
            print("| {6:2} |\t {0:15}   | {1:9} \t| {2:5} | {3:3} | {4:3} | {5:5} |".format(tampil[0], tampil[1][0], tampil[1][1], tampil[1][2], tampil[1][3],"%.2f" % float(tampil[1][4]), no))
            print("=" * 69)
def hapus(nama):
            del dataMahasiswa[nama]
            print("DATA BERHASIL DI HAPUS!")
 
def ubah(nama):
        if nama in dataMahasiswa.keys():
            nim = int(input("Masukan Nim  : "))
            tugas = int(input("Masukan Nilai Tugas : "))
            uts = int(input("Masukan Nilai UTS     : "))
            uas = int(input("Masukan Nilai UAS     : "))
            akhir = (tugas / 3) + (uts / 3.5) + (uas / 3.5)
            dataMahasiswa[nama] = nim, tugas, uts, uas, akhir
            print("\nDATA BERHASIL DI UBAH!")
        else:
            print("\DATA TIDAK DI TEMUKAN!")

while True:
    data = input(
        "\n 1 - Tambah Data,\t 2 - Tampilkan Data,\t 3 - Hapus Data,\t 4 - Ubah Data, 5 - Keluar \n : "
    )
    if (data.lower() == '1'):
        tambah()

    elif (data.lower() == '4'):
        nama = str(input("Masukan Nama : "))
        ubah(nama)
    elif (data.lower() == '3'):
        nama = str(input("Masukan Nama : "))
        if nama in dataMahasiswa:
            hapus(nama)
        else:
            print("DATA TIDAK DI TEMUKAN ".format(nama))
    elif (data.lower() == '2'):
        if dataMahasiswa.items():
            tampilkan()
        else:
            print("=" * 69)
            print("|" + "\t" * 3 + "DAFTAR NILAI MAHASISWA" + "\t" * 3 +
                  "    |")
            print("=" * 69)
            print("| NO |   \tNAMA\t   |\tNIM \t| TUGAS | UTS | UAS | AKHIR |")
            print("=" * 69)
            print("|    " + "\t" * 3 + "TIDAK ADA DATA!" + "\t" * 4 + "    |")
            print("=" * 69)
    elif (data.lower() == '5'):
        print("\nTERIMA KASIH! \n")
        exit()
    else:
        print("PILIHAN MENU TIDAK ADA!")
        
        ![Screenshot (26)](https://user-images.githubusercontent.com/115615953/205827324-98fe392d-ca62-4a5b-b639-4d9287fab701.png)
        
        ![Screenshot (27)](https://user-images.githubusercontent.com/115615953/205827588-a5e8f225-e87e-4245-a101-15cf267a44a1.png)
        
        
![flowchart](https://user-images.githubusercontent.com/115615953/205828247-d88951db-6edb-4176-824a-a6f4cf40a5db.png)

