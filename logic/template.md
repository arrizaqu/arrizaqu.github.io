# logic 
> Untuk mengerjakan logic bintang seperti 
```
	@	 	 	 	@	 	 	 	@	
		@	 	 	@	 	 	@	 	
			@	 	@	 	@	 	 	
				@	@	@	 	 	 	
	@	@	@	@	@	@	@	@	@	
				@	@	@	 	 	 	
			@	 	@	 	@	 	 	
		@	 	 	@	 	 	@	 	
	@	 	 	 	@	 	 	 	@
```
## Step Pengerjaan
* Menentukan panjang baris dan Kolom
* Menentukan panjang Array

### Menentukan panjang baris dan Kolom
	Memberikan Default nilai untuk nilai baris dan kolom adalah 0
```java
	int baris = 0;
	int kolom = 0;
end
```

### Menentukan panjang Array
	demikian pula untuk panjang nilai pada array
```java
	String[][] data = null;
end
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