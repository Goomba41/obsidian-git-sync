```dataview
TABLE without id file.outlinks AS "Исходящие", file.inlinks AS "Обратные" WHERE file.name = this.file.name
```
```dataview
TABLE without id dateformat(this.file.ctime, "dd.MM.yyyy HH:mm") as "Создана", dateformat(this.file.mtime, "dd.MM.yyyy HH:mm") as "Обновлена" WHERE file.name = this.file.name
```

#задача/сейчас %% сейчас | потом | ожидание | однажды %%
- [ ] Завершение «Объединение репозиториев и перенос на ubuntu»

# Ссылки
[КСО](../Проекты/КСО.md); [Организация рабочего потока](../../Wiki/Программирование/GIT/Организация%20рабочего%20потока.md)

# Описание

- [x] Объединить код
- [x] Разветвить
- [x] Переместить issues
- [ ] Переделать ci/cd
- [ ] Заархивировать репозитории
- [ ] Переписать нормальный README
- [ ] Перенос сборки репозитория (@2024-02-16 10:21)
- [ ] Билд на разные поддомены?
- [x] Погуглить md для gitlab (Сделал Аркадий)