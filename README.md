Descripción General:
Desarrollar un juego del Ahorcado utilizando un microcontrolador AVR ATMEGA2560 y el
entorno de desarrollo AVR Studio. El juego debe desplegarse en una pantalla ST7735,
mostrando tanto la animación del juego como las letras del mismo. Las palabras del juego se
almacenarán en la memoria flash del microcontrolador y se gestionarán a través de una
interfaz serial (HERCULES). Debe contar con sonidos y contadores de tiempo transcurrido.
https://www.hw-group.com/software/hercules-setup-utility
Requisitos Funcionales:
Menú de Inicio:
Al comienzo del programa, se debe reproducir un sonido de iniciación de la aplicación y
mostrar un menú en la terminal serial con las siguientes opciones:
• Presione 1 para iniciar el juego.
• Presione 2 para guardar una nueva palabra.
• Presione 3 para activar modo oculto
• Presione 4 Para desactivar modo oculto.
• Presione 5 para ver los integrantes del equipo. (ver en Terminal y LCD)
En la pantalla principal debe aparecer un mensaje de bienvenida y mostrar la opción
seleccionada desde la terminal serial, acompañada de un sonido corto almacenado en el
DFplayer, y ejecutar la tarea solicitada.
¡El futuro está en tus manos, programa con pasión y crea algo extraordinario!
Si se selecciona la opción de inicio, el juego comenzará mostrando en pantalla un contador
de tiempo transcurrido. Si se selecciona la opción número 2, se mostrará en la pantalla LCD
un mensaje indicando que se ha ingresado en modo de almacenamiento, y se enviarán por la
terminal serial las indicaciones correspondientes para almacenar palabras. Es importante
tener en cuenta que solo se pueden almacenar letras; si se ingresa un número u otro tipo de
carácter fuera del alfabeto, se mostrará un mensaje en la terminal serial indicando que el
carácter no es válido.
Si se selecciona la opción 3 o 4, se debe indicar la acción tanto en la pantalla LCD como en
la terminal serial. La opción número 5 corresponde a los créditos, y debe mostrar los nombres
de los integrantes en texto, acompañado de un sonido que represente un momento épico.
Además, se debe definir un carácter distinto al alfabeto que permita finalizar el juego en
cualquier momento, así como otro carácter que permita pausar el juego, deteniendo el
contador de tiempo. El juego solo se reanudará con la pulsación de otro carácter o el mismo
utilizado para pausar.
¡El futuro está en tus manos, programa con pasión y crea algo extraordinario!
Interacción con la Hiperterminal:
• El usuario debe poder enviar caracteres a través de la hiperterminal.
• La interfaz de la terminal debe permitir la entrada de letras para adivinar la palabra
durante el juego.
Almacenamiento de Palabras:
• Debe haber una funcionalidad para agregar nuevas palabras a través de la opción 2
del menú. Las palabras deben almacenarse en la memoria flash del microcontrolador.
Se debe contar con la opción de seleccionar el número de palabra y almacenar hasta
un máximo de 5 palabras. Al seleccionar esta opción, se enviarán por la terminal serial
las palabras previamente almacenadas. Si el número de palabra ya está almacenado,
se debe poder reemplazar la palabra existente e indicar que se actualizará.
• Si considera que esta opción se puede mejorar para hacerla más interactiva, puede
implementar las acciones adicionales que considere adecuadas.
Visualización del Juego:
La pantalla ST7735 debe mostrar:
• La palabra con las letras adivinadas y los guiones bajos (_) para las letras no
adivinadas.
• Se debe poder mostrar las palabras a adivinar en un color claro si se activa la opción
de modo oculto, y en la medida que se adivine la letra se debe cambiar el color, esto
con fines de depuración.
• La animación del ahorcado progresando con cada intento fallido.
• La pantalla debe actualizarse en tiempo real según los aciertos y errores del usuario.
• Se debe visualizar un contador del tiempo que a transcurrido desde el inicio del juego
Animación del Ahorcado:
La animación del ahorcado debe progresar de manera secuencial con cada fallo del usuario,
mostrando las partes del cuerpo en el siguiente orden: cabeza, ojos, torso, brazos, y piernas
etc. El diseño de esta animación es libre, pero se valorará especialmente la creatividad y
originalidad en su ejecución durante la evaluación. Se alienta a los desarrolladores a explorar
diferentes estilos y enfoques artísticos para hacer la animación más interesante y visualmente
atractiva.
¡El futuro está en tus manos, programa con pasión y crea algo extraordinario!
Gestión del Juego:
• Iniciar el juego seleccionando una palabra al azar de las almacenadas en la memoria
flash. Consulte el uso de la biblioteca estándar de C stdlib.h para la función rand().
• Verificar las letras ingresadas por el usuario y actualizar la visualización en la pantalla
ST7735.
• El juego debe terminar cuando se adivine la palabra completa o cuando se complete
la animación del ahorcado. Al finalizar la partida, se debe reproducir un sonido de
victoria o de derrota según el resultado. Además, cada vez que se acierte una letra,
se debe reproducir un sonido alegre, y un sonido triste si la letra no está en la
palabra.
Equipo:
Mostrar los nombres de los integrantes del equipo cuando el usuario seleccione la opción 3
del menú, tanto en la terminal serial como en la pantalla LCD. Se debe acompañar de un
logo del equipo y un sonido que sea épico y representativo.
Si considera que esta opción se puede mejorar para hacerla más interactiva, puede
implementar las acciones adicionales que considere adecuadas.
Implementación de Funciones:
Desarrolle la aplicación construyendo funciones que faciliten la revisión del código y su
implementación, debe agregar comentarios en cada línea de código.
• Función para inicializar la pantalla ST7735 y limpiar la pantalla.
• Función para mostrar el menú inicial en la terminal serial.
• Función para recibir y procesar entradas desde la hiperterminal.
• Funciones para manejar la lógica del juego, incluyendo la selección de palabras,
verificación de letras, y actualización de la pantalla.
• Funciones para manejar la animación del ahorcado
