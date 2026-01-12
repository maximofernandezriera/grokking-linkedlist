# Arrays y listas enlazadas de Grokking Algorithms

# Para afrontar https://www.codewars.com/kata/55d17ddd6d7868493e000074/train/java 

A veces necesitas almacenar una lista de elementos en la memoria. Supongamos que estás escribiendo una aplicación para gestionar tus tareas pendientes. Querrás almacenar las tareas como una lista en la memoria.

¿Deberías usar un array o una lista enlazada? Almacenemos las tareas en un array primero, porque es más fácil de entender. Usar un array significa que todas tus tareas están almacenadas de forma contigua (una al lado de la otra) en la memoria.

Ahora supongamos que quieres añadir una cuarta tarea. ¡Pero el siguiente "cajón" está ocupado por las cosas de otra persona!

Es como ir al cine con tus amigos y buscar un lugar para sentarse, pero se une otro amigo, y no hay lugar para él. Tienes que moverte a un nuevo lugar donde todos quepan. En este caso, necesitas pedirle a tu computadora un bloque diferente de memoria que pueda alojar cuatro tareas. Luego, tienes que mover todas tus tareas allí.

Si otro amigo viene, te quedas sin espacio de nuevo, ¡y todos tienen que moverse por segunda vez! Qué dolor. De manera similar, añadir nuevos ítems a un array puede ser muy molesto. Si te quedas sin espacio y necesitas moverte a un nuevo lugar en la memoria cada vez, añadir un nuevo ítem será realmente lento. Una solución fácil es "reservar asientos": incluso si solo tienes 3 ítems en tu lista de tareas, puedes pedirle a la computadora 10 espacios, por si acaso. Entonces puedes añadir 10 ítems a tu lista de tareas sin tener que moverte. Esta es una buena solución, pero debes estar consciente de un par de inconvenientes:
- Puede que no necesites los espacios extras que pediste, y entonces esa memoria se desperdiciará. No la estás usando, pero nadie más puede usarla tampoco.
- Puedes añadir más de 10 ítems a tu lista de tareas y tener que moverte de todos modos.

Así que es una buena solución, pero no es perfecta. Las listas enlazadas solucionan este problema de añadir ítems.

## Listas enlazadas

Con las listas enlazadas, tus ítems pueden estar en cualquier lugar de la memoria. Cada ítem almacena la dirección del siguiente ítem en la lista. Un montón de direcciones de memoria aleatorias están enlazadas entre sí.

Es como una búsqueda del tesoro. Vas a la primera dirección, y dice: "El siguiente ítem se puede encontrar en la dirección 123". Así que vas a la dirección 123, y dice: "El siguiente ítem se puede encontrar en la dirección 847", y así sucesivamente. Añadir un ítem a una lista enlazada es fácil: lo colocas en cualquier lugar de la memoria y almacenas la dirección con el ítem anterior.

Con las listas enlazadas, nunca tienes que mover tus ítems. También evitas otro problema. Digamos que vas a una película popular con cinco de tus amigos. Los seis intentan encontrar un lugar para sentarse, pero el teatro está lleno. No hay seis asientos juntos. Bueno, a veces esto sucede con los arrays. Digamos que estás tratando de encontrar 10,000 espacios para un array. Tu memoria tiene 10,000 espacios, pero no tiene 10,000 espacios juntos. ¡No puedes conseguir espacio para tu array! Una lista enlazada es como decir: "Dividámonos y veamos la película". Si hay espacio en la memoria, tienes espacio para tu lista enlazada.

Si las listas enlazadas son mucho mejores para insertar, ¿para qué son buenos los arrays?

## Arrays

Los sitios web con listas de los 10 mejores usan una táctica desagradable para obtener más vistas de página. En lugar de mostrarte la lista en una página, ponen un ítem en cada página y te hacen hacer clic en Siguiente para llegar al siguiente ítem de la lista. Por ejemplo, Los 10 mejores villanos de la televisión no te mostrarán la lista entera en una página. En su lugar, comienzas en el #10 (Newman), y tienes que hacer clic en Siguiente en cada página para llegar al #1 (Gustavo Fring). Esta técnica les da a los sitios web 10 páginas enteras en las que mostrarte anuncios, pero es aburrido hacer clic en Siguiente 9 veces para llegar al #1. Sería mucho mejor si toda la lista estuviera en una página y pudieras hacer clic en el nombre de cada persona para obtener más información.

Las listas enlazadas tienen un problema similar. Supongamos que quieres leer el último ítem en una lista enlazada. No puedes simplemente leerlo, porque no sabes en qué dirección está. En cambio, tienes que ir al ítem #1 para obtener la dirección del ítem #2. Luego tienes que ir al ítem #2 para obtener la dirección del ítem #3. Y así sucesivamente, hasta llegar al último ítem. Las listas enlazadas son geniales si vas a leer todos los ítems uno por uno: puedes leer un ítem, seguir la dirección al siguiente ítem, y así sucesivamente. Pero si vas a saltar de un ítem a otro, las listas enlazadas son terribles.

Los arrays son diferentes. Conoces la dirección de cada ítem en tu array. Por ejemplo, supongamos que tu array contiene cinco ítems, y sabes que comienza en la dirección 00. ¿Cuál es la dirección del ítem #5?

La matemática simple te lo dice: es el 04. Los arrays son geniales si quieres leer elementos aleatorios, porque puedes buscar cualquier elemento en tu array instantáneamente. Con una lista enlazada, los elementos no están uno al lado del otro, así que no puedes calcular instantáneamente la posición del quinto elemento en la memoria; tienes que ir al primer elemento para obtener la dirección al segundo elemento, luego ir al segundo elemento para obtener la dirección del tercer elemento, y así sucesivamente hasta llegar al quinto elemento.

### Importante: https://www.it.uc3m.es/java/2012-13/units/pilas-colas/guides/2/guide_es_solution.html
