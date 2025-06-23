# DC 예제 1
## DC 모터 가변저항으로 제어하기

![DC](./images/DC_01.png).

```c
void setup()
{
  	pinMode(9,OUTPUT);      // 9핀을 출력으로 설정
}
void loop()
{
  Serial.begin(9600);      // 시리얼 통신 시작(속도는 9600bps로 설정)
  int inputValue = analogRead(A0);    // A0 핀에서 아날로그 입력값(0~1023) 읽기
  Serial.println(inputValue);         // 읽은 값을 시리얼 모니터에 출력
  int convertedValue = map(inputValue, 0, 1023, 0, 255);  // 0~1023 범위를 0~255범위로 변환
  
  analogWrite(9, convertedValue);  // 변환된 값을 9번핀에 아날로그 출력
  delay(100);          // 0.1초간 딜레이
}

```
