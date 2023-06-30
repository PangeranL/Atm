/*Nama File : Ahmad Fahrezi */
/*Deskripsi : Transaksi Mesin ATM Bank Sodikun*/
/*Pembuat   : Ahmad Fahrezi - 24060122140146*/

#include <stdio.h>
#include <stdlib.h>

// PIN dan saldo
int pin = 9999;
int saldo = 5000000;

//Menampilkan menu pilihan transaksi
void tampilkanMenu() {
    printf("\nSelamat Datang\n");
    printf("MESIN ATM BANK SODIKUN\n");
    printf("===================================\n");
    printf("< 1 > Cek Saldo\n");
    printf("< 2 > Tarik Tunai\n");
    printf("< 3 > Setor Tunai\n");
    printf("< 4 > Keluar\n");
}

//Menampilkan saldo
void cekSaldo() {
    printf("\nSaldo anda sekarang adalah sebesar Rp. %d\n", saldo);
}

//Melakukan tarik tunai
void tarikTunai() {
    int tarik;
    printf("\nMasukkan jumlah nominal yang akan ditarik tunai: Rp. ");
    scanf("%d", &tarik);

    if (tarik > saldo - 50000) {
        printf("\nMaaf saldo anda tidak mencukupi\n");
    }
    else {
        saldo -=tarik;
        printf("\nAnda berhasil menarik tunai sebesar Rp. %d\n", tarik);
        printf("Saldo anda sekarang adalah sebesar Rp. %d\n", saldo);
    }
}

//Melakukan setor tunai
void setorTunai() {
    int setor;
    printf("\nMasukkan jumlah nominal yang akan disetor tunai: Rp.");
    scanf("%d", &setor);
    saldo += setor;
    printf("\nAnda berhasil menyetor tunai sebesar Rp. %d\n", setor);
    printf("Saldo anda sekarang adalah sebesar Rp. %d\n", saldo);
}

//Fungsi utama
int main() {
    int inputPin;
    int pilihan;
    int kesalahanPin = 0;
    printf("Masukkan PIN Anda: ");
    scanf("%d", &inputPin);

    while (inputPin != pin && kesalahanPin < 2) {
        kesalahanPin++;
        printf("\nPIN Salah. Silahkan coba lagi.\n");
        printf("Masukkan PIN Anda: ");
        scanf("%d", &inputPin);
    }

    if (inputPin != pin) {
        printf("\nATM diblokir. Silahkan hubungi Bank Sodikun.\n");
        return 0;
    }
    else {
        printf("\nPIN Benar\n");

        do {
            tampilkanMenu();
            printf("Masukkan pilihan anda: ");
            scanf("%d", &pilihan);

            switch (pilihan) {
                case 1:
                    cekSaldo();
                    break;
                case 2:
                    tarikTunai();
                    break;
                case 3:
                    setorTunai();
                    break;
                case 4:
                    printf("\nTerima kasih telah menggunakan ATM kami\n");
                    return 0;
                default:
                    printf("\nPilihan yang anda masukkan tidak tersedia\n");
                    break;
            }
        } while (1);
    }

    return 0;
}
