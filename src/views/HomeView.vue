<template>
  <div class="container-fluid" id="body">
    <div class="row">
      <h1 :class="{ 'slide-in': loaded, 'rotate-on-hover': hover }" class="love-ya-like-a-sister-regular" @mouseenter="hover = true" @mouseleave="hover = false">Poetry Emporium</h1>
    </div>
    <div>
      <p class="img"> <img src="https://i.ibb.co/NsWLZZ4/4rf-removebg-preview.png"></p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeView',
  data() {
    return {
      loaded: false,
      hover: false
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
#body {
  background-color: #918e8e;
  color: #885B19; /* Light cream color */
  height: 84.88vh;
  background: linear-gradient(-45deg, #918e8e, #2a2724, #918e8e, #2a2724);
	background-size: 400% 400%;
	animation: gradient 15s ease infinite;
	height: 100vh;
}

@keyframes gradient {
	0% {
		background-position: 0% 50%;
	}
	50% {
		background-position: 100% 50%;
	}
	100% {
		background-position: 0% 50%;
	}
}

.love-ya-like-a-sister-regular {
  font-family: "Love Ya Like A Sister", cursive;
  font-weight: 600px;
  font-size: 80px;
  font-style: normal;
  line-height: 100px;
  transition: transform 0.3s ease;
}

.slide-in {
  animation: slideIn 1s ease forwards;
}

@keyframes slideIn {
  from {
    transform: translateX(-100%);
    opacity: 0;
  }
  to {
    transform: translateX(0);
    opacity: 1;
  }
}

.rotate-on-hover:hover {
  transform: rotate(360deg);
}

@media screen and (max-width: 576px) {
  .love-ya-like-a-sister-regular {
    font-size: 40px;
    line-height: 60px;
  }
}
</style>
