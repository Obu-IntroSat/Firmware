
# Прошивки для плат конструктора ИнтроСат 

## В каких случая необходимо прошивать плату?
Вышла новая версия прошивки, в которой были исправлены баги или добавлен новый функционал.

## Как прошивать плату?
1) Найти на плате название и версию. Они нанесены на каждую плату, и обычно состоят из двух или трёх заглавных латинских букв.
Например, название платы маховика - **FM**, платы солнечного датчика - **SO**. Версия платы написана сразу после названия, и состоит из двух цифр, разделённых точкой, например **1.2**. На плате это может выглядеть вот так:
<p align="center">
 <img src="https://github.com/user-attachments/assets/bea48a3f-7711-4940-910a-7d38e39ffc0e" width=300px align="center"\>
</p>

2) Найти в этом репозитории файл прошивки, соответствующий Вашей плате. Будьте внимательны с версиями - для плат маховика важно использовать прошивку соответствующей версии.

3) Следовать инструкции по прошивке, доступной по [ссылке](https://docs.google.com/document/d/15KqFrMlc6Jzxut_zMf_pXNx5r5JTjqfKEvCHWx99rEc/edit?tab=t.0#heading=h.26q1awmk9xol). 

## Актуальные прошивки для последних версий

[CM_2.x.elf](https://raw.githubusercontent.com/Obu-IntroSat/Firmware/main/CM_2.x.elf) - Прошивка для платы камеры версии 2.0 и выше

[FM_4.x.elf](https://raw.githubusercontent.com/Obu-IntroSat/Firmware/main/FM_4.x.elf) - Прошивка платы маховика версии 4.0 и выше

[eSE_1.x.elf](https://raw.githubusercontent.com/Obu-IntroSat/Firmware/main/eSE_1.x.elf) - Прошивка платы имитатора солнечной батареи

[MM_1.0-2.x.bin](https://raw.githubusercontent.com/Obu-IntroSat/Firmware/main/MM_1.0-2.x.bin) - Прошивка платы мультиметра версии 1.0 и выше

[SO_1.0-2.x.bin](https://raw.githubusercontent.com/Obu-IntroSat/Firmware/main/SO_1.0-2.x.bin) - Прошивка платы оптического датчика версии 1.0 и выше

## Прошивки для предыдущих версий плат
Файлы можно найти в папке [Archive](./Archive/)

[FM_1.01-1.6.bin](https://raw.githubusercontent.com/Obu-IntroSat/Firmware/main/FM_1.01-1.6.bin) - Прошивка платы маховика версий 1.01-1.6

[FM_1.75-2.1.bin](https://raw.githubusercontent.com/Obu-IntroSat/Firmware/main/FM_1.75-2.1.bin) - Прошивка платы маховика версий 1.75-2.1

[FM_3.0-3.3.bin](https://raw.githubusercontent.com/Obu-IntroSat/Firmware/main/FM_3.0-3.3.bin) - Прошивка платы маховика версий 3.0-3.3

[CM_1.X](./Archive/LiveOV7670) - Прошивка платы камеры версий 1.x 

> [!CAUTION]
> В камерах версии 1.x использовался микроконтроллер LGT8F328P, эти платы необходимо прошивать через Arduino IDE, используя в качестве программатора оригинальную Arduino Uno или ISP-программатор.
> Исходный код прошивки для камеры: https://github.com/indrekluuk/LiveOV7670.

 ## Полезные ссылки
Наш [канал в Telegram](https://t.me/introsat_news) поможет не пропустить обновления.

Если у вас возникли вопросы или сложности при работе с IntroSat, ответы можно найти в нашем [F.A.Q.](https://docs.google.com/document/d/15KqFrMlc6Jzxut_zMf_pXNx5r5JTjqfKEvCHWx99rEc/edit#heading=h.demjj79bt080)

Остались вопросы? Напишите нашему [боту в Telegram](https://t.me/introsatBot)! Укажите в обращении модуль конструктора, при работе с которым возникли проблемы, и версии платы (написаны на самих платах), и мы обязательно Вам поможем.   

---
<p align="center">
 <img width=70% alt="IntroSat Logo" src="https://github.com/user-attachments/assets/966f7746-2764-4479-848c-38e5ab825ff4"/>
<!--  <img width=30% alt="Education of the Future" src="https://github.com/user-attachments/assets/1c33d94c-cfc8-4a9b-a658-43fcf6d78393"/> -->
</p>
