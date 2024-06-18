Карта опкодов
по x-первый полубайт, y-второй полубайт

|  |  0 |   1|  2|  3|  4|   5|     6|  7|   8|    9|   A|  B|    C|   D|     E|  F|
|--|----|----|---|---|---|----|------|---|----|-----|----|---|-----|----|------|---|
| 0|ADD |ADC |AND|XOR|INC|PUSH|PUSHA |   |xxx |NOP  |MOV |MOV|xxx  |xxx |LOOPNE|   |
| 1|ADD |ADC |AND|XOR|   |    |POPA  |   |xxx |     |MOV |   |     |    |LOOPE |   |
| 2|ADD |ADC |AND|XOR|   |    |      |JS |    |     |MOV |   |RET  |xxx |LOOP  |   |
| 3|ADD |ADC |AND|XOR|   |    |MOVSXD|JNB|xxx |     |MOV |   |RET  |    |JCXZ  |   |
| 4|ADD |ADC |AND|XOR|   |    |FS    |JZ |TEST|     |MOVS|   |LES  |AAM |IN    |HLT|
| 5|ADD |ADC |AND|XOR|   |    |GS    |JNZ|TEST|     |MOVS|   |LDS  |AAD |IN    |   |
| 6|PUSH|PUSH|ES |SS |   |    |Prefix|JBE|XCHG|     |CMPS|   |xxx  |    |OUT   |xxx|
| 7|POP |POP |DAA|AAA|   |    |Prefix|JA |XCHG|     |CMPS|   |xxx  |XLAT|OUT   |xxx|
| 8|OR  |SBB |SUB|CMP|DEC|POP |PUSH  |JS |MOV |CBW  |TEST|MOV|ENTER|    |CALL  |CLC|
| 9|OR  |SBB |SUB|CMP|   |    |IMUL  |JNS|MOV |CWD  |TEST|   |LEAVE|    |JMP   |STC|
| A|OR  |SBB |SUB|CMP|   |    |PUSH  |JP |MOV |CALL |STOS|   |RETF |    |JMP   |CLI|
| B|OR  |SBB |SUB|CMP|   |    |IMUL  |JNP|MOV |     |STOS|   |RETF |    |JMP   |   |
| C|OR  |SBB |SUB|CMP|   |    |INS   |JL |MOV |PUSHF|LODS|   |INT 3|    |IN    |CLD|
| D|OR  |SBB |SUB|CMP|   |    |INS   |JNL|LEA |POPF |LODS|   |     |    |IN    |STD|
| E|PUSH|PUSH|CS |DS |   |    |OUTS  |JNG|MOV |SAHF |SCAS|   |INTO |    |OUT   |xxx|
| F|xxx |POP |DAS|AAS|   |    |OUTS  |JG |xxx |     |SCAS|   |IRET |    |OUT   |xxx|

|Opcode|xx000xx|xx001xx|xx010xx|xx011xx|xx100xx|xx101xx|xx110xx|xx111xx  |
|------|-------|-------|-------|-------|-------|-------|-------|---------|
|80    |ADD    |       |ADC    |       |AND    |       |XOR    |CMP      |
|81    |ADD    |       |ADC    |       |AND    |       |XOR    |CMP      |
|83    |ADD    |       |ADC    |       |AND    |       |XOR    |CMP      |
|C0    |       |       |       |       |       |       |       |         |
|D0    |       |       |       |       |       |       |       |         |
|F6    |       |       |       |       |       |IMUL   |DIV    |IDIV     |
|F7    |       |       |       |       |       |IMUL   |DIV    |IDIV     |
|FE    |INC    |DEC    |       |       |       |       |       |         |
|FF    |INC    |DEC    |CALL   |CALL   |       |       |       |         |
|OF BA |       |       |       |       |BT     |BTS    |BTR    |BTC      |
|OF AE |       |       |       |       |       |       |       |CLFLUSH  |
|0F C7 |       |       |       |       |       |       |       |CMPXCHG8B|
|      |       |       |       |       |       |       |       |         |
|      |       |       |       |       |       |       |       |         |
|      |       |       |       |       |       |       |       |         |
|      |       |       |       |       |       |       |       |         |


Байт 0F
|  |  0 |  1|  2|    3|      4|  5|   6|   7|  8|  9|    A|      B|    C|  D|   E|  F |
|--|----|---|---|-----|-------|---|----|----|---|---|-----|-------|-----|---|----|----|
| 0|    |   |   |WRMSR|CMOVO  |   |    |    |   |   |PUSH |CMPXCHG|     |   |    |    |
| 1|xxx |   |   |     |CMOVNO |   |    |    |   |   |POP  |CMPXCHG|     |   |    |    |
| 2|    |   |   |     |CMOVB  |   |    |    |JC |   |CPUID|LSS    |     |   |    |    |
| 3|    |   |   |     |CMOVNB |   |    |    |JNB|   |BT   |BTR    |     |   |    |    |
| 4|    |   |   |     |CMOVZ  |   |    |    |JZ |   |     |LFS    |     |   |    |    |
| 5|    |   |   |     |CMOVNZ |   |    |    |JNZ|   |     |LGS    |     |   |    |    |
| 6|CLTS|   |   |     |CMOVBE |   |    |    |JBE|   |     |MOVZX  |     |   |    |    |
| 7|    |   |   |     |CMOVNBE|   |    |    |JA |   |     |MOVZX  |xxx  |   |    |    |
| 8|INVD|   |   |     |CMOVS  |   |    |    |JS |   |PUSH |       |BSWAP|   |CALL|    |
| 9|    |   |   |     |CMOVNS |   |    |    |JNS|   |POP  |xxx    |     |   |    |    |
| A|    |   |   |     |CMOVP  |   |    |    |JP |   |     |xxx    |     |   |    |    |
| B| UD2|   |   |     |CMOVNP |   |    |    |JNP|   |BTS  |BTC    |     |   |    |    |
| C|    |   |   |   |CMOVL  |   |    |    |JL |   |SHRD |BSF    |     |   |    |    |
| D|    |   |   |   |CMOVNGE|   |    |    |JNL|   |SHRD |BSR    |     |   |    |    |
| E|    |   |   |   |CMOVLE |   |MOVD|MOVD|JNG|   |xxx  |MOVSX  |     |   |    |    |
| F|    |xxx|   |   |CMOVNLE|   |    |    |JG |   |IMUL |MOVSX  |     |   |    |CALL|
