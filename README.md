# electronic
Взяла пример кода для подключения датчика погоды BME280 к микроконтроллеру esp8266 с сайта https://randomnerdtutorials.com/esp8266-bme280-arduino-ide/
Код не компилировался, выдавая ошибку компиляции для платы Generic asp8266, загуглила. https://coderoad.ru/38494441/%D0%9E%D1%88%D0%B8%D0%B1%D0%BA%D0%B0-%D0%BA%D0%BE%D0%BC%D0%BF%D0%B8%D0%BB%D1%8F%D1%86%D0%B8%D1%8F-%D0%B4%D0%BB%D1%8F-%D0%BF%D0%BB%D0%B0%D1%82%D1%8B-generic-esp8266-Arduino-UNO тут было сказано, что возможно нет ядра esp8266 в Arduino IDE. Удалила и заново загрузила плату в менеджере плат.
Ошибка осталась, в начтройках Arduino IDE поставила подробную информацию об ошибках. Оказалость, что одна из необходимых библиотек пыталась загрузить и не находила библиотеку adafruit_i2cdevice.h. Загуглила эту ошибку, оказалось, что новейшая версия используемой мной библиотеки с багом, загрузила одну из старых версий библиотеки Adafruit_BME280.
Компиляция прошла успешно.
Загрузила программу на плату, но в монитор порта выводится ошибка соединения с датчиком погоды. На данный момент разбираюсь с чем это может быть связано.
