# Less1.2

## Задание №1

1. В терминал введена команда.
2. Производится системный вызов fork(), который на основе текущего процесса командного интерпретатора создаёт новый дочерний процесс. Память исходного процесса копируется в дочерний, дочернему процессу присваевается новый PID.
3. В исходном процессе производится системный вызов wait() для последующего корретного завершения дочернего процесса.
4. Внутри дочернего процесса производится системный вызов exec(), в который передается команда, введенная в терминал.
5. После вызова exec() дочерний процесс шлет родительскому сигнал о своем завершении с помощью системного вызова exit().
6. Дочерний процесс успешно завершен.

## Задание №2

Тут немного покреативил и задал кастомные имена для колонок.

```ps ax -o pid=ProccessID,ruser=RealUser,%cpu,vsz=AllocatedMemory,tt=CtrlTerminal,command | head```

![Форматированный вывод ps](/homework/Less1.2/ps-output.png)

## Задание №3

![Создание и принудительное завершение процесса](/homework/Less1.2/infinity-kill.png)
