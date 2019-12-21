![LogoGCCyC](/figs/logosNB.png)

# Contents <a name="inicio"></a>

1. [Arrays](#arrays)


# Arrays <a name="arrays"></a>



those elements can be related by different operators 
through the index.
An example (it must be corrected) of an array:

```C runnable
#include <stdio.h>

int main() {
int myArray[5]={-10, -5, 0 , 5, 10}; i;

for(int i =0;i<=4;i++){
suma = myArray[i];
}
	printf("Result = ", suma);
	return 0;
}

```

Check the previous code in order to find the 0, not the last value in the array.





Go <a href="#inicio">Up</a>

<!---
Las variables de clase en C++ son datos de distinto tipo que sirven para describir el estado actual de un objeto de esa clase.
Se declaran al interior de una clase de la misma forma en que se declaran variables en una aplicación convencional de C++. Es decir,
tipo de dato (calificadores opcionales), nombre para la variable y un valor inicial opcional.

Los métodos de una clase son funciones que sirven para manipular las variables de la clase, de ahí viene la primera característica relevante
de la programación orientada a objetos que es el `encapsulamiento`, ya que en lo posible se va a tratar de que solo pueda accederse a una
variable de clase a través de un método de la clase. Los métodos se declaran y definen de la misma manera que una función cualquiera en una
aplicación convencional de C++, dicho de otro modo, en su firma expresan el tipo del valor de retorno, un nombre para el método y una lista
de parámetros de entrada. Usualmente se hace la declaración de los métodos al interior de la clase, mientras que la definición se hace por fuera
de la clase ayudandose del operador de resolución de ámbito `::` para indicar que el método que se está definiendo pertenece a la clase en cuestión.

```cpp
class MiClase
{
	int var1; //Variable de clase
	const double var2 = 3.14159;  //Variable de clase
	
	void cambiarVar1(int a); //Declaración de un método de la clase
	double calcularArea(const double& x, const double& y); //Declaración de un método de la clase
};

void MiClase::cambiarVar1(int a)  //Definición del método por fuera de la clase
{
	var1 = a;
}

double MiClase::calcularArea(const double& x, const double& y) //Definición del método por fuera de la clase
{
	return x*y*var2;
}
```

# Encapsulamiento y nivel de acceso a miembros de la clase

El acceso a los miembros de una clase solo puede lograrse a través de una instancia de esa clase, es decir, de un objeto de dicha clase.
De modo que para acceder a un miembro en específico de una clase se llama al objeto recién declarado y con ayuda del operador punto `.` se hace
el llamado a la variable o método al cual se requiere acceder.

```cpp
int main()
{
	MiClase miObjeto; //Declarando un objeto de la clase
	
	miObjeto.cambiarVar1(5); //Accediendo a un miembro con el operador punto
	double var = miObjeto,calcularArea(34.6, 23.9); //Accediendo a un miembro con el operador punto
}
```

Acceso público (public) y acceso privado (private)

De momento se va a hacer enfasis en los niveles de acceso público y privado. El nivel de acceso público se expresa en la declaración de la clase 
con la palabra reservada `public` y permite que un miembro de clase sea accedido directamente a través del operador punto, usualmente los métodos
de una clase tienen este nivel acceso. Por otro lado, el nivel de acceso privado permite la ocultación de ciertos miembros de la clase y restringe
el acceso a dichos miembros a solo otros miembros de la misma clase, es decir solo puede accederse a un miembro privado de una clase mediante un miembro
público que acceda directamente a ese miembro. En este caso, al hacer un llamado directo del miembro privado con el operador punto resultará en un error
de compilación de la aplicación. EL nivel de acceso privado es el nivel de acceso por defecto de los miembros de una clase en C++ y se expresa con el uso
de la palabra reservada `private`.

```cpp
class MiClase
{
	int var1; //Acceso privado por defecto
	const double var2 = 3.14159;  //Acceso privado por defecto
	
	public: //De aquí en adelante los miembros son públicos a no ser que se exprese lo contrario
	void cambiarVar1(int a); //Acceso público
	double calcularArea(const double& x, const double& y); //Acceso público
};

void MiClase::cambiarVar1(int a)
{
	var1 = a;
}

double MiClase::calcularArea(const double& x, const double& y)
{
	return x*y*var2;
}

int main()
{
	MiClase obj;
	
	obj.cambiarVar1(100); //Ok!
	obj.var1 = 200;       //Error!
	
	return 0;
}
```
# Métodos Get y Set

Los métodos `Get` y `Set` son métodos que usualmente se definen para el acceso a una variable privada de la clase, para obtener su estado actual (valor)
y para modificarlo respectivamente.

Un método `Get` es por lo general un método con una sola línea de código que retorna el valor actual de la variable privada. Tiene valor de retorno del
mismo tipo de la variable en cuestión y en general no tiene parámetros de entrada.

Por otra parte, un método `Set` es un método en el cual por lo menos una de las líneas de código modifica directamente el valor de la variable privada.
Es poco usual que tenga valor de retorno, per sí debe tener por lo menos un parámetro de entrada para el valor con el que se modificará la variable.

```C++ runnable
#include<iostream>

using namespace std;

#define true 1
#define false 0

class OtraClase
{
	bool privateVar; //Acceso privado por defecto
	
	public: //Miembros públicos
	void setPrivateVar(bool newval); //Método Set
	bool getPrivateVar(void); //Método Get
};

void OtraClase::setPrivateVar(bool newval)
{
	privateVar = newval;
}

bool OtraClase::getPrivateVar(void)
{
	return privateVar;
}

int main()
{
	OtraClase obj;
	
	obj.setPrivateVar(true);
	cout<<obj.getPrivateVar()<<endl; //true
	obj.setPrivateVar(false);
	cout<<obj.getPrivateVar()<<endl; //false
		
	return 0;
}
```

--->
