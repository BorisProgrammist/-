# Итоговая работа по основному блоку

 **Задача:**

Написать программу, которая из имеющегося массива строк формирует новый массив из строк, длина которых меньше, либо равна 3 символам. Первоначальный массив можно ввести с клавиатуры, либо задать на старте выполнения алгоритма. При решении не рекомендуется пользоваться коллекциями, лучше обойтись исключительно массивами.

**Алгоритм решения**

1. *Необходимо задать исходный массив строк*

string[] originalArray = { "apple", "cat", "dog", "banana", "fox", "tree", "sun" };

2. *Определить размер нового массива для коротких строк (<= 3 символов)*

int shortStringsCount = 0;

        foreach (string str in originalArray)
        {
            if (str.Length <= 3)
            {
                shortStringsCount++;
            }
        }
3. *Создать новый массив для коротких строк*

string[] shortStrings = new string[shortStringsCount];

4. *Заполнить новый массив короткими строками*

int index = 0;

        foreach (string str in originalArray)
        {
            if (str.Length <= 3)
            {
                shortStrings[index] = str;
                index++;
            }
        }

5. *Вывод нового массива на экран*

Console.WriteLine("Short Strings (length <= 3):");

        foreach (string str in shortStrings)
        {
            Console.WriteLine(str);
        }