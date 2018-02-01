# Array dan Matrix
	* Array 
	* Matrix
	
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
