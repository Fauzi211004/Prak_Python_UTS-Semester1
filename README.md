# Prak_Python_UTS-Semester1

APLIKASI SEDERHANA CRUD DATA STOK BARANG
program ini merupakan program sederhana CRUD menggunakan bahasa python dengan menggunakan library mysql.connector untuk menghubungkan program dengan database MySQL.

Kemudian di program ini ada beberapa fungsi, antara lain :

1. INSERT = digunakan untuk menambahkan data ke dalam tabel data_stok_barang
2. SHOW = untuk menampilkan data yang sudah ada di database MySql
3. UPDATE = digunakan untuk mengupdate data
4. DELETE = untuk menghapus data
5. SEARCH = untuk mencari data

Setelah itu di program selanjutnya ada bebrapa menu yaitu :
1. Insert Data
if menu == "1":
        Id_Barang = input("Masukkan id barang : ")
        Nama_Barang = input("Masukkan nama barang : ")
        Harga_Barang = int(input("Masukkan harga barang : "))
        Stok_Awal = int(input("Masukkan stok awal : "))
        Barang_Masuk = int(input("Masukkan barang masuk : "))
        Barang_Keluar = int(input("Masukkan barang keluar : "))
        
        #Rumus untuk mencari stok_akhir
        stok_akhir = stok_awal + barang_masuk - barang_keluar
        
        #mencetak Stok_Akhir dari rumus sebelumnya
        print("stok akhir : ", stok_akhir)
        
        insert_data(id_barang, nama_barang, harga_barang, stok_awal, barang_masuk, barang_keluar, stok_akhir)
        
2. Show Data
elif menu == "2":
        show_data()
        
3. Update Data (update data berdasarkan id_barang)
 elif menu == "3":
        id_barang = input("Masukkan id barang yang akan diupdate : ")
        nama_barang = input("Masukkan nama barang baru : ")
        harga_barang = int(input("Masukkan harga barang baru : "))
        stok_awal = int(input("Masukkan stok awal baru : "))
        barang_masuk = int(input("Masukkan barang masuk baru : "))
        barang_keluar = int(input("Masukkan barang keluar baru : "))
        
        stok_akhir = stok_awal + barang_masuk - barang_keluar
        print("stok akhir setelah diupdate : ", stok_akhir)
        
        update_data(id_barang, nama_barang, harga_barang, stok_awal, barang_masuk, barang_keluar, stok_akhir)
        
4. Hapus Data (hapus data berdasarkan id_barang)
elif menu == "4":
        id_barang = input("Masukkan id barang yang ingin dihapus : ")
        
        delete_data(id_barang)
        
5. Cari Data (mencari data berdasarkan id_barang)
elif menu == "5":
        id_barang = input("Masukkan id barang yang ingin dicari : ")
        
        search_data(id_barang)
        
6. Keluar
 elif menu == "6":
        print("Terima kasih sudah menggunakan Aplikasi i")
        break

Program menggunakan loop while True, sehingga pengguna dapat memilih menu yang diinginkan selama program belum diakhiri (menu 6). Setelah pengguna memilih menu, program akan meminta input sesuai dengan fungsi yang dipilih dan kemudian menjalankan fungsi yang diinginkan. Setiap fungsi akan mengakses database MySQL yang dihubungkan dengan program menggunakan library mysql.connector dan melakukan operasi yang diinginkan. Setelah operasi selesai, program akan mengeluarkan pesan bahwa operasi telah berhasil dilakukan
