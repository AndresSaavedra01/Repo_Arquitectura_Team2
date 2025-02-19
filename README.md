📌 Arquitectura ARM

📖 Introducción a Arquitectura ARM

La arquitectura ARM (Advanced RISC Machine) es un tipo de arquitectura de procesador basada en el conjunto de instrucciones RISC (Reduced Instruction Set Computing).
Fue desarrollada originalmente por Acorn Computers en la década de 1980 y actualmente es utilizada en una gran variedad de dispositivos, desde teléfonos móviles y tabletas hasta servidores y supercomputadoras.
En los últimos años, ARM ha ganado terreno en el mercado de computadoras personales y servidores debido a su alto rendimiento y bajo consumo energético. Empresas como Apple con sus chips M1/M2 y AWS con los Graviton están impulsando esta arquitectura más allá de los dispositivos móviles.


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

## 1. Instrucciones de Transferencia de Datos
Estas instrucciones mueven datos entre registros o entre memoria y registros.

- `MOV` – Mueve datos de un lugar a otro.
- `PUSH` – Guarda un valor en la pila.
- `POP` – Recupera un valor de la pila.
- `XCHG` – Intercambia valores entre dos registros o memoria.
- `LEA` – Carga la dirección efectiva de un operando en un registro.
- `LDS`, `LES` – Carga segmento y offset en registros.

## 2. Instrucciones Aritméticas
Realizan operaciones matemáticas básicas.

- `ADD` – Suma dos valores.
- `SUB` – Resta dos valores.
- `MUL` – Multiplicación sin signo.
- `IMUL` – Multiplicación con signo.
- `DIV` – División sin signo.
- `IDIV` – División con signo.
- `INC` – Incrementa en 1 el valor de un operando.
- `DEC` – Decrementa en 1 el valor de un operando.

## 3. Instrucciones Lógicas y de Comparación
Se usan para manipular bits y evaluar condiciones.

- `AND` – Operación lógica AND.
- `OR` – Operación lógica OR.
- `XOR` – Operación lógica XOR.
- `NOT` – Invierte los bits de un operando.
- `CMP` – Compara dos valores restándolos (sin almacenar resultado).
- `TEST` – Realiza una comparación lógica AND sin almacenar resultado.

## 4. Instrucciones de Control de Flujo
Permiten alterar el flujo del programa.

- `JMP` – Salta a una dirección de memoria.
- `JE`, `JZ` – Salta si son iguales (Zero Flag = 1).
- `JNE`, `JNZ` – Salta si no son iguales (Zero Flag = 0).
- `JG`, `JNLE` – Salta si es mayor (para valores con signo).
- `JL`, `JNGE` – Salta si es menor (para valores con signo).
- `JGE`, `JNL` – Salta si es mayor o igual.
- `JLE`, `JNG` – Salta si es menor o igual.
- `CALL` – Llama a una subrutina.
- `RET` – Retorna de una subrutina.
- `LOOP` – Repite un bloque de código basado en el registro `CX`.

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

La arquitectura ARM es altamente utilizada en diversos sectores gracias a su bajo consumo energético y alto rendimiento. 
Recordando que el ecosistema ARM surgió en los últimos años con los productos y las soluciones optimizados para los servidores,
los cuales se diseñaron para la nube, sistemas informáticos escalables y el edge computing
A continuación se explicará algunas de sus principales aplicaciones

1. Dispositivos móviles (Smartphones y Tablets)

 Se utililiza en casi todos los teléfonos inteligentes, así como en otros dispositivos móviles pequeños y en las computadoras portátiles
 esto debido a que los chips x86 está diseñados para optimizar el rendimiento, mientras que con los procesadores basados en ARM se busca 
 lograr el equilibrio entre cosos y la reducción del tamaño, la disminución del consumo de energía y las temperaturas, velocidad y mayor 
 duración de la batería.

Empresas como Apple (A-series y M-series), Qualcomm (Snapdragon), Samsung (Exynos) y MediaTek diseñan sus chips basados en ARM
Otra ventaja de implementar esta arquitectura en los móviles es la integración de CPU, GPU y módulos de conectividad en un solo chip 
(SoC-System on Chip)

🔹 Ejemplo real:

Los procesadores Apple M1 y M2, basados en ARM, han demostrado superar a los chips x86 en eficiencia y rendimiento, permitiendo laptops
más ligeras y con mayor autonomía.

2. Computación en la nube y servidores

