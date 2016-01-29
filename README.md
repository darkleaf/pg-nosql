# pg-nosql

Основа - http://jsonapi.org/format/


```
#Базовая табличка
id: int
data: jsonb
mixins: array[string]
type: strign??

#Доступные функции
upsert???
find_TYPE
find_MIXIN
wrap_TYPE(row): json
getId

удалять ничего нельзя

#Схема data
{
  id: int,
  type: string,
  attributes: {},
  relationships: {},
  meta: {}
}

mixin: {
  validate(data),
  beforeUpsert(data, diff), #добавить блокировки
  upsert(data, diff),
  filter(obj): req_builder
  reduce(obj, row): obj # добавляет в итоговый объект необозимые данные 
}

#вопросы
1. full_text highlight
2. counter_cache
```
