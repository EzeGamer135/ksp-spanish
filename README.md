# Kerbal Space Program

## Delta-V
### ¿Qué es el Delta-V?
La Wikipedia define el delta-v como una medida escalar del "esfuerzo" necesario para llevar a cabo una maniobra orbital. Se expresa en metros por segundo.
### ¿Por qué es importante?
Porque esa medida se comporta como el "combustible" de tu nave: tienes una cierta cantidad de delta-v al principio, y lo vas gastando conforme haces maniobras. Pero es mucho mejor hablar de delta-v que de combustible porque el delta-v ya incluye el peso de tu nave y eficiencia de tus motores.

Por ejemplo, ¿cuánto combustible necesitas para poner un satélite en una órbita estable a 80 km de Kerbin? Pues dependiendo del peso de tu satélite y de si usas motores nucleares, de combustible líquido o turbina, la respuesta puede variar entre unos cientos de litros, a decenas de miles.

Replanteamos la pregunta. ¿Cuánto delta-v necesitas para poner un satélite en una órbita estable a 80 km de Kerbin? Pues unos 3400 m/s , independientemente de si estás lanzando el satélite más pequeño jamás creado, o uno del tamaño de un tren de mercancías.

Obviamente, si tu nave es más grande, necesitarás más litros de combustible para conseguir los 3400 m/s de delta-v Además, cuanto más eficientes sean tus motores, más delta-v conseguirás para la misma cantidad de combustible. Pero una vez en la rampa, sabes que tienes que gastar 3400 m/s para ponerte en órbita.

Bien, ¿dónde quieres ir? Sea cual sea tu destino, deberías echarle un vistazo a un mapa de Delta-V:

![](https://i.imgur.com/yO0bQax.png)

Imagina que quieres construir un cohete capaz de alunizar en Minmus. Para realizar las maniobras necesarias, deberás gastar la siguiente cantidad de delta-v :

- 3400 m/s para alcanzar una órbita estable.
- 930 m/s para hacer la transferencia.
- 160 para ponerte en una órbita a bajo nivel.
- 180 m/s para conseguir aterrizar.

En total, tu cohete deberá gastar un mínimo de 4670 m/s desde que enciendes los motores para despegar, hasta que te poses en Minmus. Si además quieres volver, tendrás que sumar los delta-v de vuelta (excepto los 3400 de Kerbin, porque usarás la atmósfera para frenar).

### ¿Qué influye en el Delta V?

Los principales parámetros que influyen en tu delta v son:

- La masa "en seco" (sin combustible) de tu cohete.
- La cantidad de combustible que llevas.
- La eficiencia de tus motores.

El cálculo exacto del delta-v está fuera del alcance de este tutorial. Usa el mod Mechjeb o Kerbal Engineer Redux para obtener un análisis por etapas del delta-v de tu cohete. A continuación tienes un ejemplo de Mechjeb:

![](https://steamuserimages-a.akamaihd.net/ugc/450667408635779902/A956D268D012ABEB792E72E7330C630928657F78/)

Las dos primeras líneas muestran el delta-v de la etapa actual y de toda la nave. La eficiencia de los motores suele variar mucho si estás en atmósfera o en el vacío, así que se suelen dar dos valores de delta-v: atmosférico y en el vacío.

Después tienes un desglose del delta-v por etapas. En la etapa actual (número 2) me quedan 7248 m/s, suficiente para llegar a casi cualquier planeta del sistema solar. La etapa 1 es una etapa de transición, así que no tiene delta-v La última etapa, la 0, es un lander pesado, diseñado para aterrizar (¡y luego volver!) de lunas o planetas con una gravedad media o baja.

El otro valor que se muestra, el TWR, lo describo en el apartado siguiente.

### ¿Cómo varía el delta-v?

- Cada vez que enciendes tus motores para realizar una maniobra, gastas delta-V.
- Cada vez que te desprendes de masa (por ejemplo, eliminando un depósito de combustible vacío), ganas delta-v.
- Cada vez que cargas combustible (abasteciendo el cohete en órbita, por ejemplo), ganas delta-v.

A igualdad de masa "seca" y combustible, cuanto más eficientes sean tus motores, más delta-v tendrás disponible.

## TWR
### ¿Por qué es importante el TWR?
Para despegar desde la superficie de Kerbin con un ingenio sin sustentación aerodinámica (es decir, cualquier cohete) necesitas un TWR superior a 1.0
### ¿Qué influye en el TWR?
- El peso de tu nave.
- El impulso de tus motores.
### ¿Cómo varía el TWR?
Una vez has conseguido despegar de la superficie, el TWR se reducirá porque 1) tu cohete consumirá combustible, así que reducirá su masa y por tanto su peso 2) el campo gravitatorio del planeta se debilita según te alejas, por lo que el peso se reduce.

