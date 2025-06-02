# LED 에제 1
## LED 깜빡이기
![led](./images/led_01.png).

## source code

```c
#define LED_1 10

void setup()
{
	pinMode(LED_1, OUTPUT);

}

void loop()
{
	digitalWrite(LED_1, HIGH);
	delay(80);
  	digitalWrite(LED_1, LOW);
	delay(80);
}
```

## a와 b로 LED 켜고 끄기
```c


void setup()
{
	Serial.begin(9600);
	pinMode(10, OUTPUT);

}

void loop()
{
  if(Serial.available() > 0)
  {
  	char sData = Serial.read();
    if(sData == 'a')
    {
    	digitalWrite(10, HIGH);
    }
  	else if(sData == 'b')
    {
    	digitalWrite(10, LOW);
    }
  }
}
```
