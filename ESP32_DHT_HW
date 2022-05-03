#include <WiFi.h>
#include <DHT.h>

#define DHTPIN 23
#define DHTTYPE DHT11 //DHT21 //DHT22

float h=0;
float t_c=0;  
float t_f=0;  

DHT dht(DHTPIN, DHTTYPE);             

void setup() {
  dht.begin();
  Serial.begin(115200);
}

void loop() {
  float h = dht.readHumidity();
  float t_c = dht.readTemperature();
  float t_f = dht.readTemperature(true);

  Serial.printf("Humedad:%f, Temp[c]:%f, Temp[f]:%f\n", h, t_c, t_f); 
  delay(2500);
}
