# hse25_hw1

# Основная часть 
### Анализ QC чтений 
Полный отчет html находится в папке data


Главная особенность по сравнению с секвенированием ДНК или РНК заключается в необычном распределении GC. Такое явление возникает из-за бисульфитной конверсии - химической обработке ДНК NaHSO₃, которая позволяет различить метилированные и неметилированные цитозины. Этот процесс лежит в основе бисульфитного секвенирования, при котором неметилированные цитозины преобразуются в урацил.

![Unknown-8](https://github.com/user-attachments/assets/d450940f-d980-4fbf-8e9c-c439af4cd84b)

По принципу комплементарности, цитозина должно быть столько же, сколько и гуанина, а % тимина = % аденина. Однако в данном случае тимина (урацила) больше чем должно быть. Это означает, что часть тиминов до секвенирования были цитозинами, следовательно большая часть цитозина была неметелирована.
![Unknown-9](https://github.com/user-attachments/assets/39adaaf6-c347-4f58-86aa-c330a2436d79)

### Работа с bam файлами выравниваниями BS-seq ридов на 11-ю хромосому мыши
<img width="511" alt="Снимок экрана 2025-02-16 в 21 29 01" src="https://github.com/user-attachments/assets/010ceea2-04e4-481a-bea8-552e8c6e9393" />

 ### Дедупликация файлов выравниваний
<img width="684" alt="Снимок экрана 2025-02-16 в 21 35 48" src="https://github.com/user-attachments/assets/2ba7d7c1-8669-4c2a-95a0-88c47efb0d71" />

 ### Описание M-bias plot

В отчетах находятся графики, которые показывают уровень метилирования на хромосому. 
Наибольшая доля метилирования наблюдается в образце Epiblast (77-78%), затем в образце 8_cell (42-45%), а наименьшая доля метилирования у образца icm (22-24%), такое распределение соответствует литературным данным, что доказывает, что работа проделана корректно. 



##### Epiblast – стадия эпибласта, примерно 6.5 дней после оплодотворения яйцеклетки
<img width="1181" alt="Снимок экрана 2025-02-16 в 21 43 38" src="https://github.com/user-attachments/assets/c7fd547b-5901-4ef7-9897-857b04570229" />
<img width="1181" alt="Снимок экрана 2025-02-16 в 21 43 50" src="https://github.com/user-attachments/assets/1e4bf01a-7f44-4525-969b-e6f438401aea" />

##### ICM – внутренняя клеточная масса бластоциста, примерно 3.5 дня после оплодотворения яйцеклетки


### Гистограммы распределения метилирования цитозинов по хромосоме

Полученные гистограммы для ICM и Epiblast в точности совпадают с референсом из статьи. Для 8 cell тенденция так же схожа, единственное, в референсе не такой резкий спад в начале и нет увеличения в конце.
<img width="813" alt="reference" src="https://github.com/user-attachments/assets/ea8d48ba-4d3b-4fe6-95aa-cc941c6849ec" />



![8_cell](https://github.com/user-attachments/assets/43588855-91f0-47c8-9acc-f73158e4ca10)
![icm](https://github.com/user-attachments/assets/72345b68-ee4a-41ba-bf81-f5fae5865cda)
![epiblast](https://github.com/user-attachments/assets/5c838f2f-cc53-4a01-a3bd-b2dd67e98fcb)

## Визуализация уровней метилирования и покрытия для каждого образца 

### Метилирование 
Из данного графика следует, что уровень метилирования не различается между группами.
![image_cov](https://github.com/user-attachments/assets/108ccf97-64ba-444f-a323-237dd648c426)

### Покрытие 

Высокие пики означают области с высокой глубиной секвенирования, что говорит о надежности данных в этих участках. Наиболее высокие пики находятся практически на всем участке Epiblast, короче всех пики у icm.
Визуально профили покрытия схожи между всеми тремя образцами на разных стадиях развития эмбриона мыши. Следовательно, данные секвенирования были получены равномерно.
![image_met](https://github.com/user-attachments/assets/66e16b71-b811-4f6f-b8d7-8ff2657f06c7)





