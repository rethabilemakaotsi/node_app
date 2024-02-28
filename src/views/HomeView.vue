<template >
    <div class="container-fluid" id="body">
      <div class="row">
        <h1 class="love-ya-like-a-sister-regular">Poetry Emporium</h1>
      </div>
      <div>
        <p class="img"> <img src = "https://i.ibb.co/NsWLZZ4/4rf-removebg-preview.png"></p>
      </div>
    </div>
  </template>
  <script>



    export default {
    name: 'HomeView',
    components: {
 
    },
    data() {
      return {
        loaded: false
      };
    },
    mounted() {
      setTimeout(() => {
        this.loaded = true;
      }, 2000);
    }
  }
  </script>
  <style scoped>


#body{
    background-color:#918e8e ;
    color: #885B19;
    height:84.88vh
}
.love-ya-like-a-sister-regular {
  font-family: "Love Ya Like A Sister", cursive;
  font-weight: 600px;
  font-size: 80px;
  font-style: normal;
  line-height: 100px;
}




@media screen and (max-width: 576px) {
  .love-ya-like-a-sister-regular {
    font-size: 40px;
    line-height: 60px;
  }
}
</style>