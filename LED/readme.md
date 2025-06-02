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


## LED 여러개 동시에 깜빡이기

![](./images/led_02).


##source code
```c
#define LED_1 10
#define LED_2 9
#define LED_3 8


void setup()
{
	pinMode(LED_1, OUTPUT);
	pinMode(LED_2, OUTPUT);
	pinMode(LED_3, OUTPUT);

}

void loop()
{
	digitalWrite(LED_1, HIGH);
	digitalWrite(LED_2, HIGH);
	digitalWrite(LED_3, HIGH);
	delay(100);
  	digitalWrite(LED_1, LOW);
	digitalWrite(LED_2, LOW);
	digitalWrite(LED_3, LOW);
	delay(100);
}

```

