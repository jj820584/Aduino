# LED 에제 1
## LED 깜빡이기
![led](./images/LED_00.png).

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
