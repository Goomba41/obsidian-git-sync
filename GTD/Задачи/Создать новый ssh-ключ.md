```dataview
TABLE without id file.outlinks AS "Исходящие", file.inlinks AS "Обратные" WHERE file.name = this.file.name
```
```dataview
TABLE without id dateformat(this.file.ctime, "dd.MM.yyyy HH:mm") as "Создана", dateformat(this.file.mtime, "dd.MM.yyyy HH:mm") as "Обновлена" WHERE file.name = this.file.name
```

#задача/сейчас %% сейчас | потом | ожидание | однажды %%
- [ ] Завершение «Создать новый ssh-ключ»

# Ссылки

Проекты:
 - [КСО](../Проекты/КСО.md)

Задачи:
 - %% задача %%

Персоны:
 - %% персона %%

Справки:
 - %% справка %%

# Описание

- [ ] Создать новый ssh-ключ для Gitlab (@2024-03-25)