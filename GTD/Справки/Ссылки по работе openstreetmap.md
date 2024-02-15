```dataview
TABLE without id file.outlinks AS "Исходящие", file.inlinks AS "Обратные" WHERE file.name = this.file.name
```
```dataview
TABLE without id dateformat(this.file.ctime, "dd.MM.yyyy HH:mm") as "Создана", dateformat(this.file.mtime, "dd.MM.yyyy HH:mm") as "Обновлена" WHERE file.name = this.file.name
```

#справка

# Связи
[РИАС](../Проекты/РИАС.md)

# Описание

- Рисование [дорог](https://gis.stackexchange.com/questions/84954/how-can-i-get-clean-road-attributes-from-osm-data)
- [Объект](https://wiki.openstreetmap.org/wiki/Key:highway) дорог
- [Карта](https://overpass-turbo.eu) с запросом данных по кировской области

Отдельно запрос:
```
[out:json][timeout:150];
{{geocodeArea:Kirov Oblast}}->.searchArea;
(
  relation["admin_level"="4"](area.searchArea);
  relation["admin_level"="6"](area.searchArea);
);

out body;
>;
out skel qt;
```