# 부저 예제 1
## 부저로 피아노 만들기

![Buzer](./images/buzer_01.png).


```c

#define PIEZO_BUZZER 3  //3번 핀으로 피에조 부저 전력을 공급해준다.
#define SW1 12          //12번 ~ 8번 핀을 사용할 예정이다.
#define SW2 11
#define SW3 10
#define SW4 9
#define SW5 8

void setup() {
  pinMode(SW1, INPUT_PULLUP);  // 스위지 1번 ~ 5번을 누르면 풀업, 즉 작동되도록 설정한다.
  pinMode(SW2, INPUT_PULLUP);  // INPUT_PULLUP 모드를 사용하기 때문에 0일때 작동하고 1일때 중지된다.
  pinMode(SW3, INPUT_PULLUP);
  pinMode(SW4, INPUT_PULLUP);
  pinMode(SW5, INPUT_PULLUP);
}

void loop() {
  if (digitalRead(SW1) == 0) tone(PIEZO_BUZZER, 262, 1000);        // digitalRead는 버튼상태를 읽는 함수이다.sw1이 0=low 즉, 버튼이 눌러졌다면 작동한다. 
  else if (digitalRead(SW2) == 0) tone(PIEZO_BUZZER, 294, 1000);    // tone함수는 피에조 부저의 소리를 출력하는 함수이다. tone(핀번호, 주파수, 지속시간)이다.
  else if (digitalRead(SW3) == 0) tone(PIEZO_BUZZER, 330, 1000);    // 즉, 해당되는 스위치를 누르면 피에조 부저가 작동하고 버튼마다 할달된 주파수를 1초간 출력된다.
  else if (digitalRead(SW4) == 0) tone(PIEZO_BUZZER, 349, 1000);    // 262 도, 294 레, 330 미, 349 파, 392 솔, 440 라, 494 시
  else if (digitalRead(SW5) == 0) tone(PIEZO_BUZZER, 392, 1000);
  else noTone(PIEZO_BUZZER);                                        // 지정된 핀에 재생된 소리를 멈추는 함수이다. 즉, 스위치 1번~5번을 누르지 않으면 소리가 정지된다는 의미이다.
}

```
