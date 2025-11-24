# Airsoft Timing System
Dispositivos de Crono para IPSC Action Air

# Airsoft Timing System (ESP32 Edition)

Proyecto DIY basado en el **M4P1+ Airsoft Timing System de Special Pie**, adaptado con un **ESP32 CH340C WiFi + Bluetooth** y componentes adicionales para crear un sistema de cronometraje y control de airsoft.  
El sistema consta de **dos dispositivos**:
1. **Crono (Chrono Unit)** → da la salida al tirador y hace de **servidor** para el "End plate".  
2. **End Plate Unit** → cliente conectado al crono registrar el tiempo final del ejercicio.

---

## 🚀 Características principales
- Cronógrafo con servidor integrado (WiFi).
- Pantalla OLED de 0,96" (SSD1306, I2C, 128x64).
- Zumbador pasivo para alertas acústicas.
- Alimentación mediante batería LiPo con módulo de carga TP4056.
- Conectividad WiFi y Bluetooth para expansión futura.
- Diseño modular y portátil.

---

## 🛠️ Hardware utilizado
- **ESP32 CH340C WiFi + Bluetooth**
- **Pantalla OLED 0,96" I2C SSD1306 (128x64)**
- **Zumbador pasivo 42R 12085 (12mm x 8,5mm)**
- **Módulo de carga TP4056**
- **Batería LiPo**

---

## 📐 Esquema básico de conexión
| Componente         | Conexión ESP32 |
|--------------------|----------------|
| OLED SSD1306 (I2C) | SDA → GPIO21   |
|                    | SCL → GPIO22   |
| Zumbador pasivo    | GPIO25         |
| TP4056             | Batería LiPo   |
| Batería LiPo       | VIN / GND      |

*(Los pines pueden ajustarse según tu firmware.)*

---

## ⚙️ Instalación

Abre el proyecto en Arduino IDE o PlatformIO.

Instala las librerías necesarias:
  Adafruit SSD1306
  Adafruit GFX
  WiFi.h (incluida en ESP32)
  BluetoothSerial.h (incluida en ESP32)

Compila y sube el firmware a cada ESP32
