<template>
  <!DOCTYPE html>
<html>

<head>
  <meta charset="UTF-8">
  <title>Informer</title>
  <link rel="stylesheet" href="style.css">
</head>

<body>

  <div class="app">
    <div class="informer-container">

      <div class="temperature">
        <img src="../assets/thermometer.png">
        <div class="temp-real">{{weather.temperatureReal}}</div>
        <div class="temp-feel">{{weather.temperatureFeel}} </div>
      </div>

      <div class="flex-break"></div>

      <div class="humidity">
        <img src="../assets/humidity.png"> {{weather.humidity}} <small>%</small>
      </div>

      <div class="vertical-divider"></div>

      <div class="wind">
        <img src="../assets/wind.png"> {{weather.wind}} <small>м/с</small>
      </div>

    </div>
  </div>

</body>

</html>
</template>

<script>
export default{
  name: 'FirstComponent',
  props:{
    weather:{
      type:Object
    }
  }
}

</script>

<style>
body {
  margin: 0;
  padding: 0;
}

.app {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100vh;
  background: rgb(244, 123, 186);
  background: linear-gradient(-25deg, rgba(244, 123, 186, 0.5) 20%, rgba(90, 95, 245, 0.5) 80%);
}

.informer-container {
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  flex-wrap: wrap;
  width: 400px;
  padding: 30px;
  background-image: url('../assets/wind.png');
  background-size: cover;
  background-position: center center;
  border-radius: 20px;
  box-shadow: 0px 0px 10px 0px rgba(50, 50, 50, 0.75);
}

.temperature {
  display: flex;
  align-items: flex-end;
  margin: 15px;
}

.temp-real {
  position: relative;
  display: inline-block;
  font-family: 'Arial', sans-serif;
  font-size: 100px;
  font-weight: 400;
  color: #fff;
  line-height: 0.9;
  text-shadow: 2px 2px 2px #444;
}

.temp-real:after {
  content: 'o';
  color: #fff;
  font-size: 35px;
  position: absolute;
  top: -15px;
  right: -25px;
}

.temp-feel {
  position: relative;
  box-sizing: border-box;
  padding-right: 15px;
  margin-left: 20px;
  text-align: right;
  text-shadow: 2px 2px 2px #444;
  font-family: 'Arial', sans-serif;
  font-size: 30px;
  font-weight: 400;
  color: #eee;
}

.temp-feel:before {
  content: 'Ощущается';
  display: block;
  position: absolute;
  right: 0;
  top: -17px;
  font-size: 15px;
}

.temp-feel:after {
  position: absolute;
  top: -4px;
  right: 2px;
  content: 'o';
  font-size: 16px;
  font-weight: 700;
  color: #eee;
}

.temperature img {
  width: 70px;
  vertical-align: middle;
}


.humidity {
  display: inline-block;
  position: relative;
  margin: 15px;
  text-shadow: 2px 2px 2px #444;
  font-family: 'Arial', sans-serif;
  font-size: 40px;
  font-weight: 400;
  color: #fff;
  line-height: 0.9;
}

.humidity small {
  font-size: 30px;
  margin-left: -5px;
}

.humidity img {
  width: 30px;
  margin-right: -10px;
  vertical-align: middle;
}


.wind {
  font-family: 'Arial', sans-serif;
  font-size: 40px;
  font-weight: 400;
  color: #fff;
  position: relative;
  display: inline-block;
  line-height: 0.9;
  text-shadow: 2px 2px 2px #444;
  margin: 15px;
}

.wind img {
  width: 30px;
  margin-right: -5px;
  vertical-align: middle;
}



.flex-break{
  flex-basis: 100%;
  height: 0;
}

.vertical-divider{
  height: 70px;
  width: 1px;
  background-color: #fff;
  vertical-align: middle;
  display: table-cell;
}
</style>
