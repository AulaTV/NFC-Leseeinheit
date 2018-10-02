# NFC-Leseeinheit
NFC Einheit für die Authentifizierung von Benutzern

## Übersicht
Die NFC Leseeinheit vereint einige Funktionen auf einer 54 x 54 mm großen, doppelseitigen Platine:
- Anschluss eines PN532 NFC Moduls über I2C
- Kommunikation mit der zentralen Steuereinheit über RS232
- Möglichkeit für Reset des Mikrocontrollers in der Steuereinheit über RS232
- Anschluss eines 0,95" 96x64px Farb-OLEDs auf Basis des SSD1331 Controllers über SPI.
- Ausgang für einen Buzzer mit Lautstärkeeinstellung (4 bit Auflösung)
- Ausgang für den Anschluss von WS2812b digitalen LEDs
- integrierter Temperatursensor auf Basis des LM75A, angebunden über I2C
- USB für Firmwareupdates (Arduino Pro Mini 3,3 V, 8 MHz kompatibel)

## Programmierung
Die AulaTV NFC Einheit ist vollständig kompatibel mit einem Arduino Pro Mini 3,3 V, 8 MHz. Der bereits integrierte FT232RL USB <=> UART Wandler macht den beim Pro Mini benötigten FTDI-Adapter unnötig. 
Da jedoch ein fabrikneuer Chip zum Einsatz kommt, kann die Programmierung nicht sofort über USB erfolgen. Hierzu ist ein Bootloader nötig. Dieser startet nach dem Anlegen der Versorgungsspannung und erkennt, wenn die Arduino IDE ein neues Programm über USB hochladen möchte.

### Brennen des Bootloaders
Um den Bootloader zu brennen, benötigt man einen ISP Programmieradapter.

Der Bootloader kann entweder direkt aus der Arduino IDE heraus gebrannt werden, oder es kann die .hex-Datei mit z.B. Atmel Studio auf den ATmega328P gebrannt werden.

Das Hexfile für den Arduino Pro Mini 3,3 V, 8 MHz befindet sich unter C:\Program Files (x86)\Arduino\hardware\arduino\avr\bootloaders\atmega\ATmegaBOOT_168_atmega328_pro_8MHz.hex.

Es können auch lternative Bootloader wie z.B. Optiboot verwendet werden. Hier wird jedoch der Standard-Bootloader zum Einsatz kommen.

### Firmware
to be updated ...
