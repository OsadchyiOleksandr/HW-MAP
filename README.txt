На платформі зареєстрована певна кількість імен користувачів, що отримують числовий ідентифікатор як ключ.
Необхідно отримати інформацію про всіх користувачів та про одного за відповідним ідентифікатором.
Функціонал проекту реалізуйте за допомогою можливостей Interface Map

Маємо такий перелік ідентифікаторів та імен:
387 Lucy
231 Alice
394 Bob
172 Tom

Виведення має бути таким:

ALL NAMES:
1) 387, Lucy
2) 231, Alice
3) 394, Bob
4) 172, Tom

NAME: id 172, Tom

(1) Cтворіть проект Names-Map на локальній машині через IntelliJ IDEA (IDE).

(2) Структура проекту має бути такою:

(3) Функціонал класу Main

package app;

public class Main {

    public static void main(String[] args) {
        DataHandler handler = new DataHandler();
        UIOperator uiOperator = new UIOperator();
        uiOperator.getOutput(handler.getAll());
        uiOperator.getOutput(handler.getById(172));
    }
}

(4) Функціонал класу UIOperator

package app;

public class UIOperator {

    public void getOutput(String output) {
        System.out.println(output);
    }
}

(5) Доопрацюйте функціонал класу DataRepository

package app;

import java.util.HashMap;
import java.util.Map;

public class DataRepository {

    public Map<, String> getData() {
        Map<Integer, > map = new HashMap<>();

        return map;
    }
}

(6) Доопрацюйте функціонал класу DataHandler

package app;

import java.util.Map;
import java.util.concurrent.atomic.AtomicInteger;

public class DataHandler {

    Map<Integer> map = new DataRepository();

    // Метод формує виведення нумерованого переліку імен
    public String getAll() {
        StringBuilder sb = new StringBuilder();
        AtomicInteger count = new AtomicInteger(0);
        map.forEach((id, name) ->
                sb.append(.format("%d) %d, %s%n",
                        count.incrementAndGet(),id, name)
                ));
        return "\\nALL NAMES:\\n" + sb;
    }

    // Метод формує виведення імені за певним id
    public String getById(int ) {
        if (coKey(id)) {
            return "\\nNAME: id " + id + ", " +
                    map.(id);
        } else return "No data!";
    }
}

(7) Залийте виконаний проект на свій GitHub репозиторій, посилання на який зазначте в LMS.



