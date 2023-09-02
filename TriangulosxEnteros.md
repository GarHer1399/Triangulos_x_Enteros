Se presenta el codigo para obtener los posibles Triangulos en base a el entero ingresado en los lenguajes de programacion solicitados y pseudocodigo.

**PSEUDOCODIGO**

Ingrese un numero entero positivo:
Si numero < 1 entonces
    Escribir "El numero ingresado no es positivo."
Sino
    Escribir "Triangulo 1:"
    Para i desde 1 hasta numero Hacer
        Escribir "* " * i
    Fin Para

    Escribir "Triangulo 2:"
    Para i desde numero hasta 1 con paso -1 Hacer
        Escribir "* " * i
    Fin Para

    Escribir "Triangulo 3:"
    Para i desde 1 hasta numero Hacer
        Escribir "  " * (numero - i) + "* " * i
    Fin Para

    Escribir "Triangulo 4:"
    Para i desde numero hasta 1 con paso -1 Hacer
        Escribir "  " * (numero - i) + "* " * i
    Fin Para
Fin Si


---------------------------------------------------------------------------------------------------------------------------------------

**PYTHON**


numero = int(input("Ingrese un numero entero positivo: "))

if numero < 1:
    print("El numero ingresado no es positivo.")
else:
    print("Triangulo 1:")
    for i in range(1, numero + 1):
        print("* " * i)

    print("Triangulo 2:")
    for i in range(numero, 0, -1):
        print("* " * i)

    print("Triangulo 3:")
    for i in range(1, numero + 1):
        print("  " * (numero - i) + "* " * i)

    print("Triangulo 4:")
    for i in range(numero, 0, -1):
        print("  " * (numero - i) + "* " * i)




---------------------------------------------------------------------------------------------------------------------------------------------

**C++**


#include <iostream>
using namespace std;

int main() {
    int numero;
    cout << "Ingrese un numero entero: ";
    cin >> numero;

    if (numero < 1) {
        cout << "El numero ingresado no es positivo." << endl;
        return 1;
    }

    cout << "Triangulo 1:" << endl;
    for (int i = 1; i <= numero; i++) {
        for (int j = 1; j <= i; j++) {
            cout << "* ";
        }
        cout << endl;
    }

    cout << "Triangulo 2:" << endl;
    for (int i = numero; i >= 1; i--) {
        for (int j = 1; j <= i; j++) {
            cout << "* ";
        }
        cout << endl;
    }

    cout << "Triangulo 3:" << endl;
    for (int i = 1; i <= numero; i++) {
        for (int j = numero; j > i; j--) {
            cout << "  ";
        }
        for (int k = 1; k <= i; k++) {
            cout << "* ";
        }
        cout << endl;
    }

    cout << "Triangulo 4:" << endl;
    for (int i = numero; i >= 1; i--) {
        for (int j = numero; j > i; j--) {
            cout << "  ";
        }
        for (int k = 1; k <= i; k++) {
            cout << "* ";
        }
        cout << endl;
    }

    return 0;
}


