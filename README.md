📌 Arquitectura ARM

📖 Introducción a Arquitectura ARM






🏛 Historia







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






💻 Código de ejemplo





🚀 Aplicaciones



