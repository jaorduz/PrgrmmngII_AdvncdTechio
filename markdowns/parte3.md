# Statements: for, if, if-else-if, do-while, while

Different statements are outstanding for programming. 
We shall check some examples with the previous 
statements:

# for statements

```C runnable
#include <stdio.h>

int main() {
int i=0;

for(int i =0;i<=2;i++){
	printf("Hi, World!");
}

	return 0;
}

```
 






#






<!---
Acceso a miembros privados de una clase: Funciones y Clases "Amigas"

Una función o una clase "Amiga" es aquella a la que se le ha otorgado la capacidad de tener acceso a los miembros privados de la clase que la
ha declarado como amiga. Para que una clase declare a otra clase o a una función como amiga se debe declarar esa función o esa clase al interior de
la clase y se debe utilizar la palabra reservada `friend` en esa declaración.

Nota: La amistad en C++ es unívoca, es decir, si la clase A declara a la clase B como amiga eso no quiere decir que la clase B considere a la clase A
como amiga.

Las funciones amigas o los métodos de una clase amiga pueden en ocasiones recibir como parámetro de entrada una referencia a un objeto de la clase que las declaro como amigos.

Declaración de una función amiga:

```C++ runnable
#include<iostream>

using namespace std;

class MiClase
{
	public:
	void printMembers();
	friend void funcionAmiga(int x, MiClase& mc); //Se usa la palabra friend y uno de los parámetros es una referencia a la clase MiClase
	private:
	int a;
};

void MiClase::printMembers()
{
	cout<<"El valor de 'a' es: "<<a<<endl;
}

void funcionAmiga(int x, MiClase& mc)
{
	mc.a = x; //Acceso a un miembro privado del objeto mc de la clase MiClase
}

int main()
{
	MiClase obj;
	funcionAmiga(5, obj);
	obj.printMembers();
	
	return 0;
}
```
Declaración de una clase amiga:

```C++ runnable
#include<iostream>

using namespace std;

class MiClase
{
	public:
	void printMembers();
	friend class OtraClase; //Se usa la palabra friend y se nombra la clase amiga
	private:
	int a;
};

void MiClase::printMembers()
{
	cout<<"El valor de 'a' es: "<<a<<endl;
}

class OtraClase
{
	public:
	void metodoClaseAmiga(int x, MiClase& mc);
};

void OtraClase::metodoClaseAmiga(int x, MiClase& mc)
{
	mc.a = x; //Acceso a un miembro privado del objeto mc de la clase MiClase
}

int main()
{
	MiClase obj;
	OtraClase obj2;
	obj2.metodoClaseAmiga(10, obj);
	obj.printMembers();
	
	return 0;
}
```
--->