# Template logic Bintang  
* 	Membuat Area Logika
	*	angka input
	*	output area sesuai input

*	Membuat Matrik menggunakan Array
	*	Menentukan panjang baris
	*	Menentukan panjang kolom
	* 	Menentukan Panjang Array
	*   Isi Data Array
	* 	Tampilkan Data Array

## Membuat Area Logika
### angka input dan program main 
Seperti pada kebayakan pembuatan program, dalam input awal dilakukan pada program main
```java
public static void main(String[] args) throws Exception{
	Template template = new Template();
	InputStreamReader isr = new InputStreamReader(System.in);
	BufferedReader br = new BufferedReader(isr);
	System.out.print("masukkan angka >>> ");
	int angka = Integer.parseInt(br.readLine());
	template.setData(angka);
	template.showData();
}
```

### output area sesuai input
Dari program main diatas, maka dalam output yang diinginkan adalah panjang dan lebar matrix disesuaikan dengan jumlah angka input dari program main seperti berikut 
``` 
0	0	0	0	0	0	0	0	0
0	0	0	0	0	0	0	0	0
0	0	0	0	0	0	0	0	0
0	0	0	0	0	0	0	0	0
0	0	0	0	0	0	0	0	0
0	0	0	0	0	0	0	0	0
0	0	0	0	0	0	0	0	0
0	0	0	0	0	0	0	0	0
0	0	0	0	0	0	0	0	0
```

## Membuat Matrik menggunakan Array

### Menentukan panjang baris dan Kolom (Deklarasi Nilai Awal)
```java
int baris = 0;
int kolom = 0;
```

### Menentukan panjang Array (Deklarasi Nilai Awal)
```java
String[][] data = null;
```

### Isi Data Array 
Dalam isi Data Array berbentuk matrix dimana pengisian data Array (Matrix : i sebagai baris, dan x sebagai kolom), i pada looping dibawah ini adalah berperan untuk looping pada baris (vertical) dan j untuk mengerjakan panjang sisi kolom (Horizontal)
```java
public void setData(int n){
	this.baris = n;
	this.kolom = n;
	data = new String[this.baris][this.kolom];
	for(int i  = 0; i < this.baris; i++){
		// do logic 
		for(int j = 0; j < this.kolom; j++){
			data[i][j] = "0";
			
		}
	}
}
```

### Tampilkan data Array
Dari data matrix yang sudah diisi pada method setDataArray berdasarkan nilai N inputan, maka langkah terakhir adalah membuat hasil output dengan memanggil data matrix i dan j.
```java
public void showData(){
	for(int i  = 0; i < this.baris; i++){
		for(int j = 0; j < this.kolom; j++){
		System.out.print(this.data[i][j]+"\t");
		}
		System.out.println();
	}
}	
```

## Full Code 
```java
public class Template {
	
	int baris = 0;
	int kolom = 0;
	String[][] data = null;
	
	public void setData(int n){
		this.baris = n;
		this.kolom = n;
		data = new String[this.baris][this.kolom];
		for(int i  = 0; i < this.baris; i++){
			// do logic 
		}
	}
	
	public void showData(){
		for(int i  = 0; i < this.baris; i++){
			for(int j = 0; j < this.kolom; j++){
				System.out.print(this.data[i][j]+"\t");
			}
			System.out.println();
		}
	}
	
	public static void main(String[] args){
		Template template = new Template();
		template.setData(9);
		template.showData();
	}
}
```

> by Masyda Arrizaqu 