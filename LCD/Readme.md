# LCD 예제 1
## LCD 16X2 출력하기

![LCD](./images/lcd_01.png).

```c

#include <LiquidCrystal.h>

LiquidCrystal lcd(12, 11, 5, 4, 3, 2);

void setup()
{
  lcd.begin(16,2);
  lcd.print("Hello, world!!!");

}

void loop()
{}

```
