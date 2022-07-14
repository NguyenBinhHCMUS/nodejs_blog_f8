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
