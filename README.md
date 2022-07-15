<!-- PROJECT LOGO -->
<div align="center">
  <h3 align="center">MoneyTransfers</h3>

  <p align="center">
    Чтение файла, хранение и поиск информации о пользователях (Расчетный счет плательщика, получателя, перечисляемая сумма в рублях).
  </p>
</div>

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Содержание</summary>
  <ol>
    <li>
      <a href="#О-проекте">О проекте</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## О проекте
Разработан для практики написания:
* Чтения файлов;
* Классов;
	* Конструкторов;
	* Перегрузки операторов;

Проект является консольном приложение на языке C++. Программа читает файл с данными пользователя, выводит в консоль и предлагает найти информацию по «расчетному счету плательщика».
<br />

## Демонстрация
1. Вместе с программой должен лежать файл “ ReadData.txt”
Данные в формате:
«Расчетный счет плательщика» «Расчетный счет получателя» «Перечисляемая сумма в рублях»
<div align="center">

![alt text](https://github.com/SkorEgor/MoneyTransfers/blob/master/ExampleReadData.jpg)
</div>

 2. После запуска программы, в консоли появятся прочтенные данные
<div align="center">

![alt text](https://github.com/SkorEgor/MoneyTransfers/blob/master/ExampleStartProgramm.jpg)
</div>

3. При вводе расчетного счета покажется полная информация:
<div align="center">

![alt text](https://github.com/SkorEgor/MoneyTransfers/blob/master/ExampleEndProgramm.jpg)
</div>

 4. При неверном счете, сообщение об ошибке


<!--
*** 
<div align="center">
  <img src="https://github.com/SkorEgor/MoneyTransfers/blob/master/ExampleReadData.jpg" width="100" />
</div>
*** 
-->
## Начиная
Необходимо поместить файл [«ITOG_2.0.exe»](https://github.com/SkorEgor/MoneyTransfers/blob/master/Debug/ITOG_2.0.exe) и [«ReadData.txt»](https://github.com/SkorEgor/MoneyTransfers/blob/master/Debug/ReadData.txt) вместе. Причем в txt записать данные пользователей. Дальше, запустит .exe

## Алгоритм
<div align="center">

![alt text](https://github.com/SkorEgor/MoneyTransfers/blob/master/Algorithm.jpg)
</div>

## Структура  проекта
Проект разделен на 2 файла 

•	.h – Содержит определение класса ORDER, его полей и методов<br />
•	.cpp – Содержит определение методов класса ORDER и main функцию.


## Ключевые моменты
1.	Для работы со сложной структурой данных, создан класс ORDER <br />
C Публичными методами и конструкторами.<br />
С приватными полями:
	* Расчетный счет плательщика;
	* Расчетный счет получателя;
	* Перечисляемая сумма в рублях.

2.	Методы. Их переопределяем. К примеру, оператор «=». 
Прототип в .h:
```C
ORDER& operator= (const ORDER&);
```
Тело в .cpp:
```C
ORDER& ORDER::operator= (const ORDER& argument)									
{
	payer_current_account = argument.payer_current_account;
	beneficiary_current_account = argument.beneficiary_current_account;
	summ = argument.summ;
	return *this;
}
```