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



* {
  margin: 10px;
  outline: none;
  padding: 0;
  box-sizing: border-box;
  transition: 0.3s ease;
  letter-spacing: 1px;
  font-family: Comfortaa;
}

@font-face {
  font-family: Comfortaa;
  src: url("./fonts/Comfortaa.ttf");
}

.logo {
  height: 120px;
  width: 100px;
}

.header {
  display: flex;
  align-items: center;
  text-align: center;
  justify-content: center;
  flex-direction: column;
}

.gray {
  color: rgb(54, 54, 54);
  font-weight: 1000;
}

.blue {
  color: #4285f4;
  font-weight: 100;
}

body {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  flex-direction: column;
}

#label {
  font-weight: 600;
  font-size: 20px;
  color: rgb(63, 63, 63);
}

input {
  padding: 5px;
  border: none;
  border-radius: 50px;
  box-shadow: 1px 1px 5px black;
  font-family: Comfortaa;
  font-size: 15px;
  height: 3rem;
  width: 15rem;
  padding-left: 20px;
}

button {
  padding: 7px;
  background: #4285f4;
  color: white;
  border-radius: 25px;
  border: none;
  height: 3rem;
  width: 10rem;
}

#show-age {
  font-size: 20px;
  text-align: center;
}




// calculate age
let daysH = document.getElementById("date");
let monthH = document.getElementById("month");
let yearH = document.getElementById("year");

let showAge = document.getElementById("show-age");




const btn = document.getElementById("calc-btn");

var today = new Date();
let d = today.getDate();
var m = today.getMonth() + 1;
var y = today.getFullYear();
let maxDays = 0;
let monthNum = 1;

btn.addEventListener("click", (days, month, year) => {

    days = daysH.value;
    month = monthH.value;
    year = yearH.value;

    if (daysH.value == "" || monthH.value == "" || yearH.value == "") {
        return alert("Please enter your date of birth properly to calculate your age")
    }

    // no else condition needed

    console.log(`Current Date : ${d} ${m} ${y}`);

    if (m == 1) { // january
        maxDays = 31;
        monthNum = 1;
    }
    else if (m == 2) { // february
        maxDays = 28;
        monthNum = 2;
    }
    else if (m == 3) { // march
        maxDays = 31;
        monthNum = 3;
    }
    else if (m == 4) { // april
        maxDays = 30;
        monthNum = 4;
    }
    else if (m == 5) { // may
        maxDays = 31;
        monthNum = 5;
    }
    else if (m == 6) { // june
        maxDays = 30;
        monthNum = 6;
    }
    else if (m == 7) { // july
        maxDays = 31;
        monthNum = 7;
    }
    else if (m == 8) { // august
        maxDays = 31;
        monthNum = 8;
    }
    else if (m == 9) { // september
        maxDays = 30;
        monthNum = 9;
    }
    else if (m == 10) { // october
        maxDays = 31;
        monthNum = 10;
    }
    else if (m == 11) { // november
        maxDays = 30;
        monthNum = 11;
    }

    // make december else or else if it's your choice

    else { // december
        maxDays = 31;
        monthNum = 12;
    }


    var ageYears = y - year;

    if (m <= month) {
        m = m + 12;
    }
    var ageMonths = m - month;
    var ageDays = (maxDays - d) + parseInt(days);


    // console.log(typeof days); // string why????

    showAge.innerHTML = `Your age is ${ageYears} year(s) , ${ageMonths} month(s) and ${ageDays} day(s)`;
})

```
