# Logic Bintang Bangun Loop
* 	Kebutuhan
*	Output yang diharapkan
* 	Panjang Matrix sesuai input 
* 	Formula Logika
	* 	for(i, j) 1
	* 	for(i, j) 2
	* 	copy pola
	* 	Logic lengkap
	
* Full Code 

Mengapa bangun loop, karena pada pembahasan ini, adalah level setelah terbangun sebuah pola kemudian dari pola tersebut akan membentuk pola yang lebih besar, dicontohkan membuat bangun dari Array Matrix peramida dengan input : 2,
```js
	*		
*	*	*	
	*	
```

dari bentuk piramid diatas akan di loop kepada ke bentuk yang lebih besar, seperti berikut 
```js
	*						*	
*	*	*				*	*	*
	*						*	
				*				
			*	*	*			
				*				
	*						*	
*	*	*				*	*	*
	*						*	

```

## Kebutuhan
Mengerti konsep menggunakan Array Matrix [lihat disini](https://arrizaqu.github.io/logic/template).
	
## Output yang diharapkan
```java
Jika inputan adalah 2 maka akan terbentuk : 

	*						*	
*	*	*				*	*	*
	*						*	
				*				
			*	*	*			
				*				
	*						*	
*	*	*				*	*	*
	*						*	
```
## Panjang Matrix sesuai input
untuk sifat bangun yang sama dengan panjang baris dan panjang kolom (i == j) seperti kotak, piramid, maka panjang matrix akan secara mudah dipahami dengan:
```js
this.baris = n*n;
this.kolom = n*n;
```

## Formula Logika
### for(i, j) 1
```java
for(int i  = 0; i < this.baris; i++){
	for(int j = 0; j < this.kolom; j++){
	boolean a = j + i >= n/2 && j -i <= n/2;
	boolean b = i -j <= n/2 && i + j <= (n/2) + (n - 1);
		if( a && b){
		//pola dasar
		}
	}
}
```

### for(i, j) 2
### copy pola
### Logic lengkap

### Full Code 
```java
public class Template {
	//written by masyda arrizaqu
	int baris = 0;
	int kolom = 0;
	String[][] data = null;
	
	public void setData(int n){
		this.baris = n*n;
		this.kolom = n*n;
		data = new String[this.baris][this.kolom];
		int addBlock = 0;
		for(int block = 0; block < n; block++){
			int addBangun = 0;
			for(int bangun = 0; bangun < n; bangun++){
				for(int i  = 0; i < this.baris; i++){
					for(int j = 0; j < this.kolom; j++){
						if(j + i >= n/2 && j -i <= n/2 && i -j <= n/2 && i + j <= (n/2) + (n - 1)){
							if(bangun  == block){
								data[i+ addBlock][j + addBangun] = "#";
							} else if(bangun + block == n - 1){
								data[i+ addBlock][j + addBangun] = "#";
							}
							
						}	
					}
				}
				addBangun = addBangun + n;
			}
			addBlock = addBlock + n;
		}
		
		
	}
	
	public void showData(){
		for(int i  = 0; i < this.baris; i++){
			for(int j = 0; j < this.kolom; j++){
				if(data[i][j] != null){
					System.out.print(this.data[i][j]+"\t");
				}
				else {
					System.out.print("\t");
				}
			}
			System.out.println();
		}
	}
	
	public static void main(String[] args){
		Template template = new Template();
		template.setData(3);
		template.showData();
	}

}

```

> by Masyda Arrizaqu 