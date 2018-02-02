# Hello world dan Java Variable
* Program Main
* Java Class
* Java Variable  
* Java Object

## Program Main
Program main biasa digunakan untuk menjalan program pada saat program dijalankan untuk pertama kali, sehingga jika tidak ada program main maka program tidak akan pernah dijalankan karena program tidak mengetahui mana yang akan dijalankan terlebih dahulu.
```java
public class Main{
	public static void main(String args[]){
		System.out.println("java hello world..!!");
	}
}
```

## Java Class
Java class biasanya atau mudahnya dibuat untuk memberikan deskripsi atau gambaran terhadap object yang akan dibuat dalam system.
sebagai contoh jika ada entitas "EMPLOYEE dalam system" sehingga akan terbentuk: 
```java
public class Employee{
	long id;
	String name;
	String address;
	String phone;
	int age;
	double salary;
	void info(){
		//script..
	}
}
```

## Java Variable
Karena java merupakan salah satu pemrograman yang berorientasi Object, maka bisa jadi sebuah java variable memiliki description pada class, namun demikian java masih mempertahankan untuk type data primitive.
seperti yang sudah dicontohkan pada class EMPLOYEE diatas.
```java
	//example primitive 
	int age = 5;
	double salary = 5000.0;
	long id = 123454;
	
	//example class reference 
	Employee employee = new Employee();
	String name = new String("masyda arrizaqu");
	//bisa di shortcut menjadi
	String address = "seputih banyak";
	
```

 
