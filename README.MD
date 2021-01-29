```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="./css/style.css" />
    <title>Age Calculater</title>
  </head>
  <body>
    <div class="logo"><img src="./logo/incubical.svg" /></div>
    <div class="header">
      <h1 class="gray">
        Know your
        <h1 class="blue">EXACT</h1>
        <h1 class="gray">age</h1>
      </h1>
    </div>
    <label id="label" for="input">Enter your date of birth </label>
    <input type="number" id="date" placeholder="date" />
    <input type="number" id="month" placeholder="month" />
    <input type="number" id="year" placeholder="year" />
    <button id="calc-btn">Submit</button>

    <p id="show-age"></p>

    <script src="./app/app.js"></script>
  </body>
</html>
```
