# GDB

## Compile C code
gcc -g hello.c
gcc -g hello.c -o hello

## GDB
gdb -q a.out

set disassembly-flavor intel

list                    # shows source code

disassemble main        # disassembles main into intructions and prints them

break main              # sets a breakpoint on the beginning of main

run                     # runs programme but stops at breakpoints

info registers          # displays rcurrent register information
i r 
i r eip

x                       # Examine memory: x/FMT ADDRESS. ADDRESS is an expression for the memory address to examine.
FMT is a repeat count followed by a format letter and a size letter.
Format letters are o(octal), x(hex), d(decimal), u(unsigned decimal),
  t(binary), f(float), a(address), i(instruction), c(char), s(string)
  and z(hex, zero padded on the left).
Size letters are b(byte), h(halfword), w(word), g(giant, 8 bytes).
The specified number of objects of the specified size are printed
according to the format.  If a negative number is specified, memory is
examined backward from the address.

break [LOCATION]        # break, brea, bre, br, b
Set breakpoint at specified location.
break [PROBE_MODIFIER] [LOCATION] [thread THREADNUM] [if CONDITION]
PROBE_MODIFIER shall be present if the command is to be placed in a
probe point.  Accepted values are `-probe' (for a generic, automatically
guessed probe type), `-probe-stap' (for a SystemTap probe) or 
`-probe-dtrace' (for a DTrace probe).

nexti | ni              # Step one instruction, but proceed through subroutine calls.
Usage: nexti [N]
Argument N means step N times (or till program stops for another reason).


set                     # Evaluate expression EXP and assign result to variable VAR.
Usage: set VAR = EXP
This uses assignment syntax appropriate for the current language
(VAR = EXP or VAR := EXP for example).

cont                    # continues the execution






EAX - Main register used in arithmetic calculations. Also known as accumulator, as it holds results 
      of arithmetic operations and function return values.
EBX - The Base Register. Pointer to data in the DS segment.  Used to store the base address of the 
      program.
ECX - The Counter register is often used to hold a value representing the number of times a process 
      is to be repeated. Used for loop and string operations.
EDX - A general purpose registers. Also used for I/O operations. Helps extend EAX to 64-bits.
ESI - Source Index register. Pointer to data in the segment pointed to by the DS register.  Used as 
      an offset address in string and array operations. It holds the address from where to read data.
EDI - Destination Index register. Pointer to data (or destination) in the segment pointed to by the 
      ES register.  Used as an offset address in string and array operations. It holds the implied 
      write address of all string operations.
EBP - Base Pointer. Pointer to data on the stack (in the SS segment).  It points to the bottom of the 
      current stack frame. It is used to reference local variables.
ESP - Stack Pointer (in the SS segment). It points to the top of the current stack frame. It is used 
      to reference local variables.
EIP - Instruction Pointer (holds the address of the next instruction to be executed)
