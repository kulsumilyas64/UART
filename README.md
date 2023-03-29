## UART Basic Code

```
#include"main.h"

uint8_t buf1[10];                            // Buffer created to store received 10 char 
uint8_t buf[] = {0,1,2,3,4,5,6,7,8,9};     //data to be transmitted stored in buf1

int main(void)
{
while(1)
 {
    HAL_UART_Receive(&huart1, buf, 10, 1000);               // Receives the data stored in buf
    HAL_UART_Transmit(&huart1, buf1, 10, 1000);            // Transmit the data stored in buf1
  }
}

```