En superficie, tu TWR es crítico, porque indica si tu cohete será capaz de levantarse del suelo, o no. En el espacio no tienes que preocuparte del TWR. Si tu TWR es bajo es porque tus motores no generan mucho impulso. Cuando vayas a hacer una maniobra, tendrás que tenerlos encendidos más tiempo, lo que no es un problema.
## Motores y Fases
Hay tres reglas básicas:

- Cada gramo de combustible que añades aumenta tu delta-v, y reduce tu TWR.
- Cada motor que añades reduce tu delta-v y aumenta tu TWR.
- Cada gramo que no es combustible ni motor reduce tu delta-v y tu TWR.

Necesitas un TWR mayor de uno para despegar de Kerbin, es aconsejable un mínimo de 1.5 o 2.

Necesitas suficiente delta-v para llevar a cabo todas las maniobras necesarias para cumplir el objetivo de tu misión. Ten en cuenta que los mapas dan el delta-v necesario si realizas las maniobras de la forma más eficiente. Créeme, es mucho pedir para un novato, así que **vete siempre con una cantidad extra de delta-v**.

Como puedes ver, los dos parámetros fundamentales dependen directa o indirectamente de la masa de tu nave. Es muy importante librarse de todo aquello que no necesites, especialmente depósitos de combustible vacíos y motores que no vayas a usar más.

Por eso los cohetes se construyen en fases. La primera fase suele ser la encargada de sacar la nave de la tierra, para lo que se necesitan motores muy potentes (pero poco eficientes) que te den suficiente TWR para vencer el campo gravitatorio de la tierra. Pero una vez en el espacio, la eficiencia pasa a ser el factor clave, así que debes librarte del peso muerto y maniobrar con motores más pequeños y eficientes.

La elección de los motores para cada fase es crucial en el diseño del cohete. Voy a hacer un pequeño resumen de cada tipo de motor, válido para la versión 0.20.

- Los motores líquidos consumen una mezcla de combustible líquido y oxidante. Son el tipo de motor estándar y vienen en tres tamaños. Las versiones grandes son potentes (**mucho TWR y poco delta-v**) así que son apropiadas para las **primeras etapas** del cohete. Las pequeñas tienen menos TWR, pero son más eficientes y por tanto te dan más delta-v **con el mismo combustible**.
- Los motores de combustible sólido son muy potentes, pero tienen el grave inconveniente de que una vez encendidos no se pueden apagar ni regular. Normalmente, se usan para reforzar las primeras etapas del cohete, cuando más empuje necesitas.
- Los motores nucleares son mucho más eficientes que los líquidos "normales", pero tienen muy poco empuje. Son ideales (¿necesarios?) para viajes interplanetarios, donde la eficiencia es crítica. Sólo consumen combustible líquido.
- Los "aerospike" son un tipo de motor líquido muy eficiente en atmósfera. Se suelen utilizar en los módulos de aterrizaje para planetas y lunas con atmósfera, como Duna.
- Las turbinas (motores "jet") consumen combustible líquido y toman el oxígeno de la atmósfera. Por tanto, necesitan una atmósfera con oxígeno :P (Kerbin, Lathye y no sé si me dejo alguno). Suelen emplearse en aviones y, a veces, en las primeras fases de los cohetes.
- Los motores de iones consumen gas Xeon. Son los más eficientes de todos, pero tienen tan poco empuje que prácticamente sólo se usan en satélites y sondas, o para ajustes de órbita.

Bueno, con esto tienes lo necesario para plantar un cohete en cualquier sitio del sistema solar. Suerte por ahí fuera :)
