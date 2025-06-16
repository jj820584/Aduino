# LCD 예제 1
## LCD 16X2 출력하기



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
