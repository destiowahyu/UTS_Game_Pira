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
