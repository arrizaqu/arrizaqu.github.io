# Looping
* Definition 
* Next Level

## Definition 
Secara singkat Looping merupakan pengulangan sesuatu atau serangkaian "kerja" dari program.
Misalkan sebuah tanda "*" maka : 
```java
for(int i = 0; i < 5; i++){
	System.out.print("*");
}	
```
output : 
```js
*****
```

## Next Level
Yup, next level, maksudnya adalah apa yang terjadi jika hasil loop berupa output : 
```js
*****
```
akan di loop lagi sebanyak n, hingga memiliki : 
```js
***** ***** ***** ..(nx)
```

### example : 
```java
for(int a = 0; a < n; a++){
	for(int i = 0; i < 5; i++){
		System.out.print("*");
	}
}
```