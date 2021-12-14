# Proyecto 

Nayeli Esmeralda Aceves Angulo 215256141
Universidad de Guadalajara ( CUCEI )
Ingeniería en Computación

## ANALIZADOR LEXICO

#### ¿QUE ES UN ANALIZADOR LEXICO?

El analizador léxico. Se encarga de buscar los componentes léxicos o palabras que componen el programa fuente, según unas reglas o patrones. La entrada del analizador léxico podemos definirla como una secuencia de caracteres.

#### CARACTERISTICAS

El analizador léxico tiene que dividir la secuencia de caracteres en palabras con significado propio y después convertirlo a una secuencia de terminales desde el punto de vista del analizador sintáctico, ya que es su entrada. El analizador léxico reconoce las palabras en función de una gramática regular de manera que sus no terminales se convierten en los elementos de entrada de fases posteriores. En Lex, por ejemplo, esta gramática se expresa mediante expresiones regulares.

#### FUNCION
El analizador léxico es la primera fase de un compilador. Su principal función consiste en leer los caracteres de entrada y elaborar como salida una secuencia de componentes léxicos que utiliza el analizador sintáctico para hacer el análisis. Esta interacción, suele aplicarse convirtiendo al analizador léxico en una subrutina o corrutina del analizador sintáctico. Recibida la orden “Dame el siguiente componente léxico” del analizador sintáctico, el analizador léxico lee los caracteres de entrada hasta que pueda identificar el siguiente componente léxico. Otras funciones que realizan se listan a continuación:

* Eliminar los comentarios del programa.
* Eliminar espacios en blanco, tabuladores, retorno de carro, etc, y en general, todo aquello que carezca de significado según la sintaxis del lenguaje.
* Reconocer los identificadores de usuario, números, palabras reservadas del lenguaje y tratarlos correctamente con respecto a la tabla de símbolos (solo en los casos que debe de tratar con la tabla de símbolos).
* Llevar la cuenta del número de línea por la que va leyendo, por si se produce algún error, dar información sobre donde se ha producido.
* Avisar de errores léxicos. Por ejemplo, si @ no pertenece al lenguaje, avisar de un error.
* Puede hacer funciones de preprocesador.

#### NECESIDAD DE UN ANALIZADOR LEXICO

Entre las razones por las cuales es necesario separar el analizador léxico del sintáctico se pueden mencionar:

* Un diseño sencillo es quizás la consideración más importante. Separar el análisis léxico del análisis sintáctico a menudo permite simplificar una u otra de dichas fases. El analizador léxico nos permite simplificar el analizador sintáctico.
* Se mejora la eficiencia del compilador. Un analizador léxico independiente permite construir un procesador especializado y potencialmente más eficiente para esa función. Gran parte del tiempo se consume en leer el programa fuente y dividirlo en componentes léxicos. Con técnicas especializadas de manejo de buffers para la lectura de caracteres de entrada y procesamiento de componentes léxicos se puede mejorar significativamente el rendimiento de un compilador.
* Se mejora la portabilidad del compilador. Las peculiaridades del alfabeto de entrada y otras anomalías propias de los dispositivos pueden limitarse al analizador léxico. La representación de símbolos especiales o no estándares pueden ser aisladas en el analizador léxico.
* Para que se centre en el reconocimiento de componentes básicos complejos.

## ANALIZADOR SINTACTICO

#### ¿QUE ES UN ANALIZADOR SINTACTICO?
Un analizador sintáctico o parser (viene del inglés: parse - analizar una cadena o texto en componentes sintácticos lógicos) es un programa que normalmente es parte de un compilador. El compilador se asegura de que el código se traduce correctamente a un lenguaje ejecutable. La tarea del analizador es, en este caso, la descomposición y transformación de las entradas en un formato utilizable para su posterior procesamiento. Se analiza una cadena de instrucciones en un lenguaje de programación y luego se descompone en sus componentes individuales.

#### ¿COMO FUNCIONA?
Para analizar un texto, los analizadores suelen utilizar un analizador léxico separado (llamado lexer), que descompone los datos de entrada en fichas (símbolos de entrada como palabras). Los Lexers son por lo general máquinas de finitas, que siguen la gramática regular y por lo tanto aseguran un desglose adecuado. Los tokens obtenidos de esta manera sirven como caracteres de entrada para el analizador sintáctico.

El analizador actual maneja la gramática de los datos de entrada, realiza un análisis sintáctico de éstos y como regla general crea un árbol de sintaxis (árbol de análisis). Esto se puede utilizar para el procesamiento posterior de los datos, por ejemplo, la generación de código por un compilador o ejecutado por un intérprete (traductor). Por lo tanto, el analizador es el software que comprueba, procesa y reenvía las instrucciones del código fuente.

#### TIPOS DE ANALIZADORES

Hay básicamente dos métodos de análisis diferentes, análisis de arriba hacia abajo (top-down) y análisis de abajo hacia arriba (bottom-up). Éstos difieren generalmente en el orden en el que se crean los elementos del árbol sintáctico.

* De arriba a abajo: En el método top-down, el analizador trabaja en un método orientado a objetivos, lo que significa que busca a partir del símbolo de inicio de la sintaxis y busca una derivación sintáctica adecuada. Por lo tanto, el árbol de análisis se desarrolla de arriba hacia abajo en la dirección de un desglose cada vez más detallado.
* De abajo hacia arriba: El analizador ascendente comienza con el símbolo de la cadena de entrada e intenta establecer relaciones sintácticas cada vez mayores. Esto se hace hasta que el símbolo de inicio de la gramática se ha alcanzado.

#### APLICACIONES 

Un analizador sintáctico se utiliza a menudo para convertir texto en una nueva estructura, por ejemplo, un árbol sintáctico, que expresa la disposición jerárquica de los elementos. En las siguientes aplicaciones el uso de un analizador es usualmente esencial:

* La lectura de un lenguaje de programación es realizada por un analizador. Proporciona una estructura de datos al compilador, con la que se puede generar el código máquina o bytecode.
* El código HTML es al principio sólo una cadena de caracteres para un ordenador que debe ser analizada por el analizador contenido en el navegador web. Proporciona una descripción de la página web como una estructura de datos que puede ser proyectada por un motor de diseño en la pantalla.
* Los analizadores especiales de XML son responsables del análisis de los documentos XML y preparan la información contenida en ellos para su uso posterior.
* Los analizadores de URI descomponen esquemas complejos tales como URLs en su estructura jerárquica.
* Los motores de búsqueda como Google extraen (analizan) texto relevante para ellos de las páginas web descargadas con rastreadores. Se procesan y los datos analizados se pueden utilizar para la navegación.

