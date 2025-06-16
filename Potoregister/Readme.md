# 포토레지스터 예제1
## 포토레지스터 빛 센서 사용하기


![LCD](./images/Photoregister_01.png).

```c

void setup()
{
  pinMode(9, OUTPUT);
}

void loop()
{
  int val1 = analogRead(0);
  int val2 = map(val1, 0, 1023, 0, 255);

  analogWrite(9, val2);
  delay(20);
}

```



