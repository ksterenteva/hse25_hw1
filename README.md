# hse25_hw1

# Основная часть коллаб
[Ссылка на коллаб](https://colab.research.google.com/drive/1sTUf4Czoi7746JVj4NDJlCudLH7Da4_q?authuser=2#scrollTo=Yh76j0rKXQzD)

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

Графики показывают уровень метилирования на хромосому. 
Наибольшая доля метилирования наблюдается в образце Epiblast (77-78%), затем в образце 8_cell (42-45%), а наименьшая доля метилирования у образца icm (22-24%), такое распределение соответствует литературным данным, что доказывает, что работа проделана корректно. 

##### 8cell – 8-клеточный эмбрион, примерно 2.25 дня после оплодотворения яйцеклетки
![8_cell_Read_1](https://github.com/user-attachments/assets/c3e298d9-758a-44a7-874c-aed0de95206b)
![8_cell_Read_2](https://github.com/user-attachments/assets/eec9deee-3c7c-4eba-a9e6-bea1c52dfd7a)


##### ICM – внутренняя клеточная масса бластоциста, примерно 3.5 дня после оплодотворения яйцеклетки
![icm_Read_1-1](https://github.com/user-attachments/assets/0f5c22bd-1645-42f2-b47f-9f4c71d7ed90)
![icm_Read_2-1](https://github.com/user-attachments/assets/9e8213e7-7bc0-493e-96d7-5b4a5b0d2f1e)



##### Epiblast – стадия эпибласта, примерно 6.5 дней после оплодотворения яйцеклетки
![epiblast_Read_1](https://github.com/user-attachments/assets/ea34b2ce-023d-465a-a3b8-cde0c6005da6)
![epiblast_Read_2](https://github.com/user-attachments/assets/8322dfd2-a893-4c32-b9a9-e6faaa390643)


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

# DMR и DMC 
[Ccылка на коллаб 2](https://colab.research.google.com/drive/1RI9xG9rPYnjw5um_z_OWujJDo37ZfC0Y?authuser=2#scrollTo=p1-D-P25cqHy)
## Дифференциально метилированные цитозины (DMC)

Файлы не загружаются в папку data из-за больших размеров, могу прислать если нужно, вот скрины:
<img width="614" alt="Снимок экрана 2025-02-16 в 23 36 03" src="https://github.com/user-attachments/assets/b87287e5-9453-430e-a356-2da95963273a" /><img width="614" alt="Снимок экрана 2025-02-16 в 23 36 14" src="https://github.com/user-attachments/assets/2523d6b1-caa6-4226-8ae7-fd414ab92ebe" /><img width="614" alt="Снимок экрана 2025-02-16 в 23 36 23" src="https://github.com/user-attachments/assets/31ac07f5-05f1-45c2-b0cb-785181326243" />




На следующих графиках можем увидеть распределение разницы метилирования между двумя группами. График должен отражать паттерны изменения уровня метилирования между двумя состояниями.
8-клеточная стадия (8cell) vs Эпибласт (epiblast)

Можно увидеть, что в стадии 8cell количество метилированных цитозинов гораздо больше, чем в стадии ICM

![Unknown-7](https://github.com/user-attachments/assets/157ccded-ec47-4d07-ad1c-d368bfc01e03)

У эпибласта очень много метилированных цитозинов относительно 8cell исходя из графика

![Unknown-5](https://github.com/user-attachments/assets/3e1a82c8-b0c6-4833-b9d4-cc34ef7d2881)

Самые значительные изменения в метилировании происходят при переходе от ICM к эпибласту, что указывает на важные эпигенетические перестройки в этом периоде.

![Unknown-6](https://github.com/user-attachments/assets/1d88074d-802e-4fc2-87d1-448ace873b7d)

Вывод: Эпибласт в целом характеризуется более высоким уровнем метилирования, что показывали и результаты работы ранее 

## Дифференциально метилированные участки (DMR)

Файлы с результатами находятся в папке data

На стадии 8cell гораздо больше метилированных участков, чем в стадии ICM
![Unknown](https://github.com/user-attachments/assets/8f56a7eb-bfc7-4606-a1b4-743ba2da2df7)

На стадии Epiblast больше всего метилированных участков в сравнении с 8cell, ICM

![Unknown-3](https://github.com/user-attachments/assets/3954583c-0c55-470c-9cb4-06359c4542f0)

![Unknown-10](https://github.com/user-attachments/assets/9a353d83-def4-4e99-a7ff-1ac898a67b42)


# Дополнительная часть 

## Определение в каких генах попадают DMR
[Cсылка на коллаб 3](https://colab.research.google.com/drive/1WkKOUdcxESIV2QzV-4_BlWT6GT9U_irp?authuser=2#scrollTo=oUXvC2gVdKUf)

Все результаты находятся в папке data 

DMR_in_genes_8cell_icm_chr11.bed, DMR_in_genes_8cell_epiblast_chr11.bed, DMR_in_genes_icm_epiblast_chr11.bed - результат программы bedtools, координаты пересечения между генами и метилированными участками 

Final_DMR_in_Genes_8cell_icm_chr11.bed, Final_DMR_in_Genes_8cell_epiblast_chr11.bed, Final_DMR_in_Genes_icm_epiblast_chr11.bed - координаты с названиями генов 

