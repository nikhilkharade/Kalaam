<template>
    <div>
      <div id="header">
<div id="LogoandTitle">
<!--<router-link  to="/" ><img id="KalamLogo" src="../src/assets/LogoBlack.png" alt=""></router-link> -->
<router-link id="Kalaam" to="/" >Kalaam</router-link> 
</div>
  <button @click="toggleMenu()" id="stackMenuIcon" >☰</button> 

<ul id="headerlist">
   <li><router-link to="/Practise">Practice</router-link> </li>
 <li><router-link to="/Documentation">Documentation</router-link> </li>
  <li><router-link to="/Examples">Examples</router-link> </li>
   <li><router-link to="/Support">Support</router-link> </li>
    <li><router-link to="/About">About</router-link> </li>
   
   
</ul>
<transition name="slide-fade">

<ul v-if="showMenu==true" id="headerlistMobile">
 <div @click="toggleMenu()" ><li><router-link  to="/Practise">Practice</router-link> </li></div>  
 <div @click="toggleMenu()"><li><router-link to="/Documentation">Documentation</router-link> </li></div>  
 <div @click="toggleMenu()"> <li><router-link to="/Examples">Examples</router-link> </li></div>  
  <div @click="toggleMenu()"> <li><router-link to="/Support">Support</router-link> </li></div>  
   <div @click="toggleMenu()"> <li><router-link to="/About">About</router-link> </li></div>  
   
   
</ul>

</transition>

   </div>
   <div id="footer">
  <p style=" color: white">Released Under the MIT Licence</p>
  <p style="color: #ffeb00"><a style="text-decoration:none;">Created By Swanand Kadam</a></p>
</div>


    <router-view/>

  </div>
</template>


<script>
export default {
  name:'Header',

  data() {
    return {
      showMenu:false
    }
  },

  methods: {
    toggleMenu:function()
{

console.log('this: ', this.showMenu);
if(this.showMenu==false)

{
this.showMenu=true


}

else if(this.showMenu==true)
{
this.showMenu=false


}


}
  },


}
</script>

<style >


#Kalaam{

  float: left;
    text-decoration: none;
    margin-left: 2%;
    font-size: 163%;
    color: black;
}

#LogoandTitle{

position: absolute;
    display: block;
    width: 65%;


}



#header{

display: inline-block;
width: 100%;
background-color: white;
    height: 48px;
    position: relative;
    z-index: 20;
    padding-top: 1%;


}

#headerlistMobile{

  display: none 
  }

#headerlist{

      list-style-type: none;
    margin: 0;
    padding: 0;
    position: absolute;
    right: 3%;
    
    line-height: 40px;

}

#headerlist li{

      display: inline-block;
    margin: 0 2em;
    font-size: 110%;

}
#headerlist a{

  text-decoration: none;
   cursor:pointer; 
   color: #2c3e50;
}

#headerlist a:hover{

 
   color: rgb(52, 204, 218)
}

#footer{
display: none;
    background-color: #fff;
    /* height: 40px; */
    position: absolute;
    bottom: 0;
    width: 100%;
    background-color: #2f3c44;
    left: 0;
}
#stackMenuIcon
{


  display: none
}

#KalamLogo
{

      width: 4.5%;
    float: left;
    margin-left: 2.4%;
    margin-top: -0.2%;
}
.slide-fade-enter-active {
  transition: all .3s ease;
}
.slide-fade-leave-active {
  transition: all .3s ease cubic-bezier(1.0, 0.5, 0.8, 1.0);
}
.slide-fade-enter, .slide-fade-leave-to
/* .slide-fade-leave-active below version 2.1.8 */ {
  transform: translateY(10px);
  opacity: 0;
}

/* Smartphones (portrait) ----------- */
@media only screen
and (max-width : 480px) {
#headerlist{


  display: none
}
#stackMenuIcon
{


  display:block;
  float: right;
  font-size: 150%;
  border: none;
    background: white;
    color: black;
}

#Kalaam{

  float: left;
    text-decoration: none;
    margin-left: 4%;
    font-size: 163%;
    margin-top: 1%;
    color: black;
}

#LogoandTitle{

position: absolute;
    display: block;
    width: 65%;


}
#KalamLogo{

  width: 18.5%;
   
}

#headerlistMobile{

       display: inline-grid;
    position: absolute;
    left: 0%;
    width: 100%;
    background-color: #f3e78b;
    line-height: 40px;
    top: 86%;
    padding: 0%;
    
}


#headerlistMobile li{

      display: inline-block;
    font-size: 120%;
    margin-top: 1%

}
#headerlistMobile a{

  text-decoration: none;
   cursor:pointer; 
   color: rgb(12, 12, 12)
}

#headerlistMobile a:hover{

 
   color: rgb(214, 200, 0)
}
::-webkit-input-placeholder {
text-align: center;
vertical-align: middle;

line-height: 500px;}

:-moz-placeholder { /* Firefox 18- */
text-align: center;
vertical-align: middle;

line-height: 500px;}

::-moz-placeholder {  /* Firefox 19+ */
text-align: center;
vertical-align: middle;

line-height: 500px;}

:-ms-input-placeholder {  
text-align: center;
vertical-align: middle;

line-height: 500px;}

}

@media only screen
and (min-width : 768px)
and (max-width : 1024px) {



#headerlist li{

margin-left: 0%
}

}

</style>
