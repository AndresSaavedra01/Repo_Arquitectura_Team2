📌 Arquitectura ARM

📖 Introducción a Arquitectura ARM






🏛 Historia

### Origenes

En 1978 se fundó Acorn Computers por Chris Curry y Hermann Hauser. Acorn obtuvo los derechos para producir el BBC Micro,
 un proyecto del gobierno británico para llevar computadoras a las aulas. Como parte de esto, Steve Furber y Sophie Wilson
diseñaron el primer procesador Arm, el ARM1, que manejaba eficientemente tareas como procesamiento de texto y gráficos.
Este avance sentó las bases para los procesadores modernos de Arm, utilizados en diversos dispositivos. Sin embargo, 
Acorn enfrentó dificultades financieras a mediados de los 80, lo que llevó a su adquisición por el Grupo Olivetti.
Hauser asumió brevemente el rol de VP de Investigación en Olivetti antes de irse, mientras que Furber y Wilson continuaron desarrollando
el procesador ARM2.

### ARM en dipositivos moviles
 
En 1993, Arm firmó un acuerdo con el proveedor de silicio, Texas Instruments, con la compañía aconsejando a Nokia que utilizara los diseños
de Arm para sus próximos teléfonos móviles GSM. El teléfono móvil GSM Nokia 6110 con tecnología Arm fue un éxito masivo, y el procesador Arm7
 se convirtió en el diseño móvil insignia de Arm. Hoy en día, más del 99 por ciento de los teléfonos inteligentes del mundo se basan en la
tecnología Arm.

### Diversificación de su linea de productos

Arm como empresa llevó a una mayor diversificación de su línea de productos a través de los procesadores CPU Cortex-A, Cortex-R y Cortex-M
que lanzó al mercado en la década de 2000. 
* Cortex-A continuó el impulso hacia el alto rendimiento y la eficiencia en los mercados de dispositivos móviles
* Cortex-R se centró en los requisitos altamente especializados en tiempo real en una era de creciente conectividad
* Cortex-M proporcionó núcleos de muy bajo consumo y bajo costo para microcontroladores que comenzaban a proliferar en el creciente Internet de las cosas (IoT)

### El auge de los teléfonos inteligentes

La introducción de los primeros teléfonos inteligentes del mundo en 2007 creó aún más demanda de un mayor rendimiento que mantuviera una larga duración de la batería Arm respondió a este desafío con su procesador multinúcleo Cortex-A9 CPU, antes de presentar el innovador "big. LITTLE" en 2011, que combinaba un núcleo potente para el alto rendimiento con un núcleo de menor potencia cuando el alto rendimiento no era necesario. Este enfoque sigue siendo utilizado por Arm en la actualidad.

### Impulsando la conectividad

La proliferación de IoT y dispositivos conectados a principios y mediados de la década de 2010 proporcionó nuevas oportunidades tecnológicas para Arm. Sus tecnologías iban más allá de los dispositivos móviles e impulsaban una gama cada vez mayor de dispositivos en un panorama tecnológico cada vez más amplio. En 2022, el 65 por ciento de los dispositivos IoT integrados del mundo se construyeron con sistemas en chips (SoC) basados en Arm.

La adquisición de SoftBank permitió a Arm invertir fuertemente en la compañía y continuar su impulso para la diversificación tecnológica en los mercados emergentes, incluidos los automóviles y la infraestructura. Por otro lado el lanzamiento de la línea de productos Neoverse por parte de Arm en octubre de 2018 para soluciones de computación de alto rendimiento (HPC) y computación en la nube condujo a importantes victorias a finales de la década de 2010. Entre ellas, la adopción de instancias basadas en Arm en todos los principales hiperescaladores y el superordenador más rápido del mundo con SoC basados en Arm en 2019

### Actualidad

Debido a sus exitosos orígenes y al trabajo de miles de empleados talentosos durante los últimos 30 años, Arm es el líder mundial en tecnología con licencia para empresas de semiconductores. Arm es una empresa verdaderamente global, con 43 oficinas en 21 países y más de 6.000 empleados en todo el mundo, incluidos casi 3.000 en el Reino Unido con sede mundial en Cambridge. Gracias a un ecosistema tecnológico líder de más de 1.000 socios
de confianza, la tecnología de Arm se ha enviado en más de 265.000 millones de chips, alimentando todo, desde sensores hasta supercomputadoras.
Arm es la plataforma informática más extendida en todo el mundo en la actualidad, y la tecnología llega a aproximadamente el 70 por ciento de la población mundial.


🛠 Ensamblador

🔹 Instrucciones






🔹 Registros
Los procesadores ARM cuentan con un conjunto de registros que se utilizan para almacenar datos, direcciones y estados del procesador. Estos registros se pueden clasificar en:

1. Registros de propósito general (GPR - General Purpose Registers)
ARM dispone de 16 registros principales en su modo de ejecución estándar:

R0 - R12: Se utilizan para almacenar datos temporales y variables en la ejecución de programas.
R13 (SP - Stack Pointer): Apunta a la cima de la pila, utilizada para gestionar llamadas a funciones y almacenamiento temporal.
R14 (LR - Link Register): Guarda la dirección de retorno al llamar una función.
R15 (PC - Program Counter): Contiene la dirección de la siguiente instrucción a ejecutar.

2. Registros de estado y control

CPSR (Current Program Status Register): Guarda información sobre el estado del procesador, incluyendo los flags de condición (Zero, Carry, Overflow, Negative).
SPSR (Saved Program Status Register): Se usa para almacenar el CPSR cuando se produce un cambio de modo de ejecución.

3. Modos de operación y registros en ARM

ARM soporta varios modos de operación, como User, FIQ (Fast Interrupt), IRQ (Interrupt), Supervisor, Abort, Undefined y System, algunos de los cuales tienen versiones dedicadas de ciertos registros (como R13 y R14).


💻 Código de ejemplo


Hola Mundo en Ensamblador x86 (Linux)
-------------------------------------

section .data

    msg db '¡Hola, mundo!', 0  ; El mensaje a imprimir, terminado en 0 (nulo)

section .text

    global _start

_start:

    ; Escribir en la salida estándar (stdout)

    mov eax, 4        ; syscall número 4 (sys_write)

    mov ebx, 1        ; file descriptor 1 (stdout)

    mov ecx, msg      ; puntero al mensaje

    mov edx, 13       ; longitud del mensaje (¡Hola, mundo! tiene 13 caracteres)

    int 0x80          ; llamar al kernel
    

    ; Salir del programa
    mov eax, 1        ; syscall número 1 (sys_exit)
    xor ebx, ebx      ; código de salida 0
    int 0x80          ; llamar al kernel
----------------------------------------


Hola Mundo en Ensamblador x86 (Windows)
----------------------
.386


.model flat, stdcall


option casemap :none




include windows.inc


include kernel32.inc


include user32.inc


includelib kernel32.lib


includelib user32.lib

.data

    msg db '¡Hola, mundo!', 0


.code

start:

    ; Mostrar el mensaje usando MessageBoxA

    push MB_OK

    push offset caption

    push offset msg

    push 0

    call MessageBoxA


    ; Salir del programa
    push eax
    call ExitProcess

caption db "Mensaje", 0
end start

-------------------
🚀 Aplicaciones



