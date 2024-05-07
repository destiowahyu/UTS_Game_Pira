    #include <iostream> // 1
    #include <cstdlib> // 2
    #include <ctime> // 3

    int main() {
        std::srand(std::time(0)); // 4
        int number = std::rand() % 100 + 1; // 5
        int guess = 0; // 6
        int attempts = 0; // 7

    std::cout << "Tebak angka antara 1 dan 100.\n"; // 8

    do {
        std::cout << "Masukkan tebakan Anda: "; // 9
        std::cin >> guess; // 10
        attempts++; // 11

        if (guess > number) { // 12
            std::cout << "Terlalu tinggi. Coba lagi.\n"; // 13
        } else if (guess < number) { // 14
            std::cout << "Terlalu rendah. Coba lagi.\n"; // 15
        }
    } while (guess != number); // 16

    std::cout << "Selamat! Anda menebak angka dengan benar dalam " << attempts << " percobaan.\n"; // 17

    return 0; // 18
    }


Penjelasan Tiap Baris Kode :
1. `#include <iostream>`: Mengimpor library iostream yang digunakan untuk operasi input dan output.
2. `#include <cstdlib>`: Mengimpor library cstdlib yang berisi fungsi untuk operasi umum seperti pembangkit bilangan acak.
3. `#include <ctime>`: Mengimpor library ctime untuk mendapatkan waktu sistem saat ini.
4. `std::srand(std::time(0))`: Menginisialisasi pembangkit bilangan acak dengan nilai seed berdasarkan waktu sistem.
5. `int number = std::rand() % 100 + 1`: Mendeklarasikan dan menginisialisasi variabel `number` dengan bilangan acak antara 1 dan 100.
6. `int guess = 0`: Mendeklarasikan variabel guess untuk menyimpan tebakan pengguna.
7. `int attempts = 0`: Mendeklarasikan variabel attempts untuk menghitung jumlah percobaan.
8. `std::cout << "Tebak angka antara 1 dan 100.\n"`: Menampilkan pesan ke pengguna untuk menebak angka.
9. `std::cout << "Masukkan tebakan Anda: "`: Menampilkan pesan yang meminta pengguna untuk memasukkan tebakan.
10. `std::cin >> guess`: Membaca input tebakan dari pengguna.
11. `attempts++`: Menambahkan jumlah percobaan setiap kali pengguna memasukkan tebakan.
12. `if (guess > number)`: Memeriksa apakah tebakan lebih besar dari angka yang dihasilkan.
13. `std::cout << "Terlalu tinggi. Coba lagi.\n"`: Menampilkan pesan bahwa tebakan terlalu tinggi jika kondisi di atas terpenuhi.
14. `else if (guess < number)`: Memeriksa apakah tebakan lebih kecil dari angka yang dihasilkan.
15. `std::cout << "Terlalu rendah. Coba lagi.\n"`: Menampilkan pesan bahwa tebakan terlalu rendah jika kondisi di atas terpenuhi.
16. `while (guess != number)`: Loop akan terus berjalan selama tebakan tidak sama dengan angka yang dihasilkan.
17. `std::cout << "Selamat! Anda menebak angka dengan benar dalam " << attempts << " percobaan.\n"`: Menampilkan pesan selamat dan jumlah percobaan setelah tebakan benar.
18. `return 0`: Mengakhiri fungsi `main` dan mengembalikan nilai 0 yang menandakan program berakhir dengan sukses.

Cara kerja Program :
1. Program menginisialisasi generator angka acak dengan `std::srand(std::time(0))`.
2. Program memilih angka acak antara 1 dan 100 menggunakan `std::rand() % 100 + 1`.
3. Program meminta pengguna untuk menebak angka dengan memberikan prompt di konsol.
4. Pengguna memasukkan tebakan mereka, dan program memeriksa apakah tebakan itu terlalu tinggi, terlalu rendah, atau benar.
5. Jika tebakan pengguna salah, program akan memberikan petunjuk dan meminta tebakan lain.
6. Proses ini berulang sampai pengguna menebak angka yang benar.
7. Setelah tebakan yang benar, program mencetak jumlah percobaan yang dibutuhkan pengguna untuk menebak angka dan mengakhiri permainan.

- Destio
