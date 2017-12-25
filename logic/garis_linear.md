# Logic Bintang Garis Linear  
* 	Kebutuhan
*	output yang diharapkan 
* 	Formula Logika
	* garis diagonal 1 (naik ke kiri)
	* garis diagonal 2 (naik ke kanan)
	* garis tengah (horizontal)
	* garis tengah (vertical)

## Kebutuhan
Mengerti bagaimana konsep data Array pada template logic bintang.
	
## Output yang diharapkan
```java
*	 	*	 	*
 	*	*	*	 
*	*	*	*	*
 	*	*	*	 
*	 	*	 	*
```

## Formula Logika
### garis diagonal 1 (naik ke kiri)
```js
	i == j
```

### garis diagonal 2 (naik ke kanan)
```js
	i + j == n - 1
```

### garis tengah (horizontal)
```js
	i == n / 2
```

### garis tengah (vertical)
```js
	j == n / 2
```

> by Masyda Arrizaqu 