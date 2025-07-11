АНАЛИЗ СТРУКТУРЫ ПРОГРАММЫ

1. Формирование графического интерфейса (GUI).
   Программа создает окно входа с современным и удобным для пользователя внешним видом на основе библиотеки `tkinter`. Окно открывается в полноэкранном режиме, а в качестве фонового изображения на весь экран отображается файл `fon2.png`. Это обеспечивает визуально приятный интерфейс для пользователя.

2. Окна ввода логина и пароля.
   Поля логина и пароля размещены с использованием центральных координат. Они требуют от пользователя ввода необходимых данных для входа. Эти поля состоят из компонентов `Label` и `Entry`, которые размещаются на экране с помощью `Canvas`. Поле логина отображает вводимые символы, а поле пароля скрывает их с помощью символов-звездочек.

3. Аутентификация пользователя (проверка).
   Функция `login_check()` проверяет введённые пользователем логин и пароль. В данном случае логин должен быть равен `"admin"`, а пароль — `"1234"`. Несмотря на простоту, такая система аутентификации широко используется в тестовом режиме или на этапе разработки. В реальных проектах этот компонент должен быть интегрирован с базой данных (например, MySQL, SQLite, PostgreSQL и др.).

4. Условная навигация (переход к новому модулю).
   Если пользователь вводит правильные данные, с помощью `messagebox` выводится уведомление об успешном входе, а файл `bosh.py` запускается в новом окне с помощью `subprocess.Popen`. Затем функция `root.after()` через 0,5 секунды закрывает старое окно входа (`root.destroy()`).

5. Обработка ошибок и взаимодействие с пользователем.
   Если пользователь вводит неверные данные, появляется предупреждающее сообщение об ошибке с помощью `messagebox.showerror()`. Эта функциональность побуждает пользователя к быстрому исправлению ошибок.

6. Возможность быстрого выхода из интерфейса.
   К окну входа привязана клавиша `<Escape>`. При её нажатии программа немедленно завершает работу. Это является удобной возможностью навигации в GUI-программах.



