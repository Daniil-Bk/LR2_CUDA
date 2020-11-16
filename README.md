  Массовый поиск подстрок с использованием CUDA
  
 На ввод программы подается текст ALICE'S ADVENTURES IN WONDERLAND.
 Программа ищет подстроку Alice, выводит количество вхождений подстроки и время работы программы.
 
 В программе используются 2 функции для поиска на CPU и GPU.
 
 Описание работы алгоритма на GPU
 
 Каждый поток проверяет символ, который ему сопоставлен. Если проверяемый символ не является первым символом ключевой строки, то поток завершает выполнение.
 Если проверяемый символ является первым символом ключевой строки, поток начинает проверять следующие символы.
 Если все следующие символы совпадают с символами ключевой строки, поток сохраняет индекс первого символа.
 
 Результаты работы
При количестве строк 3589
Time GPU 0.7598 ms
Time CPU = 1.000000 ms

При увеличении строк до 21529
Time GPU 8.8272 ms
Time CPU = 4.000000 ms

Таким образом, можно сделать вывод об увеличении производительности поиска на заданном объеме данных и снижение производительности при увеличении объема.
