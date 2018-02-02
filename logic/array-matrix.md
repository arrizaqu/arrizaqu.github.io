# Array dan Matrix
* Array 
* Matrix
* Menampilkan Data
* Tugas
	
## Array 
Dalam implementasinya sebuah Array digunakan untuk menyimpan data yang memiliki banyak value.

### Bentuk 1
```java
String[] data = new String[3];
data[0] = "jakarta barat";
data[1] = "jakarta pusat";
data[2] = "jakarta timur";
```

### Bentuk 2 
```java
String[] data = new String[]{
	"jakarta barat", "jakarta pusat", "jakarta timur", "jakarta barat"
};
```

### Bentuk 3 
```java
String[] data = {
	"jakarta barat", "jakarta pusat", "jakarta timur", "jakarta barat"
}; 
```

## Array Multidimensi
Yaitu jika sebuah data Array memiliki value Array, secara singkat bisa dicontohkan sebagai berikut : 

```java
String[][] data2 = new String[2][2];
data2[0][0] = "0.0";
data2[0][1] = "0.1";
data2[1][0] = "1.0";
data2[1][1] = "1.1";
```

## Matrix
Demikian pentingnya sebuah matrix dalam perkembangan system sangat diperkukan, terutama untuk kebutuhan kumpulan data seperti table.

untuk membuat matrix akan sangat membutuhkan : 
1. panjang baris 
2. panjang kolom

secara singkat dapat dilihat pada code berkut : 

```java
int baris = 9; 
int kolom = 9;
String[] data = new String[this.baris][this.kolom];

for(int i = 0; i < this.baris; i++){
	for(int j = 0; j < this.kolom; j++){
		data[i][j] = i +"," + j;
	}
}
```

## Menampilkan data
Berikut ini adalah contoh untuk menampilkan data Matrix seperti code diatas.

```java
for(int i = 0; i < this.baris; i++){
	for(int j = 0; j < this.kolom; j++){
		System.out.println(data[i][j] + "");
	}
}
```
Atau, dengan fungsi Arrays.toString seperti berikut :
 
```java
System.out.println(Arrays.toString(data)); 
```

# Tugas
1. Buatlah Function dengan Return array (String[]) nama - nama hari. (ex: n = 5, result : ["ahad", "senin", dst])
2. Buatlah Function dengan Return array (String[]) nama - nama bulan. (ex: n = 5, result : ["january", "february", dst])
3. Buatlah Function bilangan increment dengan Return array (int[]) (ex: n = 5, result : [0,1,2,3,4])
4. Buatlah Function bilangan ganjil dengan return array (int[])(ex: n = 5, result : [1,3,5,7,9])
5. Buatlah Function dengan Return array (int[]) bilangan Fibonachi untuk jumlah data sebanyak n. (ex: n = 5, output : 1,1,2,3,5).
6. Buatlah Function dengan Return array (int[]) bilangan Fibonachi untuk jumlah data sebanyak n dan angka terbalik, (contoh : input = 5 => 1, 1, 2, 1, 1).
7. Buatlah Function dengan Return array (int[]) bilangan Tribonachi untuk jumlah data sebanyak n. (ex: n = 5, result : [1,1,1,3,5])
8. Buatlah Function dengan Return array (int[]) bilangan Tribonachi untuk jumlah data sebanyak n dan angka terbalik. (ex: n = 7, result : [1,1,1,3,1,1,1])
9. Buatlah Function dengan Return array (int[]) bilangan Triangular untuk jumlah data sebanyak n. (ex: n = 5, result : [1,3,6,10,15])
10. Buatlah Function dengan Return array (int[]) bilangan Triangular untuk jumlah data sebanyak n dan angka terbalik (ex: n = 5, result : [1,3,6,3,1])
