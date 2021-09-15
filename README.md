# Calendar
Класс статических методов конвертации времени

Использует функционал Qt 5

---

Публичные статические методы

1. TDateTimeToQDateTime переводит дату и время из формата TDateTime в формат QDateTime
TDateTime содержит количество суток, прошедших от 00:00 30.12.1899 г.
Подаваемое на вход время должно быть больше 01.01.1970 г.
Синтаксис:
static QDateTime TDateTimeToQDateTime(double Value)


2. QDateTimeToTDateTime переводит дату и время из формата QDateTime в формат TDateTime
TDateTime содержит количество суток, прошедших от 00:00 30.12.1899 г.
Подаваемое на вход время должно быть больше 01.01.1970 г.
Синтаксис:
static double QDateTimeToTDateTime(QDateTime Value)


3. QStringToQDateTime переводит строку типа Qstring в формат QDateTime, разбирая 
вышеупомянутую строку по заданной пользователем маске
Подаваемое на вход время должно быть больше 01.01.1970 г.
Примеры масок:
  - "dd.MM.yyyy  HH:mm:ss.zzz";
  - "dd.MM.yyyy  HH:mm:ss";
  - "dd.MM.yyyy".
Синтаксис:
static QDateTime QStringToQDateTime(QString Value, QString Mask)


4. QDateTimeToQString переводит дату и время из формата QDateTime в строку типа 
QString, создавая вышеупомянутую строку по заданной пользователем маске
Подаваемое на вход время должно быть больше 01.01.1970 г.
Примеры масок:
  - "dd.MM.yyyy  HH:mm:ss.zzz";
  - "dd.MM.yyyy  HH:mm:ss";
  - "dd.MM.yyyy".
Синтаксис:
static QString QDateTimeToQString(QDateTime Value, QString Mask)


5. QStringToTDateTime переводит строку типа Qstring в формат TDateTime, разбирая 
вышеупомянутую строку по заданной пользователем маске
TDateTime содержит количество суток, прошедших от 00:00 30.12.1899 г.
Подаваемое на вход время должно быть больше 01.01.1970 г.
Примеры масок:
  - "dd.MM.yyyy  HH:mm:ss.zzz";
  - "dd.MM.yyyy  HH:mm:ss";
  - "dd.MM.yyyy".
Синтаксис:
static double QStringToTDateTime(QString Value, QString Mask)


6. TDateTimeToQString переводит дату и время из формата TDateTime в строку типа 
QString, создавая вышеупомянутую строку по заданной пользователем маске
TDateTime содержит количество суток, прошедших от 00:00 30.12.1899 г.
Подаваемое на вход время должно быть больше 01.01.1970 г.
Примеры масок:
  - "dd.MM.yyyy  HH:mm:ss.zzz";
  - "dd.MM.yyyy  HH:mm:ss";
  - "dd.MM.yyyy".
Синтаксис:
static QString TDateTimeToQString(double Value, QString Mask)


7. DecodeQDateTime перегруженный метод разбирает дату и время из формата 
QDateTime на составные части
Подаваемое на вход время должно быть больше 01.01.1970 г.
На вход подается:
  - Value дата и время в формате QDateTime.
На выходе можно получить:
  - DayInWeek день недели (1 - понедельник; 2 - вторник; 3 - среда; 
    4 - четверг; 5 - пятница; 6 - суббота; 7 - воскресенье);
  - DayInYear номер дня в году (начинается с 1);
  - WeekInYear номер недели в году (начинается с 1);
  - Year год;
  - Month месяц;
  - Day день;
  - Hour часы;
  - Min минуты;
  - Sec секунды;
  - MilliSec милисекунды.
Синтаксис:
static void DecodeQDateTime(QDateTime Value, int *DayInWeek, int *DayInYear, 
                            int *WeekInYear, int *Year, int *Month, int *Day, 
                            int *Hour, int *Min, int *Sec, int *MilliSec)


8. DecodeQDateTime перегруженный метод разбирает дату и время из формата 
QDateTime на составные части
Подаваемое на вход время должно быть больше 01.01.1970 г.
На вход подается:
  - Value дата и время в формате QDateTime.
На выходе можно получить:
  - DayInWeek день недели (1 - понедельник; 2 - вторник; 3 - среда; 
    4 - четверг; 5 - пятница; 6 - суббота; 7 - воскресенье);
  - DayInYear номер дня в году (начинается с 1);
  - WeekInYear номер недели в году (начинается с 1).
Синтаксис:
static void DecodeQDateTime(QDateTime Value, int *DayInWeek, 
                            int *DayInYear, int *WeekInYear)


9. DecodeQDateTime перегруженный метод разбирает дату и время из формата 
QDateTime на составные части
Подаваемое на вход время должно быть больше 01.01.1970 г.
На вход подается:
  - Value дата и время в формате QDateTime.
На выходе можно получить:
  - Year год;
  - Month месяц;
  - Day день;
  - Hour часы;
  - Min минуты;
  - Sec секунды;
  - MilliSec милисекунды.
Синтаксис:
static void DecodeQDateTime(QDateTime Value, int *Year, int *Month, int *Day, 
                            int *Hour, int *Min, int *Sec, int *MilliSec)


10. EncodeQDateTime собирает дату и время в формате QDateTime из составных частей
Подаваемое на вход время должно быть больше 01.01.1970 г.
На вход подаются:
  - Year год;
  - Month месяц;
  - Day день;
  - Hour часы;
  - Min минуты;
  - Sec секунды;
  - MilliSec милисекунды.
Синтаксис:
static QDateTime EncodeQDateTime(int Year, int Month, int Day, int Hour, 
                                 int Min, int Sec, int MilliSec)


11. CrosDiapasons решает задачу пересечения двух временных отрезков First 
и Second в формате TDateTime
На вход подаются:
  - FirstStart начало первого временного отрезка;
  - FirstStop окончание первого временного отрезка;
  - SecondStart начало второго временного отрезка;
  - SecondStop окончание второго временного отрезка.
На выходе можно получить:
  - ResultStart начало интервала пересечения двух временных 
    отрезков (если пересечение есть);
  - ResultStop окончание интервала пересечения двух временных 
    отрезков (если пересечение есть).
Возвращает True, если временные отрезки пересекаются.
Возвращает False, если временные отрезки не пересекаются (ResultStart и 
ResultStop равны нулю).
Считается, что есть пересечение, если оно состоит более чем из одной точки.
Синтаксис:
static bool CrosDiapasons(double FirstStart, double FirstStop, double SecondStart, 
                          double SecondStop, double *ResultStart, double *ResultStop)
