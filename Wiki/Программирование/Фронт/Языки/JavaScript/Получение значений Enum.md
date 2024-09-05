Код фукнции:

```ts
/**
 * Функция, которая возвращает данные из перечисляемого типа в виде массива данных
 *
 * @example Пример использования:
 * ```
 * getFromEnum('objects', enum)
 * ```
 * 
 * @export
 * @param {'object'} output
 * тип элементов результирующего массива
 *
 * @param {enum} enumObject
 * перечисляемый тип
 * 
 * @example Пример:
 * ```
 *  enum edges {
      ValueMin,
      ValueMax,
    }
 * ```
 * 
 * @returns {{ id: number | string; value: string | number }[]} массив объектов
 * @example Пример результата:
 * ```
 * [{ id: 0, value: 'ValueMin' }, { id: 1, value: 'ValueMax' }]
 * ```
 */
export function getFromEnum(
  output: 'objects',
  enumObject: Object
): { id: number | string; value: string | number }[];
/**
 * Функция, которая возвращает данные из перечисляемого типа в виде массива данных
 *
 * @example Пример использования:
 * ```
 * getFromEnum('values', enum)
 * ```
 * 
 * @export
 * @param {'values'} output
 * тип элементов результирующего массива
 *
 * @param {enum} enumObject
 * перечисляемый тип
 * 
 * @example Пример:
 * ```
 *  enum edges {
      ValueMin,
      ValueMax,
    }
 * ```
 * 
 * @returns {string[]} массив значений перечисляемого типа
 * @example Пример результата:
 * ```
 * ['ValueMin', 'ValueMax']
 * ```
 */
export function getFromEnum(output: 'values', enumObject: Object): string[];
/**
 * Функция, которая возвращает данные из перечисляемого типа в виде массива данных
 *
 * @example Пример использования:
 * ```
 * getFromEnum('keys', enum)
 * ```
 * 
 * @export
 * @param {'keys'} output
 * тип элементов результирующего массива
 *
 * @param {enum} enumObject
 * перечисляемый тип
 * 
 * @example Пример:
 * ```
 *  enum edges {
      ValueMin,
      ValueMax,
    }
 * ```
 * 
 * @returns {{ id: number | string; value: string | number }[]} массив ключей перечисляемого типа
 * @example Пример результата:
 * ```
 * [0, 1]
 * ```
 */
export function getFromEnum(output: 'keys', enumObject: Object): number[];
export function getFromEnum(output: 'keys' | 'values' | 'objects', enumObject: Object) {
  const isNumeric: boolean = Object.keys(enumObject).some((value) => !isNaN(Number(value)));

  if (isNumeric) {
    const items = Object.keys(enumObject);
    const values = items.filter((v) => isNaN(Number(v)));

    if (output === 'keys') return items.filter((v) => !isNaN(Number(v))).map((v) => Number(v));
    if (output === 'values') return values;
    if (output === 'objects')
      return values.map((value) => {
        return {
          id: (enumObject as { [key: string | number]: string | number })[value],
          value,
        };
      });
  } else {
    const items = Object.keys(enumObject);
    if (output === 'keys') return items;
    if (output === 'values') return Object.values(enumObject);
    if (output === 'objects')
      return items.map((id) => {
        return {
          id,
          value: (enumObject as { [key: string | number]: string | number })[id],
        };
      });
  }

  throw new TypeError('"enumObject" parameter is not of type Enum');
}
```