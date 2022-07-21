# Tạo dự án

npm init

# Taọ file entry point

Tạo file index.js

# Cày đặt Express

npm i express

# Start project

node index.js

# Install nodemon

listening onchange
npm i -g nodemon

add package.json::
script: {
...
"start": "nodemon --inspect index.js",
}
==> start: npm start

# Install Morgan

Quan sát các log từ client lên server.
npm i morgan
var morgan = require('morgan)

# Template engine (handlebars)

npm i express-handlebars

# Install node-sass

npm i node-sass --save-dev
Cập nhật đường dẫn package.json/script: "watch": "node-sass --watch src/resources/scss/app.scss src/public/css/app.css"
npm run watch: compile app.scss => app.css

# Form default html bahavior

- Phương thức mặc định: method="GET"
- Hàm submit lấy giá trị value dựa vào name trong thẻ input và truyền lên query parameters
- Khi đổi method form sang POST thì f5 lại trang sẽ là phương thức post, khi vào lần đầu tiên nó là GET.
- Attribute action="", cho chúng ta biết chúng ta submit ở đâu. Mặc định sẽ lấy url hiện tại.

# Mô hình MVC]

M: model tương tác với resource để lấy dữ liệu.
V: view chứ các file html, css
C: control trung chuyển giữa view và model

# Prettier

npm i husky prettier lint-staged --save-dev

prettier: format code
lint-staged: format code khi thao tác vói git
husky: tự động chạy prettier và lint-staged

.prettierrc
{
"bracketSpacing": true,
"printWidth": 100,
"singleQuote": true,
"trailingComma": "all",
"tabWidth": 2,
"useTabs": false,
"semi": true
}

"scripts": {
...
"format": "prettier --write src",
},

.huskyrc

{
"hooks": {
"pre-commit": "lint-staged"
}
}

package.json

```js
"scripts": {
    ...
    "precommit": "yarn run lint && yarn test",
    "prepush": "yarn run lint",
},
"husky": {
    "hooks": {
        "pre-commit": "lint-staged"
    }
}
```
