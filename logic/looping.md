# Looping
* Definition 
* Loop level 1
* Loop level 2
* Loop level 3

## Definition 
Secara singkat Looping merupakan pengulangan sesuatu atau serangkaian "kerja" dari program.

## Loop level 1
Misalkan sebuah tanda "*" akan di loop sebanyak 5x seperti code dibawah: 
```java
for(int i = 0; i < 5; i++){
	System.out.print("*");
}	
```
maka output yang dihasilkan adalah : 
```js
*****
```

## Loop level 2
Yup, next level 2, maksudnya adalah apa yang terjadi jika hasil pada "Loop level 1" seperti : 
```js
*****
```
akan di loop lagi sebanyak 3x, hingga memiliki : 
```js
***** ***** *****
```

maka code nya adalah : 
```java
for(int i = 0; i < 3; i++){
	for(int j = 0; j < 5; j++){
		System.out.print("*");
	}
}
```

### Loop Level 3 
Apa yang terjadi jika level di naikknya 1 lagi, maka akan terbentuk 3 for loop, dan misalkan hasil sebelumnya di loop 2x lagi, maka output : 
```js
***** ***** ***** ***** ***** *****
```
maka code nya adalah sebagai berikut : 
```java
for(int bangun = 0; bangun < 2; bangun++){
	for(int i = 0; i < 3; i++){
		for(int j = 0; j < 5; j++){
			System.out.print("*");
		}
	}
}
```

dan seterusnya.., 

### Basic Logic
loop seperti ini adalah bagian basic untuk mengerjakan logic bintang dengan menggunakan Loop., 
```java
for(int i = 0; i < 3; i++){
	for(int j = 0; j < 5; j++){
		System.out.print("*");
	}
	System.out.println("\t");
} 
```
output: 
```js
* * * * * 
* * * * * 
* * * * *
```
 
