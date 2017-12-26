# Logic Bintang Bangun Loop
* 	Kebutuhan
*	Output yang diharapkan
* 	Panjang Matrix sesuai input 
* 	Formula Logika
	* Segitiga Normal
	* Segitiga Kebalik
	* Segitiga kekanan
	* Segitiga kekiri
* Full Code 

Mengapa bangun loop, karena pada pembahasan ini, adalah level setelah sudah terbangun sebuah pola kemudian dari pola tersebut adalah membentuk pola yang lebih besar kembali, pada pembahasan sebelumnya dapat digambarkan adalah membuat bangun dari Array Matrix sebagai contoh adalah membuat peramida dengan input : 2,
```js
	#		
#	#	#	
	#	
```

dengan pembahasan ini maka dari segitiga akan di loop yang ke bentuk yang lebih besar.
```js
	#						#	
#	#	#				#	#	#
	#						#	
				#				
			#	#	#			
				#				
	#						#	
#	#	#				#	#	#
	#						#	

```

## Kebutuhan
Mengerti konsep menggunakan Array Matrix [lihat disini](https://arrizaqu.github.io/logic/template).
	
## Output yang diharapkan
```java
 	 	*	 	 
 	*	*	*	 
*	*	*	*	*
```
## Panjang Matrix sesuai input
Panjang pada baris dan kolom untuk setup matrix vertical dan horizontal (i dan j), untuk segitiga memiliki panjang yang berbeda, dan dapat disimpulkan, bahwa jumlah perbandingan antara i dan j adalah 
```js
jika pajang sisi panjang segita adalah sesuai n
n / 2
```

dan
```js
jika pajang sisi panjang segita adalah 2x nilai n
n * 2 - 1
```

```java
contoh simple untuk baris dan kolom segitiga sesuai input diatas.
this.baris = n;
this.kolom = n* 2 - 1;
```

## Formula Logika
### Segitiga Normal
```java
i + j >= n - 1 && j - i <= n - 1

 	 	*	 	 	
 	*	*	*	 	
*	*	*	*	*
```

### Segitiga Kebalik
```java
j - i >=0 && i + j <= this.kolom - 1

*	*	*	*	*
 	*	*	*	 
 	 	*	 	 
```

### Segitiga kekanan
Berbeda dengan segita normal dan kebalik untuk matrix segitiga ke kanan sumbu baris akan lebih besar dibanding sumbu kolom, maka ubah matrix menjadi 
```js
this.baris = n* 2 - 1;
this.kolom = n;
```

formula
```js
i >= j && i + j <=this.baris - 1

*	 	 	 	 
*	*	 	 	 
*	*	*	 	 
*	*	*	*	 
*	*	*	*	*
*	*	*	*	 
*	*	*	 	 
*	*	 	 	 
*
```

### Segitiga kekiri
```java
i + j >= n - 1 && i - j <= this.baris/2

 	 	 	 	*
 	 	 	*	*
 	 	*	*	*
 	*	*	*	*
*	*	*	*	*
 	*	*	*	*
 	 	*	*	*
 	 	 	*	*
 	 	 	 	*
```

### Full Code 
```java
public class Template {
	//written by masyda arrizaqu
	int baris = 0;
	int kolom = 0;
	String[][] data = null;
	
	public void setData(int n){
		this.baris = n* 2 - 1;
		this.kolom = n;
		data = new String[this.baris][this.kolom];
		for(int i  = 0; i < this.baris; i++){
			// do logic 
		for(int j = 0; j < this.kolom; j++){
			if(i + j >= n - 1 && i - j <= baris/2){
				data[i][j] = "*";
			} else {
				data[i][j] = " ";
			}
		}
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
	
	public static void main(String[] args) throws Exception{
		Template template = new Template();
		InputStreamReader isr = 
		new InputStreamReader(System.in);
		BufferedReader br = new BufferedReader(isr);
		System.out.print("masukkan angka >>> ");
		int angka = Integer.parseInt(br.readLine());
		template.setData(angka);
		template.showData();
	}
}

```

> by Masyda Arrizaqu 