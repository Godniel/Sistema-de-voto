//Código criado para simular uma votação eleitoral, mostrando ao final os candidatos eleitos, os votos do eleitor e estatísticas. Código criado em C

#include <stdio.h>
#include <stdlib.h>
#include <locale.h>
 
int main (){
    setlocale(LC_ALL, "Portuguese");
    
    int totalP,presidente,maeli=0,antonio=0,lissandro=0;
    int totalG,governador,maia=0,gentil=0,donaSelma=0;
    int totalS,senador,gutemberg=0,fernando=0;
    int totoalDF,deputadoF,anaVitoria=0,paulo=0;
    int totalDE,deputadoE,anaRita=0,anaG=0,adalberto=0;
    int contador = 0;
    int branco=0,nulo=0;
    int titulo;
    int totalFem,totalMasc;
   
    while(contador==0){
    printf("SEJA BEM VINDO AS ELEIÇÕES 2018 TSEc!\n\nDigite seu número do título: \n");
    scanf("%d", &titulo);
    printf("\nAgora, eleja o seu Deputado Estadual: \nSr. Adalberto (11)\nSra. Ana Guilherme (34)\nDra. Ana Rita (51)\n");
    scanf("%d", &deputadoE);
     
    switch (deputadoE){
        case 51: anaRita++;
             printf("Você votou em Dra. Ana Rita\n\n"); break;
        case 34: anaG++;
             printf("Você votou em Sra. Ana Guilherme\n\n"); break;
        case 11: adalberto++;
             printf("Você votou em Sr. Adalberto\n\n"); break;
        case 00: branco++;
             printf("Você votou em branco\n\n"); break;
        default: nulo++;
             printf("Você votou nulo\n\n"); break;
                 
    }
    system("pause");
    system("cls");
       
    printf("Agora, eleja o seu Deputado Federal: \nSr. Paulo Guilherme (33)\nSra. Ana Vitória (56)\n");
    scanf("%d", &deputadoF);
     
    switch (deputadoF){
        case 56: anaVitoria++; 
             printf("Você votou em Sra. Ana Vitória\n\n"); break;
        case 33: paulo++;
             printf("Você votou em Sr. Paulo Guilherme\n\n"); break;
        case 00: branco++;
             printf("Você votou em branco\n\n"); break;
        default: nulo++;
             printf("Você votou nulo\n\n" ); break;
    }
    
    system("pause");
    system("cls");  

    printf("Agora, eleja o seu Senador: \nSr. Gutemberg Silva (04)\nSr. Fernando Fernandes (67)\n");
    scanf("%d", &senador);
     
    switch (senador){
        case 04: gutemberg++; 
             printf("Você votou em Sr. Gutemberg Silva\n\n"); break;
        case 67: fernando++;
             printf("Você votou em Sr. Fernando Fernandes\n\n"); break;
        case 00: branco++;
             printf("Você votou em branco\n\n"); break;
        default: nulo++;
             printf("Você votou nulo\n\n"); break;
}
    printf("Agora, eleja o seu Governador: \nSr. Maia de Ana (38)\nSra. Dona Selma (18)\nSr. Gentil (40)\n");
    scanf("%d", &governador);
     
    switch (governador){
        case 38: maia++;
             printf("Você votou em Sr. Maia de Ana\n\n"); break;
        case 18: donaSelma++;
             printf("Você votou em Sra. Dona Selma\n\n"); break; 
        case 40: gentil++; 
             printf("Você votou em Sr. Gentil\n\n"); break;
        case 00: branco++;
             printf("Você votou em branco\n\n"); break;
        default: nulo++;
             printf("Você votou nulo\n\n"); break;
}    
    printf("Finalmente, eleja o seu Presidente: \nSra. Maeli (17)\nSr. Antônio (22)\nSr. Lissandro (31)\n");
    scanf("%d",&presidente);
     
    switch (presidente){
        case 17: maeli++;
             printf("Você votou em Sra. Maeli\n\n"); break;
        case 22: antonio++;
             printf("Você votou em Sr. Antônio\n\n"); break;
        case 31: lissandro++;
             printf("Você votou em Sr. Lissandro\n\n"); break;
        case 00: branco++;
             printf("Você votou em branco\n\n"); break;
        default: nulo++;
             printf("Você votou nulo\n\n"); break;
             
        system("pause");
        system("cls");
    
}
}
    //FINAL DE VOTAÇÃO, APARIÇÃO DO ESPELHO
    printf("FINAL DE VOTAÇÃO \nConfira agora seus dados e seus candidatos escolhidos: ");
    presidente==17 ?: printf("Você votou em Maeli para presidente\n");
    presidente==22 ?: printf("Você votou em Antônio para presidente\n");
    presidente==31 ?: printf("Você votou em Lissandro para presidente\n");
    presidente==00 ?: printf("Você votou em branco para presidente\n");
    presidente!=17 && presidente!=22 && presidente!=31 && presidente!=00 ?: printf("Você votou nulo para presidente\n");
     
    governador==38 ?: printf("Você votou em Maia de Ana para governador\n");
    governador==40 ?: printf("Você votou em Gentil para governador\n");
    governador==18 ?: printf("Você votou em Dona Selma para governador\n");
    governador==00 ?: printf("Você votou em branco para governador\n");
    governador!=38 && governador!=40 && governador!=18 && governador!=00 ?: printf("Você votou nulo para governador\n");
     
    senador==04 ?: printf("Você votou em Gutemberg para senador\n");
    senador==67 ?: printf("Você votou em Fernando para senador\n");
    senador==00 ?: printf("Você votou em branco para governador\n");
    senador!=04 && senador!=67 && senador!=00 ?: printf("Você votou nulo para senador\n");
     
    deputadoF==56 ?: printf("Você votou em Ana Vitória para deputado federal\n");
    deputadoF==33 ?: printf("Você votou em Paulo Guilherme para deputado federal\n");
    deputadoF==00 ?: printf("Você votou em branco para deputado federal\n");
    deputadoF!=56 && deputadoF!=33 && deputadoF!=00 ?: printf("Você votou nulo para deputado federal\n");
     
    deputadoE==51 ?: printf("Você votou em Ana Rita para deputado estadual\n");
    deputadoE==34 ?: printf("Você votou em Ana Guilherme para deputado estadual\n");
    deputadoE==11 ?: printf("Você votou em Adalberto para deputado estadual\n");
    deputadoE==00 ?: printf("Você votou em branco para deputado estadual\n");
    deputadoE!=51 && deputadoE!=34 && deputadoE!=11 && deputadoE!=00 ?: printf("Você votou nulo para deputado estadual\n");
    
    system("pause");
}   
    //DEMONSTRACAO DOS RESULTADOS

