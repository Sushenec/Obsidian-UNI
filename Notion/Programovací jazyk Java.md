- OOP jazyk
- převod do byte code
- JVM
- Oracle
- grabage collector - čistí data

## Implementace Javy

- JRE
- JDK
- OpenJDK

## Virtuální stroj

- JVM
- Mezikód - Java bytecode
- Kompilace do binárního tvaru (soubory s příponou*class)
- přípona .jar
- Přenositelnost

# Třídy a objekty

- Komunikace mez objekty

### Objekt

- Konkrétní jev
- atributy - vlastnosti
- metody - reakce na okolí
- vztahy mezi objekty

### Třída

- Obecnější koncept
- instance třídy - konkrétní jev
- **Přístupová práva**
    - private
    - public
    - protected

## UML

- Unified Modeling Language
- UML jako náčrt
- UML jako plán
- UML jako programovací jazyk

![[image 11.png]]

  

## Přístupová práva

- - (mínus) private - privátní atribut nebo metoda
- + (plus) public - veřejná atribut nebo metoda
- # (hash) protected - chráněný atribut nebo metoda
- ~ (tilda) atribut viditelný v rámci balíčku

## Metody

- Schopnost něco dělat
- Getter
- Setter
- Přístupové a změnové metody
- Velbloudí notace
    - Třídy začínají velkým písmenem
    - Metody a proměnné začínají malým písmenem

```Java
public int nejakMetoda(int nejakyParametr){
	//kod metody
	return cislo;
}
```

## Datové typy

- int
- double
- String
- void

  

## Konstruktor

- Vytváří objekt
- Vyhradí paměť pro objekt
- Může inicializovat atributy objektu
    - Implicitní konstruktory
    - Vlastní konstruktory

```Java
public class Rectangle {
	private int a;
	private int b;
	
	//Konstrukor
	public Rectangle(int a, int b){
		this.a = a;
		this.b = b;
	}
	public void setA(int a) {
		this.a = a;
	}

}
```

### Přetížený konstruktor

- Stejný název
- Liší se v počtu nebo typu parametrů

```Java
public Rectangle(int a, int b){
	setA(a);
	setB(b);
}

public Rectangle(){
	setA(1);
	setB(2);	
}
//copy constructor
public Rectangle(Rectangle rectangle){
	setA(rectangle.getA());
	setB(rectangle.getB());
}
```