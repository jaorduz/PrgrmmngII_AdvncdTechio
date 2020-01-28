![LogoGCCyC](/figs/logosNB.png)


# Contents <a name="inicio"></a>

1. [Data type](#Data_type)



# Data type <a name="Data_type"></a>

Consider the type: _int_, _float_ and...

?[What are the other types?]
-[ ] main, string, char
-[x] double, char, bool
-[ ] String, return, sizeof
-[ ] stdio.h, printf, Bool


1. Fix the next code to get the size of a. 

```C runnable

#include<stdio.h>
int main(){

  int a = 2;
   b =sizeof(a); 
  printf("salida %i. El tamanio es: %i Bytes\n" a, b)
  
  return 0;
}

```
2. Repair the follow code to get the values and size of _A_ and _a_.

```C runnable
#include <stdio.h>

int main(){

int A, a;

A = 2
a = 3; 

printf("A=\n", A);
printf("a=%i\n", a);

   return 0;
}
```



3. Organize the code in the correct form:

```C runnable
#include <stdio.h>
    return 0;
{

    bool isEven = true;
int main()

if(p==2)
else{
    printf("p=%i es Impar %i\n",p ,isEven);
{
    printf("p=%i es Par %i\n",p ,isEven);
	}
	}
    int p=3;
#include <stdbool.h>

puts("1 = true and 0 = false\n\n");
}
```


4. Arrange  the code in the correct form:

```C runnable
// Biblioteca




// Declaracion de la funcion

void func(void);

// Definicion de la funcion funcion principal
int main(){
   while(count--) {
   }

   return 0;


     func(); // llamar la funcion
static int count = 5; // variable global 

}

// Definicion de la funcion

   printf("i es %d y la cuenta es %d\n", i, count);
   register int i = 5; //variable local register(static)


void func( void ) {

   i++;

}
#include <stdio.h>

```


Go <a href="#inicio">Up</a>





<!---
Clase:
![analog clase](/img/car_class.png)

Objetos:
![analog objeto1](/img/car_obj1.png)
![analog objeto2](/img/car_obj2.png)

```cpp
class MiClase
{
  //Aquí van los miembros de la clase: Variables y funciones
}; //NO olvidar el ;
```
Los objetos, tal como se había mencionado con anterioridad, son variables (instancias) del tipo de dato definido por una clase. Por tanto, los
objetos se pueden declarar al interior o por fuera de funciones, tal y como una variable local o global respectivamente. Pueden ser declarados
como miembros de otras clases, es decir al interior de otras clases. Luego, para declarar un objeto primero se utiliza el mobre de la clase a la
que pertenece el objeto seguido de un nombre para el objeto y de una lista opcional de inicialización entre paréntesis. Dicha lista se verá más
adelante.

```cpp
MiClase objetoGlobal;  //Declaración de un objeto global de la clase MiClase

int main()
{
	MiClase objetoLocal; //Declaración de un objeto local de la clase MiClase  
}
```
--->
