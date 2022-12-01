# АНАЛИЗ ДАННЫХ И ИСКУССТВЕННЫЙ ИНТЕЛЛЕКТ [in GameDev]
Отчет по лабораторной работе #4 выполнил(а):
- Ахидов Роман Игоревич
- РИ210934
Отметка о выполнении заданий (заполняется студентом):

| Задание | Выполнение | Баллы |
| ------ | ------ | ------ |
| Задание 1 | * | 60 |
| Задание 2 | * | 20 |
| Задание 3 | * | 20 |

знак "*" - задание выполнено; знак "#" - задание не выполнено;

Работу проверили:
- к.т.н., доцент Денисов Д.В.
- к.э.н., доцент Панов М.А.
- ст. преп., Фадеев В.О.

[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

Структура отчета

- Данные о работе: название работы, фио, группа, выполненные задания.
- Цель работы.
- Задание 1.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Задание 2.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Задание 3.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Выводы.
- ✨Magic ✨

## Цель работы
Ознакомиться с перцептроном.

## Задание 1
### В проекте Unity реализовать перцептрон, который умеет производить вычисления логических операций.
Обучение перцептрона логическими операциями:
- OR обучилось до total_error = 0 за 3 эпохи при 8 эпохах
![image](https://user-images.githubusercontent.com/105049918/205110249-a9a6ecd4-a17d-4392-aa3c-3530032212f7.png)
- AND обучилось до total_error = 0 за 6 эпох при 8 эпохах
![image](https://user-images.githubusercontent.com/105049918/205110996-692baad6-f465-45f7-afc9-5b03ba1a79a4.png)
- NAND обучилось до total_error = 0 за 8 эпох при 8 эпохах
- ![image](https://user-images.githubusercontent.com/105049918/205112546-cbcea12f-7166-4847-aac4-c4edc16cc43e.png)
- XOR не обучилось за 10000 эпох
- ![image](https://user-images.githubusercontent.com/105049918/205113349-18d557dc-8ed1-4511-bb6f-6fa1f9c8515e.png)

## Задание 2
### Построить графики зависимости количества эпох от ошибки обучения. Указать от чего зависит необходимое количество эпох обучения.
![image](https://user-images.githubusercontent.com/105049918/205117081-d3daa795-78cd-4d6f-8dec-a7b4aa05ce33.png)

## Задание 3
### Построить визуальную модель работы перцептрона на сцене Unity
- OR
- ![OR](https://user-images.githubusercontent.com/105049918/205128108-1cfd1f19-a2ff-4da7-a48d-53cc8bee73b2.gif)

```C#
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class ChangeColor : MonoBehaviour
{
    private void OnTriggerEnter(Collider other)
    {
        if (other.gameObject.GetComponent<Renderer>().material.color == Color.white && this.gameObject.GetComponent<Renderer>().material.color == Color.white)
        {
            other.gameObject.GetComponent<Renderer>().material.color = Color.white;
            this.gameObject.GetComponent<Renderer>().material.color = Color.white;
        }
        else
        {
            other.gameObject.GetComponent<Renderer>().material.color = Color.black;
            this.gameObject.GetComponent<Renderer>().material.color = Color.black;
        }
    }
}
```

- AND
- ![AND](https://user-images.githubusercontent.com/105049918/205128503-3d2e636c-c8e9-4ea8-b1e5-a77497144282.gif)


```C#
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class ChangeColor : MonoBehaviour
{
    private void OnTriggerEnter(Collider other)
    {
        if (other.gameObject.GetComponent<Renderer>().material.color == Color.white || this.gameObject.GetComponent<Renderer>().material.color == Color.white)
        {
            other.gameObject.GetComponent<Renderer>().material.color = Color.white;
            this.gameObject.GetComponent<Renderer>().material.color = Color.white;
        }
        else
        {
            other.gameObject.GetComponent<Renderer>().material.color = Color.black;
            this.gameObject.GetComponent<Renderer>().material.color = Color.black;
        }
    }
}
```
## Выводы

Абзац умных слов о том, что было сделано и что было узнано.

| Plugin | README |
| ------ | ------ |
| Dropbox | [plugins/dropbox/README.md][PlDb] |
| GitHub | [plugins/github/README.md][PlGh] |
| Google Drive | [plugins/googledrive/README.md][PlGd] |
| OneDrive | [plugins/onedrive/README.md][PlOd] |
| Medium | [plugins/medium/README.md][PlMe] |
| Google Analytics | [plugins/googleanalytics/README.md][PlGa] |

## Powered by

**BigDigital Team: Denisov | Fadeev | Panov**
