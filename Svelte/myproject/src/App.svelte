<script>
//myproject\images\Sanskrit-Sahitya-Kaumudi-025.jpg
//let imagePath = imagePath
import LeftColumn from "./LeftColumn.svelte";
import RightColumn from "./RightColumn.svelte";

</script>

<main>
  <div class="topnav">
    <a class="home" href="#home">Home</a>
    <a href="#textract">Textract</a>
    <a href="#contact">Login</a>
  </div>
	<div class="flex-container">
    <LeftColumn/>
    <RightColumn />
    </div>
</main>

<style>
  .flex-container  {
  display: flex;
  flex-direction:row;

}
   .topnav {
  background-color: #333;
  overflow: hidden;
}

/* Style the links inside the navigation bar */
.topnav a {
  float: left;
  color: #f2f2f2;
  text-align: center;
  padding: 12px;
  text-decoration: none;
  font-size: 17px;
  width: 33.33%;
}

/* Change the color of links on hover */
.topnav a:hover {
  background-color: #ddd;
  color: black;
}

/* Add a color to the active/current link */


* {
  box-sizing: border-box;
}

.column {
  flex: 60%;
  padding: 10px;
  background-color:#e6f3ff;
  flex-wrap: wrap;
  height: calc(100vh);

}

#image {
   width: 90%;
   height: 80%;

}

#text {
  width: 75%;
  height: 80%;
}

.button {
    /* Center the content */
    align-items: center;
    display: flex;
    justify-content: center;

    /* Spacing */
    padding: 8px;
}

.button__arrow {
    /* Transparent background */
    background-color: transparent;

    /* Size */
    height: 15px;
    width: 15px;
}

.button__arrow--right {
    /* Edges */
    border-right: 1px solid rgba(0, 0, 0, 0.3);
    border-top: 1px solid rgba(0, 0, 0, 0.3);
    transform: translateX(-25%) rotate(45deg);
}


.button__arrow--left {
    /* Edges */
    border-bottom: 1px solid rgba(0, 0, 0, 0.3);
    border-left: 1px solid rgba(0, 0, 0, 0.3);
    transform: translateX(25%) rotate(45deg);
}

#try {
  font-size: 20px;
  font-family: monospace;
}

</style>