📌 Arquitectura ARM

📖 Introducción a Arquitectura ARM






🏛 Historia







🛠 Ensamblador

🔹 Instrucciones






🔹 Registros






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



