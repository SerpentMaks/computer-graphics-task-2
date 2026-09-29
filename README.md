# Computer Graphics — Task 2

> Учебная задача на C с отдельными модулями сортировки и поиска и автоматическими тестами.

## Реализованные модули

CMake собирает статическую библиотеку:

`edu_sort_and_search`

из двух исходников:

- `src/edu_sort.c` — операции сортировки;
- `src/edu_search.c` — операции поиска.

Публичные заголовки находятся в `include/`.

## Тестирование

Проект использует **Criterion 2.4.2** и CTest.

В сборку включены строгие предупреждения:

```text
-Wall -Wextra -pedantic -Werror
```

и sanitizers:

- AddressSanitizer;
- LeakSanitizer;
- UndefinedBehaviorSanitizer.

## Сборка

```bash
cmake -S . -B build
cmake --build build
ctest --test-dir build --output-on-failure
```

## Структура

```text
include/   # заголовочные файлы
src/       # сортировка и поиск
test/      # тесты
external/  # Criterion
CMakeLists.txt
```

## Статус

🎓 Учебный C-проект с тестированием.
