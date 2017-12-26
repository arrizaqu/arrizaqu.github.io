# Logic Bintang Segitiga Empat
* 	Kebutuhan
*	Output yang diharapkan
* 	Panjang Matrix sesuai input 
* 	Formula Logika
	* 	Bagian Segitiga
		* Segitiga atas
		* Segitiga Kanan
		* Segitiga Bawah
		* Segitiga kiri
	* 	Segitiga Bertemu horizontal
	* 	Segitiga Bertemu Vertical
* Full Code 

Pada script berikut ini adalah membuat segitiga empat, apa maksutnya ? yaitu, membuat segitiga dalam 4 bagian, dan konsep ini biasanya menjadi dasar untuk bentuk bentuk yang lain.

## Kebutuhan
Mengerti konsep menggunakan Array Matrix [lihat disini](https://arrizaqu.github.io/logic/template).
	
## Output yang diharapkan
```java
*	*	*	*	*	*	*	*	*
 	*	*	*	*	*	*	*	 
 	 	*	*	*	*	*	 	 
 	 	 	*	*	*	 	 	 
 	 	 	 	*	 	 	 	 
 	 	 	*	*	*	 	 	 
 	 	*	*	*	*	*	 	 
 	*	*	*	*	*	*	*	 
*	*	*	*	*	*	*	*	*
```

## Panjang Matrix sesuai input 
```java
this.baris = n;
this.kolom = n;
```

## Formula Logika
### Bagian Segitiga
#### Segitiga atas
```js
boolean sgAtas = j >= i && i + j <= this.kolom - 1;
```

#### Segitiga Kanan
```js
boolean sgKanan = i + j >= this.kolom - 1 && i <= j;
```
#### Segitiga Bawah
```js
boolean sgBawah = i >= j && i + j >= this.kolom - 1;
```

#### Segitiga kiri
```js
boolean sgKiri = i >= j && i + j <= this.kolom - 1;
```

### Segitiga Bertemu Vertical
```js
boolean sgAtas = j >= i && i + j <= this.kolom - 1;
boolean sgBawah = i >= j && i + j >= this.kolom - 1;
if(sgAtas || sgBawah){
	data[i][j] = "*";
}
```

### Segitiga Bertemu Horizontal
```js
dipikir sendiri ya.. :)
```


### Full Code 
```java
public class Template {
	// written by masyda arrizaqu
	int baris = 0;
	int kolom = 0;
	String[][] data = null;
	
	public void setData(int n){
		this.baris = n;
		this.kolom = n;
		
		data = new String[this.baris][this.kolom];
		for(int i  = 0; i < this.baris; i++){
			// do logic 
		for(int j = 0; j < this.kolom; j++){
			//segitiga atas
			boolean sgAtas = j >= i && i + j <= this.kolom - 1;
			boolean sgBawah = i >= j && i + j >= this.kolom - 1;
			boolean sgKanan = i + j >= this.kolom - 1 && i <= j;
			boolean sgKiri = i >= j && i + j <= this.kolom - 1;
			
			if(sgAtas || sgBawah){
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
		InputStreamReader isr = new InputStreamReader(System.in);
		BufferedReader br = new BufferedReader(isr);
		System.out.print("masukkan angka >>> ");
		int angka = Integer.parseInt(br.readLine());
		template.setData(angka);
		template.showData();
	}
}

```

> by Masyda Arrizaqu 