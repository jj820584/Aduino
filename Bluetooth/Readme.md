# 블루투스 예제 1
## 블루투스로 램프 점등하기

![bluetooth](./images/bluetooth_01.png).
![bluetooth](./images/bluetooth_02.png).


```c

#include <SoftwareSerial.h>
SoftwareSerial BT(2, 3);

void setup() {
  BT.begin(9600);
  pinMode(8, OUTPUT);
}

void loop() {
  if (BT.available()) {
    int value = BT.read();
    if (value == '1') {
      digitalWrite(8, HIGH);
    }
    if (value == '2') {
      digitalWrite(8, LOW);
    }
  }
}


```
