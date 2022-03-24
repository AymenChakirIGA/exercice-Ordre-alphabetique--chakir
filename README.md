 exercice-Ordre-alphabetique--chakir
// Methode 1 : utilisation de STRCMP
//Pour comparer deux chaine de caractere on utilise la fonction 'strcmp' 

#include<stdio.h>
#include<stdlib.h>
#include<string.h>
int main (){
    char txt1[25],txt2[25] ;
    
    printf("donner le premier text ");
    gets(txt1);
    printf("donner le 2eme text ");
    gets(txt2);
    if (strcmp(txt1,txt2)<0){    // on a utiliser '<' car la fonction strcmp(x1,x2) compare x2 par x1 pas l'inverse 
        printf("%s\n %s" , txt1 , txt2);
}
else
{
    printf("%s\n %s \n" , txt2 , txt1);
    }
    system("pause");
    return 0;
}


//Methode 2 : Utilisation des tableaux
#include<stdio.h>
#include<stdlib.h>
#include<string.h>
int main(){
        char txt1[25] , txt2[25];
        int i , j , M , N;
        gets(txt1);
        gets(txt2);
        j = 0;
        i = 0;
        int x = 0, y = 0;
        N = strlen(txt1);
        M =  strlen(txt2);
        while (i<N && j<M){
               
               if (txt1[i]< txt2[j]){ // Jsp pour quoi mais si on fais txt1[i]< txt2[j] le programe va realiser corectement 
                  x++;
                  break;          
          }
              else if (txt1[i]> txt2[j]){
                   y++; 
                   break;
              }
              else {
                   i++;
                   j++;
                   }
        }
        if (x == 1)
        {
              puts(txt1);
               puts(txt2);
              }
        else if ( y == 1)
        {
             puts(txt2);
               puts(txt1);
             }
        else {
             printf("egals");
             }
        system ("pause");
        return 0;
}

               
            
