<template>
  <div id="bo">
  <body class="bg-body">
    <div class="row con-bg">
      <div class="col-md-6">
        <div class="map-container">
          <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d13242.314214447726!2d18.442668354896814!3d-33.92624486651537!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x1dcc5da25b1b83cb%3A0x9528ebc70c50cb86!2sWoodstock%2C%20Cape%20Town!5e0!3m2!1sen!2sza!4v1709189845138!5m2!1sen!2sza" width="400" height="300" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
          <div class="map-info">
            <h3>Location</h3>
            <p class="location"><img src="https://i.ibb.co/smp9Sxs/location.png" class="small-image">28 Blue Cakes St, Woodstock, Cape Town</p>
            <h3>Contact Details</h3>
            <p class="landline"><img src="https://i.ibb.co/McGLXQY/landline.png" class="small-image"> 021 4300 882</p>
            <p class="Email"><img src="https://i.ibb.co/FKqgRhN/arroba.png" class="small-image"> Poetryemporium@gmail.com</p>
          </div>
        </div>
      </div>
      <div class="col-md-6">
        <div class="contact-container">
          <div class="form-container">
            <h4>Get in Touch</h4>
            <form action="https://formspree.io/f/xgegvewy" method="POST" class="float start">
              <div class="form-row">
                <label for="name">Name</label>
                <input name="name" id="name" type="text" required>
              </div>
              <div class="form-row">
                <label for="number">Contact Number</label>
                <input name="number" id="number" type="tel" required>
              </div>
              <div class="form-row">
                <label for="email">Your Email</label>
                <input name="email" id="email" type="email" required>
              </div>
              <div class="form-row">
                <label for="message">Message</label>
                <textarea name="message" id="message" rows="4" required></textarea>
              </div>
              <button class="btn" type="submit">Submit</button>
            </form>
          </div>
        </div>
      </div>
    </div>
  </body>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>

#bo{
  background-color: #6b00f6;
}
.bg-body {
  color: #090808;
}
.con-bg{
  background-color: #918e8e;
}

.contact-container {
  text-align: center;
  max-width: 800px;
  margin: auto;
}

h1 {
  font-family: 'Inter', sans-serif;
  color: #0f50dd;
  margin-bottom: 20px;
}

.form-container,
.map-container {
  max-width: 400px;
  margin: 20px auto;
  padding: 20px;
  border: 7px solid #885B19;
  border-radius: 5px;
  background-color: #f6fbf9;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

.form-container {
  margin-right: 15px;
}

.map-info {
  margin-top: 15px;
}

iframe {
  width: 100%;
  height: 300px;
}

form {
  display: flex;
  flex-direction: column;
}

.label {
  margin-bottom: 5px;
  font-weight: bold;
  color: #60ce0c;
}

input,
textarea {
  padding: 10px;
  border: 2px solid #885B19;
  border-radius: 3px;
  box-sizing: border-box;
  width: 100%;
  background-color: #616463;
}

button {
  background-color: #616463;
  color: #491988;
  padding: 10px;
  border: none;
  border-radius: 10px;
  cursor: pointer;
  font-weight: bold;
  transition: background-color 0.20s ease;
}

.btn:hover {
  background-color: #885B19;
}

/* Define the style for small images */
.small-image {
  max-width: 50px; /* Adjust the size as needed */
}
.contact-container {
  text-align: center;
  max-width: 800px;
  margin: auto;
  margin-top: 20px; /* Add margin at the top to separate from the map */
}
</style>
