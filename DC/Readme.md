# DC 예제 1
## DC 모터 가변저항으로 제어하기

![DC](./images/DC_01.png).

```c
void setup()
{
  	pinMode(9,OUTPUT);
}
void loop()
{
  Serial.begin(9600);
  int inputValue = analogRead(A0);
  Serial.println(inputValue);
  int convertedValue = map(inputValue, 0, 1023, 0, 255);
  
  analogWrite(9, convertedValue);
  delay(100);
}

```
