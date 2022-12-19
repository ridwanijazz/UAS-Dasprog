# Ujian Akhir Semester 
<br>Mata Kuliah 	: Dasar Pemrograman
<br> Nama		: Muhammad Saifurridwani 'Ijazi
<br>NIM			: 1227050094
<br>Jurusan		: [Teknik Informatika](http://if.uinsgd.ac.id/) [UIN Sunan Gunung Djati Bandung](https://uinsgd.ac.id/) 

## Deskripsi Umum
<br>Pada program kali ini dibuat untuk memenuhi Ujian Akhir Semester(UAS) mata kuliah Dasar Pemrograman, pada program ini terdapat 2 soal yaitu:
<br>1. Mengubah baris jadi kolom dan kolom jadi baris (transpose)
<br> Pada program ini kita akan mengubah nilai baris yang diinputkan menjadi kolom pada hasil dan mengubah nilai kolom yang diinputkan menjadi baris pada hasil, ini disebut juga transpose
<br>2. Menampilkan bilangan yang habis dibagi 3, 5 dan 7
<br> Pada program ini kita akan mengecek bilangan yang diinputkan apakah bisa dibagi dengan bilangan 3, 5, 7 atau tidak
## Source Code
	#include <iostream>
	using namespace std;

	int main()
	{
		int m, n;
	
		cout << "UAS"<<endl;
		cout << "===="<<endl;
		cout << "Nama : Muhammad Saifurridwani 'Ijazi"<<endl;
		cout << "NIM  : 1227050094"<<endl;
		cout << "======================================"<<endl<<endl<<endl;

		cout << "No.1 Mengubah baris jadi kolom dan kolom jadi baris (transpose)" << endl;
		cout << "==============================================================="<<endl;
		cout << "Masukkan jumlah baris matriks: ";
		cin >> m;
		cout << "Masukkan jumlah kolom matriks: ";
		cin >> n;

		int matriks[m][n], transpose[n][m];

		cout << "Masukkan Nilai-Nilai Matriks\n";
		for (int i = 0; i < m; i++)
		{
			for (int j = 0; j < n; j++)
			{
				cout <<"Baris ke "<<i+1<<", Kolom ke "<<j+1<<" : ";
				cin  >> matriks[i][j];
			}
		}

		cout << "Hasil dari matriks yang diinputkan :\n";
		for (int i = 0; i < m; i++)
		{
			for (int j = 0; j < n; j++)
			{
				cout << matriks[i][j] << "\t";
			}
			cout << endl;
		}
		cout << endl;

		for (int i = 0; i < m; i++)
		{
			for (int j = 0; j < n; j++)
			{
				transpose[j][i] = matriks[i][j];
			}
		}

		cout << "Hasil Transpose Matriks: \n";
		for (int i = 0; i < n; i++)
		{
			for (int j = 0; j < m; j++)
			{
				cout << transpose[i][j] << "\t";
			}
			cout << endl;
		}
		cout <<endl;

		cout << "No.2 Menampilkan bilangan yang habis dibagi 3, 5 dan 7" << endl;
		cout << "==============================================================="<<endl;
		cout << "Masukkan jumlah baris matriks: ";
		cin >> m;
		cout << "Masukkan jumlah kolom matriks: ";
		cin >> n;

		cout << "Masukkan Nilai-Nilai\n";
		for (int i = 0; i < m; i++)
		{
			for (int j = 0; j < n; j++)
			{
				cout <<"("<<i+1<<","<<j+1<<") : ";
				cin  >> matriks[i][j];
			}
		}
		cout << endl;

		bool cek = true;
		cout << "Nilai yang bisa dibagi 3, 5, 7 yaitu :";
		for (int i = 0; i < m; i++)
		{
			for (int j = 0; j < n; j++)
			{
				if (matriks[i][j]%3==0 && matriks[i][j]%5==0 && matriks[i][j]%7==0)
				{
					cout << " " << matriks[i][j];
					cout << endl;
					cek = false;
				}
			}
		}
		if (cek)
		{
			cout << " Nilai yang anda input tidak bisa dibagi 3, 5 dan 7" <<endl;
		}
		return 0;
	}

## Output
<br>UAS
<br>====
<br>Nama : Muhammad Saifurridwani 'Ijazi
<br>NIM  : 1227050094
<br>======================================


<br>No.1 Mengubah baris jadi kolom dan kolom jadi baris (transpose)
<br>===============================================================
<br>Masukkan jumlah baris matriks: 2
<br>Masukkan jumlah kolom matriks: 2
<br>Masukkan Nilai-Nilai Matriks
<br>Baris ke 1, Kolom ke 1 : 2
<br>Baris ke 1, Kolom ke 2 : 3
<br>Baris ke 2, Kolom ke 1 : 4
<br>Baris ke 2, Kolom ke 2 : 5
<br>Hasil dari matriks yang diinputkan :
<br>2       3
<br>4       5

<br>Hasil Transpose Matriks:
<br>2       4
<br>3       5

<br>No.2 Menampilkan bilangan yang habis dibagi 3, 5 dan 7
<br>===============================================================
<br>Masukkan jumlah baris matriks: 2
<br>Masukkan jumlah kolom matriks: 2
<br>Masukkan Nilai-Nilai
<br>(1,1) : 1
<br>(1,2) : 2
<br>(2,1) : 105
<br>(2,2) : 210

<br>Nilai yang bisa dibagi 3, 5, 7 yaitu : 
<br>105
<br>210
