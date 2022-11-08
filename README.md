# ตรวจวัดอุณหภูมิและความชื้นด้วย sensor DHT11 ผ่าน Arduino

### ภาพปกตัวอย่าง
![image](https://i.ibb.co/d7wGdnZ/free-Delivr-3.png)

### Source Code

#### Set Up
void setup()
{
   Serial.begin(115200);
   Serial.println(F("DHTxx test!"));
   dht.begin();
 }
#### Loop
void loop()
{
   delay(2000);
   float h = dht.readHumidity(); //อ่านค่า ความชื่นสัมพัธท์ในอากาศ
   float t = dht.readTemperature();//อ่านค่า อุณหภูมิ
   if (isnan(h) || isnan(t))
      {
         Serial.println(F("Failed to read from DHT sensor!"));
         return;
      }
      Serial.print(F("Humidity: "));
      Serial.print(h);
      Serial.print(F("% Temperature: "));
      Serial.print(t);
      Serial.println(F(" C "));
}

### ลิ้งวีดีโอ https://www.youtube.com/watch?v=KQl_TQoP4Nk
