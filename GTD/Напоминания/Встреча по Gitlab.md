```dataview
TABLE without id file.outlinks AS "Исходящие", file.inlinks AS "Обратные" WHERE file.name = this.file.name
```
```dataview
TABLE without id dateformat(this.file.ctime, "dd.MM.yyyy HH:mm") as "Создана", dateformat(this.file.mtime, "dd.MM.yyyy HH:mm") as "Обновлена" WHERE file.name = this.file.name
```

#напоминание
- [x] Завершение «Встреча по Gitlab (@2024-05-16 14:55)»

# Связи

# Участники

# Повестка
Обсуждение возможности перевода проектов всех структурных подразделений компании в Gitlab. Обусждение возможностей gitlab, пожеланий и прочих вопросов

# Заметки
%% Ключевая информация %%