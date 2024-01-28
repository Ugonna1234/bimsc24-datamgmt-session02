<!-- the script is where the js code goes -->
<script>



</script>

<!-- the template is where the html code goes -->
<template>

    <div id="navbar" class="container">  
        <div id="title">You win ${{dollaramount}}</div>
        <div id="logo">
            <img src="./cow.jpg" alt="macad cow">
        </div> 
        <div id="content"></div>
            <!--Define button function-->
            <button @click="handleButtonClick">Get Rich</button>
        </div>  

        <div id="flex">
    <div id="sidebar" class="container">
      Sidebar
      <div class="input-group">
        <input type="text" v-model="newText" placeholder="Enter Text">
        <button @click="addTextToMain">Add More Text</button>
      </div>
      <div class="input-group">
        <input type="text" v-model="mainColor" placeholder="Enter Color Value">
        <button @click="applyColor">Change Color</button>
      </div>
    </div>

    <div id="main" class="container" :style="{ backgroundColor: mainColor }">
      <p v-html="mainContent"></p>
    </div>
  </div>


</template>

<!-- style is where the css code goes -->
<style scoped>
html {
    background-color: #f0f0f0;
    color: #333;
    font-family: 'Arial', sans-serif;
}

body {
    margin: 0;
    padding: 20px;
}

.container {
    border: 1px solid #ddd;
    border-radius: 8px;
    padding: 15px;
    margin-bottom: 20px;
    background-color: white;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

#navbar {
    display: flex;
    align-items: center;
    justify-content: space-between;
    height: 75px;
    border-bottom: 2px solid #e0e0e0;
}

#flex {
    display: flex;
    gap: 20px;
}

#sidebar {
  width: 30%;
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.input-group {
  display: flex;
  gap: 10px;
  align-items: center;
}

.input-group input {
  flex-grow: 1;
}

#main {
    width: 70%;
}

#title {
    font-size: 24px;
    font-weight: bold;
    color: #4a4a4a;
}

#logo {
    width: 30%;
    text-align: right;
}

img {
    max-height: 60px;
    width: auto;
}

button {
    padding: 10px 15px;
    background-color: #4caf50;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    font-size: 16px;
}

button:hover {
    background-color: #45a049;
}

button:focus {
    outline: none;
}

</style>
