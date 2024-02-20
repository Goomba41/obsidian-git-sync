```dataview
TABLE without id file.outlinks AS "Исходящие", file.inlinks AS "Обратные" WHERE file.name = this.file.name
```
```dataview
TABLE without id dateformat(this.file.ctime, "dd.MM.yyyy HH:mm") as "Создана", dateformat(this.file.mtime, "dd.MM.yyyy HH:mm") as "Обновлена" WHERE file.name = this.file.name
```

#задача/ожидание %% сейчас | потом | ожидание | однажды %%
- [x] Завершение «Обновить CI»

# Ссылки
[КСО](../Проекты/КСО.md)
[Аркадий Вадимович Челядников](../Справки/Персоны/Аркадий%20Вадимович%20Челядников.md)

# Описание

Аркадий попросил обновить CI шагом генерации шаблона пустой базы