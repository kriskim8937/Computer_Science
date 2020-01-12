## Assemblers
- fundamental functions tha any assembler must perform.
  - translatin mnemonic operation codes to their machine language equivalents, 
  - assigning machine addresses to symbolic labels used by the programmer
- 2.1 ifundamental operations performed by a typical assembleer
  - algorithms and data structures
- 2.2 typical extensions to the basic assem bler structrue that might be dictated by hard ware considerationss
- 2.3 discussion of some of the most commonly encountered machine-independent assmebler language features their implementations
- 2.4 important alternative design schemes for assembler
> difference between assembler, compiler, interpreter Assembler is a program that converts assembly level language (low level language) into machine level language. Compiler compiles entire C source code into machine code. Whereas, interpreters converts source code into intermediate code and then this intermediate code is executed line by line.
 - 2.1 Basic Assembler functions
  - START, END, BYTE, WORD, RESB, RESW
  - 2.1.1 A simple SIC Assembeler 
    - source code를 object code로 변환하기 위해서는 다음의 과정이 필요하다.
      - 1. Convert mnemonic operation codes to their machine language code 
      - 2. Convert symbolic operands to their equivalent machine addresses 
      - 3. Build the machine instructions in the proper format
      - 4. Convert the data constatnts specified in the source program in to their internal machine representations.
      - 5. Write the object program and the assembly listing
