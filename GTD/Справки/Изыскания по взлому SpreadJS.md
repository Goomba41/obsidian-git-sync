```dataview
TABLE without id file.outlinks AS "Исходящие", file.inlinks AS "Обратные" WHERE file.name = this.file.name
```
```dataview
TABLE without id dateformat(this.file.ctime, "dd.MM.yyyy HH:mm") as "Создана", dateformat(this.file.mtime, "dd.MM.yyyy HH:mm") as "Обновлена" WHERE file.name = this.file.name
```

#справка

# Связи
Проекты:
 - [РИАС](../Проекты/РИАС.md)

Задачи:
 - [Взлом SpreadJS](../Задачи/Взлом%20SpreadJS.md)

Персоны:
 - %% персона %%

Справки:
 - %% справка %%
 
# Описание

Для начала мы нашли 