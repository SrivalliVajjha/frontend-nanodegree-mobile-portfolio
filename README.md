## Guidelines 

- The source code is in folder **src**.
- The production code(with minified code) is in directory **dist**.
- Run the `index.html` from **dist** directory.
- For viewing the source code, refer the **src** directory.
- Use **ngrok.exe** in **dist** directory to host index.html on server for testing on Pagespeed Insights.
To use **ngrok.exe**, run it, and in command box, type `./ngrok http 8000` 

## Optimizations made to `index.html`

- Fonts css made to load asynchronously.
- Style css made internal rather than external.
- `Media="print"` added for `print.css`.
- Optimized jpeg files `img/profilepic.jpg` and `views/images/pizzeria.jpg`.
- Set the JS files to `async`.
- Moved Google Analytics `<script>` file to bottom of `<body>`.

## Optimizations made to `views/js/main.js` and `views/css/style.css`

#### For achieving 60fps
- Made `items` and `itemLength` as global variable and defined it outside `updatePositions()`.
- Moved few variables outside `for` loop in `updatePositions()`.
- Used `style.transform` property instead of `style.left` property.
- Number of pizzas in background is calculated according to the screen height.
- Replaced `querySelector` by `getElement method`.
- Modified the `.mover` class in CSS file.

#### For resizing pizza within 5ms
- Moved few variables out of `resizePizzas()` function.
- Replaced `querySelector` by `getElement method`.
- Optimized switch function to directly change the width in `changePizzaSizes()` function.