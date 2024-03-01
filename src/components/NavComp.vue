<template>
  <nav class="navbar navbar-expand-lg justify-content-start">
    <div class="container-fluid">
      <img src="https://i.ibb.co/Q8LMD7F/logo.png" id="logo">
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent"
        aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav m-auto mb-2 mb-lg-0">
          <li class="nav-item">
            <router-link to="/" class="nav-link">Home</router-link>
          </li>
          <li class="nav-item">
            <router-link to="/about" class="nav-link">About</router-link>
          </li>
          <li class="nav-item">
            <router-link to="/products" class="nav-link">Products</router-link>
          </li>
          <li class="nav-item">
            <router-link to="/admin" class="nav-link">Admin</router-link>
          </li>
          <li class="nav-item">
            <router-link to="/contact" class="nav-link">Contact us</router-link>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>
<script>
export default {
  components: {}
};
</script>
<style scoped>
nav {
  background-color: #918E8E;
  padding: 10px 0;
}
#logo {
  width: 100px; /* Adjust logo width as needed */
  margin-right: 20px; /* Add margin to separate logo from navbar items */
}
.navbar-nav .nav-item {
  margin: 0 10px; /* Adjust margin between navbar items */
}
.navbar-nav .nav-link {
  color: #885B19; /* Set text color for navbar links */
  font-size: 18px; /* Adjust font size for navbar links */
  font-weight: bold;
  text-transform: uppercase;/* Add font weight to navbar links */
}
.navbar-toggler {
  border: none; /* Remove border from navbar toggler */
}
.navbar-toggler:focus {
  outline: none; /* Remove focus outline from navbar toggler */
}
.navbar-toggler-icon {
  background-color: #fff; /* Set background color for navbar toggler icon */
}
</style>