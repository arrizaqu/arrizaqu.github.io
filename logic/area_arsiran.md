# Logic Bintang Area Arsiran  
* 	Kebutuhan
*	output yang diharapkan 
* 	Formula Logika
	* arsiran 1 (naik ke kiri)
	* kebalikan arsiran 1 
	* arsiran 2 (naik ke kanan)
	* kebalikan arsiran 2
* Full Code 

Disesuikan dengan judulnya, bahwa bagaimana membuat area arsiran pada logik bintang.

## Kebutuhan
Mengerti konsep menggunakan Array Matrix [lihat disini](https://arrizaqu.github.io/logic/template).
	
## Output yang diharapkan
```java
*	 	 	 	 	 	 
*	*	 	 	 	 	 
*	*	*	 	 	 	 
*	*	*	*	 	 	 
*	*	*	*	*	 	 
*	*	*	*	*	*	 
*	*	*	*	*	*	*
```

## Formula Logika
### arsiran 1 (naik ke kiri)

```js
i >= j

*	 	 	 	 	 	 
*	*	 	 	 	 	 
*	*	*	 	 	 	 
*	*	*	*	 	 	 
*	*	*	*	*	 	 
*	*	*	*	*	*	 
*	*	*	*	*	*	*
```

### kebalikan arsiran 1 
```js
i <= j

*	*	*	*	*	*	*
 	*	*	*	*	*	*
 	 	*	*	*	*	*
 	 	 	*	*	*	*
 	 	 	 	*	*	*
 	 	 	 	 	*	*
 	 	 	 	 	 	*
```

### arsiran 2 (naik ke kanan)
```js
i + j >= n - 1

	 	 	 	 	 	*
 	 	 	 	 	*	*
 	 	 	 	*	*	*
 	 	 	*	*	*	*
 	 	*	*	*	*	*
 	*	*	*	*	*	*
*	*	*	*	*	*	*
```

### kebalikan arsiran 2
	
### garis diagonal 1 (naik ke kiri)
```js
i + j <= n - 1

*	*	*	*	*	*	*
*	*	*	*	*	*	 
*	*	*	*	*	 	 
*	*	*	*	 	 	 
*	*	*	 	 	 	 
*	*	 	 	 	 	 
*
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
				if(i + j <= n - 1){
					data[i][j] = "*";
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