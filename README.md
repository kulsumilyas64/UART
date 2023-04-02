## UART Basic Code
### 1st Method-
```
#include"main.h"

uint8_t buf[10];                            // Buffer created to store received 10 char 
uint8_t buf1[] = "Kulsum\r\n";               //data to be transmitted stored in buf

int main(void)
{
while(1)
 {
    HAL_UART_Receive(&huart2, buf, sizeof(buf), 1000);               // Receives the data stored in buf
    HAL_UART_Transmit(&huart2, buf1, sizeof(buf1), 1000);            // Transmit the data stored in buf1
    HAL_Delay(500);
  }
}

```
### 2nd Method-

```
#include"main.h"

uint8_t buf1[]="Kulsum\r\n";                   // Size can also be written in the bracket - buf1[10]

int main(void)
{
while(1)
{
   HAL_UART_Transmit(&huart1, buf1, sizeof(buf1),1000);
   HAL_Delay(500);
  }
}
```


