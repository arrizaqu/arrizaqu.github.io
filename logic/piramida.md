# Logic Bintang Piramida 
* 	Kebutuhan
*	Output yang diharapkan
* 	Panjang Matrix sesuai input 
* 	Formula Piramida
	* Segitiga atas
	* Segitiga bawah
	* Jadinya 
	
* Full Code 

Disesuikan dengan judulnya, bahwa bagaimana membuat piramida pada logic bintang dengan Matrix

## Kebutuhan
Mengerti konsep menggunakan Array Matrix [lihat disini](https://arrizaqu.github.io/logic/template).
	
## Output yang diharapkan
```java
 	 	*	 	 
 	*	*	*	 
*	*	*	*	*
 	*	*	*	 
 	 	*	 	 
```

## Panjang Matrix sesuai input
Panjang matrix untuk bentuk piramida adalah sama untuk i dan j
```js
this.baris = n* 2 - 1;
this.kolom = n* 2 - 1;
```

## Formula Piramida
### Segitiga atas
```js
j - i <= this.kolom / 2 && i + j >= this.kolom / 2 
```
### Segitiga bawah
```js
i - j <= this.baris / 2 && i + j <= this.baris + this.kolom / 2 - 1
```

### Jadinya
```java
boolean segitigaAtas = j - i <= this.kolom / 2 && i + j >= this.kolom / 2;
boolean segitigaBawah = i - j <= this.baris / 2 && i + j <= this.baris + this.kolom / 2 - 1;
if(segitigaAtas && segitigaBawah){
	data[i][j] = "*";
}
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
		this.kolom = n* 2 - 1;
		
		data = new String[this.baris][this.kolom];
		for(int i  = 0; i < this.baris; i++){
			// do logic 
		for(int j = 0; j < this.kolom; j++){
			//segitiga atas
			boolean segitigaAtas = j - i <= this.kolom / 2 && i + j >= this.kolom / 2;
			boolean segitigaBawah = i - j <= this.baris / 2 && i + j <= this.baris + this.kolom / 2 - 1;
			if(segitigaAtas && segitigaBawah){
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