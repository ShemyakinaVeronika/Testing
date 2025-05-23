# Testing

[![Build Status](https://github.com/ShemyakinaVeronika/Testing/actions/workflows/testing.yml/badge.svg?branch=main)](https://github.com/ShemyakinaVeronika/Testing/actions/workflows/testing.yml) <br>

| Название | Описание|Тип теста| Входные данные | Ожидаемый результат|
|---|---|---|---|---|
| test_positive_discriminant | Проверяет, что функция quadratic_equation возвращает список с двумя корнями уравнения при положительном дискриминанте. | позитивный | a = 1 <br> b = -5 <br> c = -6 | [2.0, 3.0] |
| test_zero_discriminant | Проверяет, что функция quadratic_equation возвращает список с одним корнем уравнения при дискриминанте равным 0. | позитивный |  a = 1 <br> b = -2 <br> c = -1 | [1.0] |
| test_negative_discriminant | Проверяет, что функция quadratic_equation возвращает сообщение "Действительных корней нет." при отрицательном дискриминанте. | позитивный | a = 3 <br> b = -1 <br> c = 7| "Действительных корней нет." |
| test_wrong_type_parameters |	Проверяет, что функция quadratic_equation возвращает сообщение "Неверный тип коэффициентов, необходимы действительные числа", если хотя бы один параметр не является целым или вещественным числом. | негативный| a = "string" <br> b = 3 <br> c = -4; <br> a = 1 <br> b = [3] <br> c = -4; <br> a = 4 <br> b = 3 <br> c = "string"; | "Неверный тип коэффициентов, необходимы действительные числа." |
| test_a_equals_zero | Проверяет, что функция quadratic_equation возвращает сообщение "Это не квадратное уравнение." при a = 0. | негативный| a = 0 <br> b = 2 <br>c = -4 | "Это не квадратное уравнение." |
| test_b_equals_zero_c_greater_zero | Проверяет, что функция quadratic_equation возвращает сообщение об ошибке "Уравнение имеет комплексные корни.", при b = 0, c > 0. | негативный | a = 2 <br> b = 0 <br> c = 16| "Уравнение имеет комплексные корни." |
| test_less_number_of_parameters | 	Проверяет, что функция quadratic_equation возвращает ошибку TypeError, если в функцию переданы не все аргументы. | негативный | b = 1 <br> c = 3 | TypeError |
| test_more_number_of_parameters | Проверяет, что функция quadratic_equation возвращает ошибку TypeError, если в функцию передано больше трех аргументов. | негативный | 	a = 4 <br> b = -1 <br> c = 3 <br> d = 14 | TypeError |
