📌 Arquitectura ARM

📖 Introducción a Arquitectura ARM






🏛 Historia







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




💻 Código de ejemplo





🚀 Aplicaciones



