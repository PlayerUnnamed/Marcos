#include <stdio.h>
#include <stdlib.h>
#include <conio.h>
#include <locale.h>



int main() {
    int an,a1,n,r,opcao,elemento,x;
    setlocale(LC_ALL,"Portuguese");
    system("color 04");
    
    do{
        printf("1-an a1 n (falta r)\n");
        printf("2-an a1 r (falta n)\n");
        printf("3-an r m (falta a1)\n");
        printf("4-a r m (falta an)\n");
        scanf("%d",opcao);
    }while(opcao<1||opcao>4);
     switch (opcao){
         case 1:
             printf("informe a1");
             scanf("%d",&a1);
             prinft("informe an");
             scanf("%d",&an);
             printf("informe n");
             scanf("%d",&n);
             printf("informe r");
             scanf("%d",&r);
             r=(an-a1)/(n-1);
             printf("r eh igual a %d",r);
             prinft("o somatorio eh %d", (n*(a1+an))/2);
             break;
             
         case 2:
             printf("informe a1");
             scanf("%d",&a1);
             prinft("informe an");
             scanf("%d",&an);
             printf("informe n");
             scanf("%d",&n);
             printf("informe r");
             scanf("%d",&r);
             n=(an-a1)/(n+1);
             printf("n eh igual a %d",n);
             prinft("o somatorio eh %d", (n*(a1+an))/2);
             break;
             
         case 3:
             printf("informe a1");
             scanf("%d",&a1);
             prinft("informe an");
             scanf("%d",&an);
             printf("informe n");
             scanf("%d",&n);
             printf("informe r");
             scanf("%d",&r);
             a1=an-(n-1)*r;
             printf("a1 eh igual a %d",a1);
             prinft("o somatorio eh %d", (n*(a1+an))/2);
             break;
             
         default:
             printf("informe a1");
             scanf("%d",&a1);
             prinft("informe an");
             scanf("%d",&an);
             printf("informe n");
             scanf("%d",&n);
             printf("informe r");
             scanf("%d",&r);
             a1=an-(n-1)*r;
             printf("an eh igual a %d",an);
             prinft("o somatorio eh %d", (n*(a1+an))/2);
             break;
             do{
             prinft("informe o elemento entre o primeiro e o elemento %d",n);
             scanf("%d",&elemento);
             }while(elemento<n);
             x=a1;
             int i=1;
             for(i=1;i<elemento;i++){
                 x +=r;
             }
             printf("valor do %d", elemento,x);
     
    }
    return 0;
}
