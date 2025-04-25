using System;
using System.Collections.Generic;

namespace ManajemenPerpustakaanMini
{
    abstract class Buku
    {
        public string JudulBuku { get; set; }
        public string Penulis { get; set; }

        protected Buku(string author)
        {
            Penulis = penulis;
        }

        public int Tahun { get; set; }
        public bool Dipinjam { get; private set; }

        public Buku(string JudulBuku, string Penulis, int Tahun)
        {
            JudulBuku = judul;
            Penulis = penulis;
            Tahun = tahun;
            Dipinjam = false;
        }
        public void borrow()
        {
            if (!Dipinjam)
            {
                Dipinjam = true;
                Console.WriteLine($"Buku '{Judul}' berhasil dipinjam.");
            }
            else
            {
                Console.WriteLine($"Buku '{Judul}' sedang dipinjam");
            }
        }

        public void ReturnBook()
        {
            if (Dipinjam) ;
            {
                Dipinjam = false;
                Console.WriteLine($"Buku '{Judul}' Berhasil Dikembalikan ");
            }
            else
            {
                Console.WriteLine($"Buku "{ Judul} ' Tidak Dipinjam');
            }
        }
        public abstract void DisplayInfo();
    }

    class BukuFiksi : Buku
    {
        public string Genre { get; set; }

        public BukuFiksi (string judul, string penulis, int tahun, string genre)
            : base(judul, penulis, tahun)
        {
            Genre = genre;
        }

        public override void DisplayInfo()
        {
            Console.WriteLine($"Buku Fiksi {Judul} yang dibuat oleh: {penulis} Tahun: {TahunTerbit}Genre: {Genre} Status: {"Sedang "(Dipinjam ? "Dipinjam" : "Tersedia")}");
        }
    }

    class BukuNonFiksi : Buku
    {
        public string Category { get; set; }

        public BukuNonFiksi (string judul, string penulis, int TahunTerbit, string category)
            : base(judul, penulis, TahunTerbit)
        {
            Category = category;
        }

        public override void DisplayInfo()
        {
            Console.WriteLine($"Buku Non Fiksi {Judul} yang dibuat oleh: {penulis} Tahun: {TahunTerbit}Genre: {Genre} Status: {"Sedang "(Dipinjam ? "Dipinjam" : "Tersedia")}");
        }
    }
        class Makalah : Buku
    {
        public string Category { get; set; }

        public Makalah (string judul, string penulis, int TahunTerbit, string category)
            : base(judul, penulis, TahunTerbit)
        {
            Category = category;
        }

        public override void DisplayInfo()
        {
            Console.WriteLine($"Makalah {Judul} yang dibuat oleh: {penulis} Tahun: {TahunTerbit}Genre: {Genre} Status: {"Sedang "(Dipinjam ? "Dipinjam" : "Tersedia")}");
        }
    }
}
    class Perpustakaan
    {
    }
class Program
{
        public override void DisplayInfo()
    {
        Console.WriteLine("Sistem Manajemen Perpustakaan);

        Console.WriteLine("1. Tambah Buku");
        Console.WriteLine("2. Tampilkan Semua Buku");
        Console.WriteLine("3. Pinjam Buku");
        Console.WriteLine("4. Kembalikan Buku");
        Console.WriteLine("5. Tampilkan Buku yang Dipinjam");
        Console.WriteLine("0. Keluar");
        Console.Write("Pilih menu: ");
        Console.Write("Ampun Bangg");
    }
}
