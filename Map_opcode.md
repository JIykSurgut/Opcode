Карта опкодов
по x-первый полубайт, y-второй полубайт

|  | 0 |  1|  2|  3|  4|  5|   6|  7|  8|  9|   A|  B|    C|  D|     E|  F|
|--|---|---|---|---|---|---|----|---|---|---|----|---|-----|---|------|---|
| 0|ADD|ADC|AND|   |INC|   |    |   |ADC|   |MOV |MOV|     |   |LOOPNE|   |
| 1|ADD|ADC|AND|   |   |   |    |   |ADC|   |MOV |   |     |   |LOOPE |   |
| 2|ADD|ADC|AND|   |   |   |    |JS |   |   |MOV |   |     |   |LOOP  |   |
| 3|ADD|ADC|AND|   |   |   |    |JNB|ADC|   |MOV |   |     |   |JCXZ  |   |
| 4|ADD|ADC|AND|   |   |   |    |JZ |   |   |MOVS|   |LES  |AAM|IN    |   |
| 5|ADD|ADC|AND|   |   |   |    |JNZ|   |   |MOVS|   |LDS  |AAD|IN    |   |
| 6|   |   |   |   |   |   |    |JBE|   |   |CMPS|   |xxx  |   |      |xxx|
| 7|   |   |DAA|AAA|   |   |    |JA |   |   |CMPS|   |xxx  |   |      |xxx|
| 8|   |   |   |CMP|DEC|   |    |JS |MOV|CBW|    |MOV|     |   |      |CLC|
| 9|   |   |   |CMP|   |   |IMUL|JNS|MOV|CWD|    |   |LEAVE|   |JMP   |   |
| A|   |   |   |CMP|   |   |    |JP |MOV|   |    |   |     |   |JMP   |   |
| B|   |   |   |CMP|   |   |IMUL|JNP|MOV|   |    |   |     |   |JMP   |   |
| C|   |   |   |CMP|   |   |INS |JL |MOV|   |LODS|   |     |   |IN    |CLD|
| D|   |   |   |CMP|   |   |INS |JNL|LEA|   |LODS|   |     |   |IN    |   |
| E|   |   |   |   |   |   |    |JNG|MOV|   |    |   |     |   |      |xxx|
| F|   |   |DAS|AAS|   |   |    |JG |   |   |    |   |     |   |      |xxx|

Байт 0F
|  | 0 |  1|  2|  3|  4|  5|   6|   7|  8|  9|    A|  B|    C|  D|   E|  F |
|--|---|---|---|---|---|---|----|----|---|---|-----|---|-----|---|----|----|
| 0|   |   |   |   |   |   |    |    |   |   |     |   |     |   |    |    |
| 1|   |   |   |   |   |   |    |    |   |   |     |   |     |   |    |    |
| 2|   |   |   |   |   |   |    |    |JC |   |CPUID|LSS|     |   |    |    |
| 3|   |   |   |   |   |   |    |    |JNB|   |BT   |BTR|     |   |    |    |
| 4|   |   |   |   |   |   |    |    |JZ |   |     |LFS|     |   |    |    |
| 5|   |   |   |   |   |   |    |    |JNZ|   |     |LGS|     |   |    |    |
| 6|   |   |   |   |   |   |    |    |JBE|   |     |   |     |   |    |    |
| 7|   |   |   |   |   |   |    |    |JA |   |     |   |     |   |    |    |
| 8|   |   |   |   |   |   |    |    |JS |   |     |   |BSWAP|   |CALL|    |
| 9|   |   |   |   |   |   |    |    |JNS|   |     |   |     |   |    |    |
| A|   |   |   |   |   |   |    |    |JP |   |     |BT |     |   |    |    |
| B|   |   |   |   |   |   |    |    |JNP|   |BTS  |BTC|     |   |    |    |
| C|   |   |   |   |   |   |    |    |JL |   |     |BSF|     |   |    |    |
| D|   |   |   |   |   |   |    |    |JNL|   |     |BSR|     |   |    |    |
| E|   |   |   |   |   |   |MOVD|MOVD|JNG|   |     |   |     |   |    |    |
| F|   |   |   |   |   |   |    |    |JG |   |IMUL |   |     |   |    |CALL|
