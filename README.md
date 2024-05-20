#include<stdio.h>
#include<stdlib.h>

int  menu();
void primos1();
void primos_rango();
int main(){
	int op;
	do{
		system("pause");
		system("cls");
		op=menu();
		
		if(op==1){
			primos1();
			
		}
		else if(op==2){
			primos_rango();
		}
		else system("cls"); printf("Sistema usado");
		
	}while(op!=3);
}
int menu(){
	int x;
	printf("Ingrese el 1 para mostrar numero primos hasta un numero");
	printf("\nIngrese el 2 para numeros primos en un rango seleccionado");
	printf("\nIngrese el 3 para salir del programa:");
	scanf("%d",&x);
	return x;
}
void primos1(){
	system("cls");
	system("pause");
	int num;
    printf("Ingrese un numero: ");
    scanf("%d", &num);
    for (int i = 0; i <= num; i++) {
        if (i <= 1) {
            continue; 
        }
        int primo = 1;
        for (int a = 2; a * a <= i; a++) {
            if (i % a == 0) {
                primo = 0;
                break;
            }
        }
        if (primo) {
            printf("%d\n", i);
        }
    }
}
void primos_rango(){
	system("pause");
	system("cls");
	int num1, num2, temp;
    printf("Ingrese el primer numero: ");
    scanf("%d", &num1);
    printf("Ingrese el segundo numero: ");
    scanf("%d", &num2);
    if (num1 > num2) {
        int temp = num1;
        num1 = num2;
        num2 = temp;
    }
    for (int i = num1; i <= num2; i++) {
        int primo = 1;
        for (int a = 2; a * a <= i; a++) {
            if (i % a == 0) {
                primo = 0;
                break;
            }
        }
        if (primo) {
            printf("%d\n", i);
        }
    }

	
	
}
