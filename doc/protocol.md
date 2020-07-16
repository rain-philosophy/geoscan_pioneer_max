# Описание протокола

## 1. События автопилота

### Команды, передоваемые Пионеру:
* evnt-0 - выполнить предвзлетную подготовку (Ev.MCE_PREFLIGHT)
* evnt-1 - выполнить взлет (Ev.MCE_TAKEOFF)
* evnt-2 - совершить посадку (Ev.MCE_LANDING)

### Подтверждения получения команд от Пионера:
* prfl - команда выполнения предвзлетной подготовки получена
* tkff - команда выполнения взлета получена
* land - команда выполнения посадки получена

### Подтверждения выполнения команд от Пионера:
* egst - двигатели заведены (Ev.ENGINES_STARTED)
* clnd - совершена посадка (Ev.COPTER_LANDED)
* ptrd - точка достигнута (Ev.POINT_REACHED, Ev.TAKEOFF_COMPLETE для АП версии 1.5 и выше)

## 2. Взаимодействие с сенсорами Пионера

### Команды, передоваемые Пионеру (Пионер на все команды возвращает числа):
* time  - запрос времени с момента включения коптера ( time() )
* dltm  - запрос разницы времени с начала включения коптера и времени глобальной системы навигации ( deltaTime() )
* lntm  - запрос времени запуска для системы навигации ( launchTime() )
* bnum запрос бортового номера

### Команды, передоваемые Пионеру (Пионер возвращает сообщение):
* 