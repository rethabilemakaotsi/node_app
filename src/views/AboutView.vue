<template>
    <div class="About">
      <div class="row">
        <div class="col-1"></div>
        <div class="col-1 display-1 mb-5">
          About Us
        </div>
        <div class="container-lg col-5 p-5"> 
          <p class="Abt-text display-6">Welcome to our poetry emporium,</p>
          <p>Where the timeless words of renowned poets find a home. At our virtual shelves, we    proudly showcase the works of some of history's most influential wordsmiths, each poem a testament to the human experience, capturing emotions, stories, and perspectives that transcend time and culture.
          </p>
          <span class="">
In our digital sanctuary, verses dance and sing,
Echoes of passion, pain, and everything between.
From Sylvia Plath to Dickinson's quiet grace,
Each stanza a window to the soul's deepest space.

Come wander through our virtual halls, where poets roam,
Where the timeless words of renowned poets find a home.</span>
          
          <!-- <p>Where the timeless words of renowned poets find a home. At our virtual shelves, we    proudly showcase the works of some of history's most influential wordsmiths, each poem a testament to the human experience, capturing emotions, stories, and perspectives that transcend time and culture.</p> -->
        </div>
        <div class="col-3">
        </div>
        <div class="container">
          <img src="https://i.ibb.co/RgRhmR9/reading.jpg" height="670">
        </div>
      </div>
    </div>
    <!-- </div>
    <h1 class="AboutUs">About Us </h1>
    <div> -->
     
   </template>
   
   <script>
   export default {
     name: 'NavBarComp'
   }
   </script>
   
   <style scoped>
   .About{
    background-color: #918e8e;
   }
   .display-1{
    position: absolute;
    margin-left: 5rem;
    transform: rotate(-90deg);
    margin-top: 18rem;
   }
   .container-lg{
    background-color: #885B19;
    border-radius: 45px;
    margin-right: 32rem;
    
    /* margin-top: 10rem; */
   }
   .container {
    margin-top: -47rem;
    margin-left: 30rem;
   }
   @media screen and (max-width: 567px) {
    .display-1{
      transform: rotate(0deg);
      margin-top: 1rem;
    }
   }
   .col-5{
    text-align: center;
    margin-top: 5rem;
    margin-bottom: 10.3rem;
    color: white;
/* width: 150px; */
   }
   .col-3{
    border-radius: 10%;
   }
   /* .navbar {
     box-shadow: 0 2px 4px rgba(28, 11, 212, 0.1);
   }
   
   .navbar-dark .navbar-nav .nav-link {
     color: #fff;
   }
   
   .navbar-dark .navbar-nav .nav-link:hover {
     color: red;
     background-color:rgba(94, 3, 119, 0.1);
   } */
   </style>
   