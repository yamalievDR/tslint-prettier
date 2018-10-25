# Tslint и Prettier

Для настройки tslint'а и prettier'a необходимо выполнить:

```
npm i tslint-config-prettier -D
npm i prettier -D
```
Установить плагин для IDE

Если используется IntelliJ, то установить [File Watcher](https://www.jetbrains.com/help/phpstorm/settings-tools-file-watchers.html) для форматирования при сохранении файла.
Далее зайти в настройки `Ctrl+Alt+S` -> Tools -> File Watcher -> + -> Prettier -> Выбрать TypeScript

Если VS Code, то установить prettier. В пользовательских настройках добавить `"editor.formatOnSave": true`

Добавить в конец файла tslint.json 
```
"extends": [
    "tslint:latest",
    "tslint-config-prettier"
  ]
```

Создать файл `.prettierrc` в корне проекта. Внутрь положить:
```
{
 "printWidth": 120,
 "singleQuote": true,
 "useTabs": false,
 "tabWidth": 2,
 "semi": true,
 "bracketSpacing": true
}
```
