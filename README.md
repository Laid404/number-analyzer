# number_analyzer.py

# Список для хранения введённых чисел
numbers = []

# Инициализация счётчиков
positive = 0
negative = 0
zeros = 0
even = 0
odd = 0

# Запрашиваем у пользователя 8 чисел
for i in range(8):
    x = int(input(f"Введите число {i + 1}: "))
    numbers.append(x)

    # Положительные / отрицательные / ноль
    if x > 0:
        positive += 1
        print("Положительное")
    elif x < 0:
        negative += 1
        print("Отрицательное")
    else:
        zeros += 1
        print("Ноль")

    # Чётные / нечётные
    if x % 2 == 0:
        even += 1
        print("Чётное")
    else:
        odd += 1
        print("Нечётное")

# Считаем сумму, среднее, максимум и минимум
total = sum(numbers)
average = total / len(numbers)
maximum = max(numbers)
minimum = min(numbers)

# Выводим результаты
print("\nРезультаты анализа чисел:")
print("Сумма:", total)
print("Среднее:", average)
print("Максимум:", maximum)
print("Минимум:", minimum)
print("Положительные числа:", positive)
print("Отрицательные числа:", negative)
print("Нулей:", zeros)
print("Чётные числа:", even)
print("Нечётные числа:", odd)
