<template>
  <div class="hello">
    <h1>P5 CIRCLES</h1>
    <div class="container border">
    <div class="d-flex justify-content-center" id="p5Canvas"></div>
  </div>
  </div>
</template>

<script>
import p5 from 'p5'
export default {
  name: 'P5Circles',
  props: {
    msg: String
  },
  mounted() {   
 const script = function (p5) {    
  var speed = 2;    
  var posX = 0;
  
  // NOTE: Set up is here   
  p5.setup = _ => {      
   p5.createCanvas(1200, 500); 
//  p5.colorMode(p5.HSB, p5.height, p5.height, p5.height/2);     
  // p5.ellipse(p5.width / 2, p5.height / 2, 500, 500);    
  }
  p5.draw = _ => { 
    // p5.background(0)
    variableEllipse(p5.mouseX, p5.mouseY, p5.pmouseX, p5.pmouseY);
  }

  function variableEllipse(x, y, px, py) {
  let speed = p5.abs(x - px) + p5.abs(y - py);
//   p5.stroke(speed);
//   let c=p5.color(getRandomInt(256),getRandomInt(256),getRandomInt(256))
//   p5.fill(c)
// p5.noStroke()
p5.fill(p5.mouseX/2, p5.mouseY, p5.height,getRandomInt(256))
  p5.ellipse(x, y, speed, speed);
}

function getRandomInt(max) {
  return Math.floor(Math.random() * max);
}

  

//   // NOTE: Draw is here
//   p5.draw = _ => {      
//    p5.background(0);
//    const degree = p5.frameCount * 3;      
//    const y = p5.sin(p5.radians(degree)) * 50;
    
//    p5.push();
//     p5.translate(0, p5.height / 2);
//     p5.ellipse(posX, y, 50, 50);
//    p5.pop();
//    posX += speed;
      
//    if (posX > p5.width || posX < 0) {    
//     speed *= -1;      
//    }
//   }  
 }   
 // NOTE: Use p5 as an instance mode
 const P5 = require('p5');
 new P5(script)
},
methods:{
//     variableEllipse(x, y, px, py) {
// console.log("variable")
//   let speed = p5.abs(x - px) + p5.abs(y - py);
//   p5.stroke(speed);
//   p5.ellipse(x, y, speed, speed);
// }
}
}


</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
