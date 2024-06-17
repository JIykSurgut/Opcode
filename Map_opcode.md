Карта опкодов
по x-первый полубайт, y-второй полубайт

|  |  0 |   1|  2|  3|  4|   5|     6|  7|   8|    9|   A|  B|    C|   D|     E|  F|
|--|----|----|---|---|---|----|------|---|----|-----|----|---|-----|----|------|---|
| 0|ADD |ADC |AND|   |INC|PUSH|PUSHA |   |xxx |NOP  |MOV |MOV|xxx  |xxx |LOOPNE|   |
| 1|ADD |ADC |AND|   |   |    |POPA  |   |xxx |     |MOV |   |     |    |LOOPE |   |
| 2|ADD |ADC |AND|   |   |    |      |JS |    |     |MOV |   |RET  |xxx |LOOP  |   |
| 3|ADD |ADC |AND|   |   |    |MOVSXD|JNB|xxx |     |MOV |   |RET  |    |JCXZ  |   |
| 4|ADD |ADC |AND|   |   |    |      |JZ |TEST|     |MOVS|   |LES  |AAM |IN    |   |
| 5|ADD |ADC |AND|   |   |    |      |JNZ|TEST|     |MOVS|   |LDS  |AAD |IN    |   |
| 6|PUSH|PUSH|   |   |   |    |      |JBE|XCHG|     |CMPS|   |xxx  |    |OUT   |xxx|
| 7|POP |POP |DAA|AAA|   |    |      |JA |XCHG|     |CMPS|   |xxx  |XLAT|OUT   |xxx|
| 8|OR  |SBB |SUB|CMP|DEC|POP |PUSH  |JS |MOV |CBW  |TEST|MOV|     |    |      |CLC|
| 9|OR  |SBB |SUB|CMP|   |    |IMUL  |JNS|MOV |CWD  |TEST|   |LEAVE|    |JMP   |STC|
| A|OR  |SBB |SUB|CMP|   |    |PUSH  |JP |MOV |     |STOS|   |RETF |    |JMP   |   |
| B|OR  |SBB |SUB|CMP|   |    |IMUL  |JNP|MOV |     |STOS|   |RETF |    |JMP   |   |
| C|OR  |SBB |SUB|CMP|   |    |INS   |JL |MOV |PUSHF|LODS|   |     |    |IN    |CLD|
| D|OR  |SBB |SUB|CMP|   |    |INS   |JNL|LEA |POPF |LODS|   |     |    |IN    |STD|
| E|PUSH|PUSH|   |   |   |    |OUTS  |JNG|MOV |SAHF |SCAS|   |     |    |OUT   |xxx|
| F|    |POP |DAS|AAS|   |    |OUTS  |JG |xxx |     |SCAS|   |     |    |OUT   |xxx|

|Opcode|xx000xx|xx001xx|xx010xx|xx011xx|xx100xx|xx101xx|xx110xx|xx111xx|
|------|-------|-------|-------|-------|-------|-------|-------|-------|
|80    |ADD    |       |ADC    |       |       |       |       |       |
|81    |ADD    |       |ADC    |       |       |       |       |       |
|83    |ADD    |       |ADC    |       |       |       |       |       |
|C0    |       |       |       |       |       |       |       |       |
|D0    |       |       |       |       |       |       |       |       |
|      |       |       |       |       |       |       |       |       |
|      |       |       |       |       |       |       |       |       |
|      |       |       |       |       |       |       |       |       |
|      |       |       |       |       |       |       |       |       |
|      |       |       |       |       |       |       |       |       |
|      |       |       |       |       |       |       |       |       |
|      |       |       |       |       |       |       |       |       |


Байт 0F
|  | 0 |  1|  2|  3|  4|  5|   6|   7|  8|  9|    A|    B|    C|  D|   E|  F |
|--|---|---|---|---|---|---|----|----|---|---|-----|-----|-----|---|----|----|
| 0|   |   |   |   |   |   |    |    |   |   |PUSH |     |     |   |    |    |
| 1|   |   |   |   |   |   |    |    |   |   |POP  |     |     |   |    |    |
| 2|   |   |   |   |   |   |    |    |JC |   |CPUID|LSS  |     |   |    |    |
| 3|   |   |   |   |   |   |    |    |JNB|   |BT   |BTR  |     |   |    |    |
| 4|   |   |   |   |   |   |    |    |JZ |   |     |LFS  |     |   |    |    |
| 5|   |   |   |   |   |   |    |    |JNZ|   |     |LGS  |     |   |    |    |
| 6|   |   |   |   |   |   |    |    |JBE|   |     |MOVZX|     |   |    |    |
| 7|   |   |   |   |   |   |    |    |JA |   |     |MOVZX|xxx  |   |    |    |
| 8|   |   |   |   |   |   |    |    |JS |   |PUSH |     |BSWAP|   |CALL|    |
| 9|   |   |   |   |   |   |    |    |JNS|   |POP  |xxx  |     |   |    |    |
| A|   |   |   |   |   |   |    |    |JP |   |     |BT   |     |   |    |    |
| B|UD2|   |   |   |   |   |    |    |JNP|   |BTS  |BTC  |     |   |    |    |
| C|   |   |   |   |   |   |    |    |JL |   |SHRD |BSF  |     |   |    |    |
| D|   |   |   |   |   |   |    |    |JNL|   |SHRD |BSR  |     |   |    |    |
| E|   |   |   |   |   |   |MOVD|MOVD|JNG|   |     |MOVSX|     |   |    |    |
| F|   |xxx|   |   |   |   |    |    |JG |   |IMUL |MOVSX|     |   |    |CALL|
