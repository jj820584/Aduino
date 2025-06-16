# LCD 예제 1
## LCD 16X2 출력하기

![LCD](./images/lcd_01.png).

```c

#include <LiquidCrystal.h>        // Liquidcrystal.h 라는 패키지를 다운받아서 사용한다.

LiquidCrystal lcd(12, 11, 5, 4, 3, 2);  // 12,11, 5, 4, 3, 2번 핀을 사용할 예정이다. 

void setup()    // 이 코드는 전원이 켜질때 또는 리셋 버튼을 눌렀을때 딱 한번 작동한다.
{
  lcd.begin(16,2);  // lcd 초기화 함수로 (열, 행)을 의미한다. 즉 가로 문자 수 16칸, 세로 문자수 2칸을 배치하도록 셋팅한다는 의미이다.
  lcd.print("Hello, world!!!");  // lcd에 헬로 월드라는 문자를 출력한다.

}

void loop()
{}

```

# LCD 예제 2
## LCD 16X2 문자열 출력하기


![LCD](./images/lcd_01.png).

```c

#include <LiquidCrystal.h>

LiquidCrystal lcd(12, 11, 5, 4, 3, 2);

void setup() {
  lcd.begin(16, 2);
  lcd.print("Hello, world!!!");
}

void loop() {
  lcd.print("Cusor ON-Blink");
  lcd.cursor();
  lcd.blink();
  delay(2000);
  lcd.clear();

  lcd.print("Cusor OFF");
  lcd.noBlink();
  lcd.cursor();
  delay(1000);
  lcd.clear();

  lcd.print("Count Up");
  delay(1000);
  lcd.clear();

  for (int k = 0; k <= 10; k++) {
    lcd.home();
    lcd.print("No : ");
    lcd.print(k);
    delay(200);
  }
  lcd.clear();

  lcd.print("Hello!");
  for (int k = 0; k < 3; k++) {
    lcd.noDisplay();
    delay(1000);
    lcd.display();
    delay(1000);
  }
  lcd.clear();

  lcd.setCursor(6, 0);
  lcd.print("Hello!");
  for (int k = 0; k < 3; k++) {
    lcd.scrollDisplayRight();
    delay(500);
  }
  lcd.clear();

  lcd.setCursor(6, 0);
  lcd.print("Hello!");
  for (int k = 0; k < 3; k++) {
    lcd.scrollDisplayLeft();
    delay(500);
  }
  lcd.clear();
}

```
