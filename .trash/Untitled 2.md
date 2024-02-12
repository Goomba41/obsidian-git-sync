```dataview
TABLE without id file.outlinks AS "Исходящие", file.inlinks AS "Обратные" WHERE file.name = this.file.name
```
```dataview
TABLE without id dateformat(this.file.ctime, "dd.MM.yyyy HH:mm") as "Создана", dateformat(this.file.mtime, "dd.MM.yyyy HH:mm") as "Обновлена" WHERE file.name = this.file.name
```

#напоминание
- [ ] Завершение «Untitled (@2024-02-12 11:21)»

# Связи

# Участники

# Повестка
%% Запишите основную тему для обсуждения%%
# Заметки
%% Ключевая информация %%