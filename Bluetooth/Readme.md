# 블루투스 예제 1
## 블루투스로 램프 점등하기

![bluetooth](./images/bluetooth_01.png).
![bluetooth](./images/bluetooth_02.png).


```c

#include <SoftwareSerial.h>
SoftwareSerial BT(2, 3);    // 2,3번핀을 블루투스 핀으로 사용

void setup() {
  BT.begin(9600);
  pinMode(8, OUTPUT);      // 8번핀을 출력핀으로 led를 점등시킬 예정
}

void loop() {
  if (BT.available()) {
    int value = BT.read();
    if (value == '1') {      // value값이 1이면 8번핀을 high로 하여 점등시킨다.
      digitalWrite(8, HIGH);
    }
    if (value == '2') {       // value값이 2이면 8번핀을 low로 하여 소등시킨다.
      digitalWrite(8, LOW);
    }
  }
}


```
