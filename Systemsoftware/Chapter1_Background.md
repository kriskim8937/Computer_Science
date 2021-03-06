## Chapter 1 - Background
- 1.1 brief introduction to system software and overview of this book
  - assemblers, loaders, linkers, macro processors, compilers, operation systems.
- 1.2 relationships between system software and machine architecture
  - System software은 machine dependent하다. System software를 다루면, machine을 다룰 수 밖에 없고 무엇이 fundamental한지 판단하기 힘들다
  - 이러한 문제를 막기위해 SIC를 사용한다. SIC는 가상의 컴퓨터로, 복잡하고 특별한 부분들을 제외하고 가장 기본이되고 많이 쓰이는 기능들을 구현하고 있다. 
  - chapter section:
    - 1. 어떠한 소프트웨어에서나 발견되는, 가장 기본적인 Feature들
    - 2. machine architecture와 관련있는 feature들
    - 3. 이러한 타입의 소프트웨어의 구현에서 쉽게 발견되고, 상대적으로 machine-independent한 다른 feature들 
    - 4. 소프트웨어의 특정 부분을 구현하는데 필요한 design options들, 예를들면 single pass, multi pass process
    - 5. 실제 machine의 구현, 실제 machine과 관련있는 unusal한 feature들
- 1.3 Simplified Instructional Computer 
  - 1.3.1 SIC Machine Architecture
    - Memory : 
      - 8 bit bytes로 memory가 이루어져있다. 3개의 연속적인(consecutive)byte들이 word를 구성한다.
      - SIC의 모든 메모리들은 byte addresse이다. 
      - 2^15 byte의 메모리가 존재한다.
    - Registers :
      - 특별한 용도로 사용되는 5개의 register 가 존재한다. 각 레지스터는 24bit이다. 
      - Mnemonic : 레지스터등을 상징하는 약어 A register
      - Table :
        - Accumulator : A
        - Index register : X
        - Linkage register : L 
        - Program counter : PC
        - Statsus word : SW
      - machine bit 랑 software 32bit 64bit 랑은 무슨 관계일까?
        > A computer with a 32-bit processor cannot have a 64-bit version of an operating system installed. It can only have a 32-bit version of an operating system installed.
        > A computer with a 64-bit processor can have a 64-bit or 32-bit version of an operating system installed. However, with a 32-bit operating system, the 64-bit processor would not run at its full capability.
        > On a computer with a 64-bit processor, you cannot run a 16-bit legacy program. Many 32-bit programs works with a 64-bit processor and operating system, but some older 32-bit programs may not function properly, or at all, due to limited or no compatibility.
        > Another big difference between 32-bit processors and 64-bit processors is the maximum amount of memory (RAM) that is supported. 32-bit computers support a maximum of 4 GB (232 bytes) of memory, whereas 64-bit CPUs can address a theoretical maximum of 18 EB (264 bytes). However, the practical limit of 64-bit CPUs (as of 2018) is 8 TB of addressable RAM.
    - Data formats
      - integer은 24bit binary number을 가지고 있다. 음수는 2의 보수 형태
      - floating point hardware은 존재하지 않는다.
      - 컴퓨터 타입마다 서로 다른 integer size를 가질 수 있다. virtual machine을 포함한 computer hardware들은 거의 항상 processor register나 memory address를 표현하는 방법으로 integer을 사용한다.
    - Instruction Format
      - 24bit format을 가진다. 8 opcode 1 indexed addressing mode flag bit , 15 address
    - Addressing Modes
      - Direct , INdexed
    - Instruction Set
      - LDA, LDX, STA, STX, ADD, SUB, MUL, DIV, COMP
    - Input and Output 
        
