
# Serial Transfer of Single Byte / Character using 8051 (Keil)

## AIM
To write and execute an Embedded C Program for Serial Transfer of Single Byte / Character using 8051 in Keil.

## APPARATUS REQUIRED
- Personal Computer  
- Keil µVision Software  

## PROGRAM

### (i) Serial Port Transfer a Single Character

```
#include<reg51.h>
void main(void)
{
	TMOD=0X20;
	TH1=0XFA;
	SCON=0X50;
	TR1=1;
	SBUF='A';
	while (T1==0);
		T1=0;
	while(1);
}

```
### (ii) Serial Port to Transfer a Message

```
#include <reg51.h>
void main(void)
{
    unsigned char msg[] = "Microcontroller";
    unsigned char i;
    TMOD = 0x20;
    TH1  = 0xFA;
    SCON = 0x50;
    TR1  = 1;
    for(i = 0; msg[i] != '\0'; i++)
    {
        SBUF = msg[i];
        while(TI == 0);
        TI = 0;
    }

    while(1);
}
```

### OUTPUT:
<img width="600" height="500" alt="image" src="https://github.com/user-attachments/assets/eab831c0-1487-4777-88de-2de7781117e1" />
<img width="600" height="500" alt="Screenshot 2026-03-17 082534" src="https://github.com/user-attachments/assets/6f2c02f2-5f5b-47eb-9c4c-c9aeddb57242" />

### RESULT:
Thus the Serial transfer of Single Byte / Character using 8051 KEIL was done and shown the output.
