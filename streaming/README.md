## super easy!

```C
#include <plotly_wifi_streaming.h>

plotly logger(username, api_key, stream_token, filename)

void setup() {

  Serial.begin(9600);


  wifi_connect();

  // initialize stream!
  logger.begin(50); // 50: max number of points in plot

}

int x, y;
void loop() {
  // giddyup!
  logger.plot(millis(), analogRead(A0));
  delay(100);
}
```