Los servidores ARM ofrecen varias ventajas sobre las arquitecturas de servidores tradicionales basadas en x86 en cuanto a consumo de energía, rendimiento por vario y eficiencia general del sistema. La explicación se encuentra a continuación:
    
    🔹Eficiencia energética: En la informática moderna, la conservación de energía es crucial, y los servidores basados en ARM son ideales para estos entornos. (Los procesadores ARM  consumen menos energía que los x86).

    🔹 Integración de IoT y computación de borde: El bajo formato de ARM y su bajo consumo  de energía lo hacen adecuado no solo para centros de datos, sino que también para dispositivos de IoT y computación de borde.

    🔹 Escalabilidad: Son altamente escalables y permiten realizar una amplia gama de cargas de trabajo, desde servidores web livianos hasta HPC (aplicaciones informáticas de alto rendimiento).

    🔹 Costos operativos más bajos.

    🔹 Licencias libres y abiertas: Permiten a las empresas a desarrollar bajo una base.

    🔹 Mayor densidad de servidores en racks.

🔹 Ejemplo real:

    🔹AWS Graviton: Procesadores ARM desarrollados por Amazon Web Services para optimizar cargas de trabajo en la nube.

    🔹Ampere Altra: Utilizado por Microsoft Azure y Google Cloud para ofrecer servicios en la nube con menor consumo.

3. Internet de las cosas (IoT) y Edge computing

El aumento de la capacidad de procesamiento y la disminución del consumo de energía y los costos de mantenimiento de los dispositivos inteligentes, interconectados e interactivos en el borde de internet están creando enormes oportunidades para equipar las ciudades, fábricas, granjas etc. 

En otras palabras, los dispositivos IoT necesitan procesadores eficiente y compactos que puedan funcionar con baterías de larga duración y también los procesadores ARM están optimizados para Edge computing, lo que permite procesar datos más cerca de donde se generan sin depender de la nube (IoT genera grandes cantidades de datos y Edge Computing los procesa más cerca del origen).

🔹Ejemplos:

    🔹ESP32 y Raspberry Pi → Utilizados en proyectos de IoT y domótica con núcleos ARM por su bajo consumo y alta integración.
    
    🔹 Ciudades inteligentes: Semáforos que procesan datos de tráfico localmente.
    
    🔹 Redes 5G: Infraestructura con chips ARM para mejorar la eficiencia energética.
    
    🔹Vehículos autónomos.

4. Supercomputacion 

Una supercomputadora es aquel tipo de ordenador que presenta capacidades de cálculo my por encima de la media. De hecho, la velocidad de estas máquinas se mide en petaflops o mil millones de operaciones por segundo. Aunque tradicionalmente dominado por x86, ARM ha ganado terreno en el mundo de los supercomputadores debido a su eficiencia energética y escalabilidad.

Entre sus ventajas de utilizar esta arquitectura está:
   🔹Eficiencia energética: Reduce el consumo y la disipación de calor en comparación al x86

   🔹Alto rendimiento escalable: Puede integrarse en arquitecturas masivamente paralelas con miles de nucleos

   🔹Menos costos operativos: Reduce gastos en refrigeración

🔹 Ejemplo real:

   🔹 Fugaku (Japón) → Supercomputador basado en procesadores ARM A64FX de Fujitsu, reconocido como uno de los más potentes del mundo.

   🔹 Cray y HPE están integrando procesadores ARM en sus supercomputadores para investigación científica.

5. Telecomunicaciones y Redes

Los procesadores ARM son esenciales en equipos de telecomunicaciones debido a su capacidad para manejar múltiples procesos de datos con bajo consumo de energía.

Algunas ventajas de ARM en telecomunicaciones:
   🔹Menor consumo de energía en redes 5G.

   🔹Infraestructura más compacta: Facilita el despliegue de redes móviles y satelitales con hardware optimizado

   🔹Mayor procesamiento en el Edge.
   
🔹 Aplicaciones en redes:

   Routers y módems: Procesamiento rápido de datos con baja latencia.

   Infraestructura 5G: ARM es clave en el despliegue de redes 5G, ya que maneja señales y conexiones en estaciones base.

   Sistemas satelitales: La baja disipación térmica de ARM es ideal para satélites de comunicación.

🔹 Ejemplo real:

Qualcomm y Broadcom diseñan chips ARM para infraestructura de telecomunicaciones y conectividad 5G.
>>>>>>> develop
