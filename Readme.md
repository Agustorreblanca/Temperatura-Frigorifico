
```c
#include <stdio.h>
#include <stdlib.h>
#include "lib.h"
#define T 10
int main()
{

    printf("|||Medicion de temperatura||| \n");
    system("pause \n");
   int minutos=0, segundos=0,Minutos=0, Segundos=0, Ts;
         srand(time(NULL));
        Ts=rand()%15;
        printf("La temperatura medida es : %d grados \n", Ts);
        system("pause");
        while (Minutos<3&&Ts>Tconfig+DeltaT)
        {
            printf("\n Refrigeracion activa \n");
            Segundos=60;
            if(Segundos==60)
            {

                Minutos++;
                Segundos=0;
                Ts=funcionarefri(Ts);
                system("Pause \n");

            }
            printf(">> Tiempo transcurrido: %d minutos << \n", Minutos);

        if(Minutos >=3 && Ts>Tconfig+DeltaT)
        {

            printf("|||||Alarma por Alta temperatura activa|||||");
        }
        if(Minutos<3 && Ts<Tconfig+DeltaT)
        {
            printf("La nueva temperatura es: %d \n", Ts);
            printf("La temperatura se regulo a %d ....", Ts);
        }
        }

        while(minutos<3 && Ts<Tconfig-DeltaT)
        {
            printf("!!!!!!!Filtro de aire activado!!!!!!! \n");
            segundos=60;
            if(segundos==60)
            {
                minutos++;
             segundos=0;
             Ts=tempfiltro(Ts);
            }
            printf("\n Nueva temperatura leida en la camara  ''''%d''''' grado(s) ", Ts );
            printf("\n Tiempo transcurrido : %d   Minuto(s) \n", minutos);
            system("pause");
            if(minutos==3&&Ts<Tconfig-DeltaT)
            {
             printf("||Alarma encendida por falta de calor||");
             system("Pause");
            }
            if (minutos<3&& Ts>Tconfig-DeltaT)
            {
             printf(" \n |||Temperatura regulada a %d grados|||", Ts );
            }

        }

    return 0;
}
```