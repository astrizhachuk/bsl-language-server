# Лишняя директивы компиляции (CompilationDirectiveNeedLess)

| Тип | Поддерживаются<br/>языки | Важность | Включена<br/>по умолчанию | Время на<br/>исправление (мин) | Тэги |
| :-: | :-: | :-: | :-: | :-: | :-: |
| `Дефект кода` | `BSL` | `Важный` | `Да` | `1` | `clumsy` |

<!-- Блоки выше заполняются автоматически, не трогать -->
## Описание диагностики

Директивы компиляции:

```bsl
&НаКлиенте (&AtClient)
&НаСервере (&AtServer)
&НаСервереБезКонтекста (&AtServerNoContext)
```

Следует применять только в коде модулей управляемых форм и в коде модулей команд. В остальных модулях рекомендуется 
применять инструкции препроцессору.

В серверных или клиентских общих модулях контекст исполнения очевиден, поэтому смысла в директивах компиляции нет. 
В общих модулях с признаками клиент и сервер применение директив компиляции затрудняет понимание, какие же 
процедуры (функции) доступны в конечном итоге.

## Источники
* Источник: [Использование директив компиляции и инструкций препроцессора](https://its.1c.ru/db/v8std#content:453:hdoc)

## Сниппеты

<!-- Блоки ниже заполняются автоматически, не трогать -->
### Экранирование кода

```bsl
// BSLLS:CompilationDirectiveNeedLess-off
// BSLLS:CompilationDirectiveNeedLess-on
```

### Параметр конфигурационного файла

```json
"CompilationDirectiveNeedLess": false
```