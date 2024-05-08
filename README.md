# Firmware
 Прошивки для плат конструктора Интросат

Flywheel_1.01-1.6.bin - Прошивка платы маховика версий 1.01-1.6;

Flywheel_1.75-2.1.bin - Прошивка платы маховика версий 1.75-2.1;

Flywheel_3.0-3.3.bin - Прошивка платы маховика версий 3.0-3.3;

FlyWheel_4.0-4.2.bin - Прошивка платы маховика версий 4.0-4.2;

Imitator_v1_1.elf - Прошивка платы имитатора солнечной батареи;

Multi.bin - Прошивка платы мультиметра;

Optical_sensor.bin - Прошивка платы оптического датчика;

LiveOV7670 - Прошивка платы камеры. Исходный код прошивки для камеры: https://github.com/indrekluuk/LiveOV7670.

## Прошивка платы имитатора солнечной батареи

После прошивки платы имитатора солнечной батареи необходимо отключить программатор и подключить плату к ПК, используя USB-UART конвертер. Необходимо использовать следующие настройки COM-порта для корректной работы с платой:
* скорость обмена данными (baud rate) **115200 бод**;
* количество бит данных (data bits) **8**;
* контроль чётности (parity) **even**;
* количество стоп-бит (stop bits) **1**.

Также в мониторе порта должен быть выставлен спецификатор конца строки "Нет конца строки". Если настройки монитора порта выставлены верно, то после подачи питания на плату в мониторе порта можно будет увидеть подсказку:

![image](https://github.com/Obu-IntroSat/Firmware/assets/160022370/58c2fdf9-6064-4f4f-b62b-70e3a40138e8)

После включения по умолчанию имитатор обеспечивает на выходе напряжение 5.5 В и силу тока 0.25 А, причём значение тока пропорционально освещённости фотодиода (режим phd_on).

Задать желаемые параметры на выходе имитатора можно, отправив в монитор порта команды:
* **U=x.xx** - значение напряжения в Вольтах в указанном символами **x** формате, например, U=5.65 (но не U=5.6);
* **I=x.xx** - значение силы тока в Амперах в указанном символами **x** формате, например, I=0.15 (но не I=0.1).

Имитатор поддерживает следующие режимы работы, которые задаются соответствующими командами:
* **phd_on** - мощность на выходе зависит от освещённости фотодиода;
* **i2c_on** - мощность на выходе зависит от освещённости датчика освещённости, подключаемого по интерфейсу I2C;
* **sbs_on** - мощность на выходе зависит от освещённости солнечной батареи;
* **UIuart** - мощность на выходе не зависит от освещённости ни одного из датчиков; ток и напряжение будут полностью соответствовать заданным значениям;
* **sunorb** - работа в цикле, упрощённо симулирующем движение по орбите: 15 минут на выходе обеспечиваются заданные напряжение и ток, 15 минут напряжение и ток отсутствуют.

Если команда была успешно принята имитатором солнечной батареи, в мониторе порта можно будет увидеть следующие ответы:
* U=x.xx - Get U;
* I=x.xx - Get I;
* phd_on - photodiode;
* i2c_on - i2c sense;
* sbs_on - solar battery;
* UIuart - only UART manage U and I
		  	      to set voltage press U=xx.x
		  	      to set current press I=x.xx;
* sunorb - sun cycle 15 minutes.

Если в ответ на команду не появилось сообщение в мониторе порта, проверьте, что команда написана верно, а также, что в настройках монитора порта стоит спецификатор "Нет конца строки". Если случайно было отправлена неверная команда, может потребоваться несколько раз отправить новую команду, чтобы она сработала. Также попробуйте отключить и снова подать питание на плату имитатора, после чего ввести верную команду.
