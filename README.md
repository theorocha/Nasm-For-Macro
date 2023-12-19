# Macros em NASM para laço for

O código consiste em três macros principais:

loopFor: A macro principal que implementa o loop. Aceita quatro parâmetros: o contador, a condição de comparação, o corpo do loop e a operação de incremento.

comparacao: Macro que realiza a comparação do contador com um valor específico. No exemplo, o loop é executado enquanto o contador (ebx) for menor que 5.

imprime: Macro que imprime a string "loop " no console usando a syscall sys_write.

adiciona_ao_contador: Macro que incrementa o valor do contador (ebx) em 1.

Observações
Certifique-se de ajustar as condições de comparação e as ações do loop conforme necessário.
Para compilar, você pode usar o NASM para montar o código e o linker (ld) para criar o executável(Usei Linux/Ubuntu).

```
  nasm -f elf32 -o for.o for.asm
  ld -m elf_i386 -o for for.o
 ./for
```
