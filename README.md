# JS style

# 1. Перенос кода в функцию #

  `var width = (value - 0.5) * 16;`
  - Не слишком понятно

  `var width = emToPixels(value);`

  `function emToPixels(ems) {
      return (ems - 0.5) * 16;
  }`

  - Название функции описывает то, что она делает, и этот код не нуждается в дальнейших уточнениях.

# 2. Объявление переменных #

  - Используйте ключевое слово var
  `var x = 42;`

  - Просто присвоить переменной значение
  `x = 42;`
  - Не рекомендуется использовать данный способ.

# 3. Используйте пробелы, а не табы #

  😃 Следует использовать два пробела (не четыре)
  - Плохо:
  `function bar() {
  ∙let name;
  }`

  - Хорошо:
  `function baz() {
  ∙∙let name;
  }`

# 4. Точки с запятыми обязательны #

  - Плохо:
  `let luke = {}`
  `let leia = {}`
  `[luke, leia].forEach(jedi => jedi.father = 'vader')`

  - Хорошо:
  `let luke = {};`
  `let leia = {};`
  `[luke, leia].forEach((jedi) => {
    jedi.father = 'vader';
  });`

# 5. Больше не используйте var #

  😃 Объявляйте все переменные с помощью const или let.
  - Плохо:
  `var example = 42;`

  - Хорошо:
  `let example = 42;`

# 6. Не используйте символов продолжения строки для длинных строк #

  - Плохо: 
  `(sorry, this doesn't show up well on mobile)
    const longString = 'This is a very long string that \
    far exceeds the 80 column limit. It unfortunately \
    contains long stretches of spaces due to how the \
    continued lines are indented.';`
 
  - Хорошо:
    `const longString = 'This is a very long string that ' + 
    'far exceeds the 80 column limit. It does not contain ' + 
    'long stretches of spaces since the concatenated ' +
    'strings are cleaner.';`

# 7. Не используйте eval() #

  - Плохо: 
  `let obj = { a: 20, b: 30 };`
  `let propName = getPropName();  // returns "a" or "b"`
  `eval( 'var result = obj.' + propName );`

  - Хорошо:
  `let obj = { a: 20, b: 30 };`
  `let propName = getPropName();  // returns "a" or "b"`
  `let result = obj[ propName ];  //  obj[ "a" ] is the same as obj.a`

# 8. Объявляйте переменные по одной #

  - Плохо:
  `let a = 1, b = 2, c = 3;`

  - Хорошо:
  `let a = 1;`
  `let b = 2;`
  `let c = 3;`

# 9. Используйте одинарные, а не двойные кавычки #

  - Плохо:
  `let directive = "No identification of self or mission."`

  - Хорошо:
  `let directive = 'No identification of self or mission.';`

# 10.  Горизонтальное выравнивание не поощряется (но не запрещается) #
  
  - Плохо:
  `{
  tiny:   42,  
  longer: 435, 
};`

  - Хорошо:
`{
  tiny: 42, 
  longer: 435,
};`


