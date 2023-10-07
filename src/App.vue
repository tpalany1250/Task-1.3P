<script setup>
import { RouterLink, RouterView } from 'vue-router'
import FooterComponent from './components/FooterComponent.vue';
</script>




<!-- Fix footer -->
<template>

  <div class="nav-container">
    <input type="checkbox" id="menu-toggle" class="menu-toggle">
    <label for="menu-toggle" class="dropdown-btn">Menu</label>
    
    <div class="links-container">
      <br>
      <RouterLink class="nav-link" to="/">Home</RouterLink>
      <RouterLink class="nav-link" to="/about">About</RouterLink>
      <RouterLink class="nav-link" to="/contact">Contact Us</RouterLink>
    </div>

  </div>

  <br>

  <div class="content-container">
    <div class="content-text">
    <br><br>
      <h2>Content Summary</h2>
      <br>
      <ul>Home</ul>
      <p>This section display the projects I have been contributing towards during the semester</p>

      <ul>About</ul>
      <p>This section represents what I am all about and why I choose the field of IT</p>
      
      <ul>Contact</ul>
      <p>This section is a place where you can contact me or provide me with feedback</p>
    </div>
  </div>
  

  <div class="page-container">
    <div class="content-wrapper">
      <!-- Your main content goes here -->

      <RouterView />
    </div>
    <footer class="amazing-footer">
      <!-- Your footer content as provided -->

  <FooterComponent/>
    </footer>
  </div>



</template>

<!-- 
<template>
  <div class="nav-container">
    <input type="checkbox" id="menu-toggle" class="menu-toggle">
    <label for="menu-toggle" class="dropdown-btn">Menu</label>
    <div class="links-container">
      <RouterLink class="nav-link" to="/">Home</RouterLink>
      <RouterLink class="nav-link" to="/about">About</RouterLink>
      <RouterLink class="nav-link" to="/contact">Contact Us</RouterLink>
    </div>
  </div>

  <RouterView />

  <FooterComponent/>
</template> -->

<style scoped>
/* Add this to your styles */
.page-container {
  display: flex;
  flex-direction: column;
  min-height: 100vh; /* This ensures the container takes at least the full height of the viewport */
}

/* .content-wrapper {
  flex: 1; /* This makes the content take up all available space, pushing the footer to the bottom
} */


.nav-container {
  /* display: flex; */
  text-align: center;
  /* background-color: #2c3e50; */
  padding: 20px 0;
  /* position: relative; */
  padding-bottom: -10px
  /* flex-wrap: wrap; */
}

.links-container {
  background-color: #2c3e50;
  padding: 10px 0;
  padding-bottom: 25px;
  /* flex: 1; */
}

.nav-link {
  text-decoration: none;
  color: #ecf0f1;
  padding: 10px 20px;
  margin: 0 10px;
  font-size: 1.1em;
  transition: background-color 0.3s, color 0.3s;
  border-radius: 4px;
}

.nav-link:hover {
  background-color: #34495e;
  color: #bdc3c7;
}

.router-link-active {
  color: #e74c3c;
  background-color: #e4dad9;
  border-radius: 4px;
}

/* Mobile styles */
.menu-toggle {
  display: none; /* hide the checkbox */
}

.dropdown-btn {
  display: none;
  background-color: #34495e;
  color: #ecf0f1;
  padding: 10px 20px;
}


.content-container {
  /* margin-left: 100px */
  display: flex;
  justify-content: flex-end;
  text-align: center;
}

.content-text ul {
  list-style: none; /* Remove bullet points */
    padding: 0; /* Remove default padding */
    margin: 25px;
    margin-left: 250px;
    margin-right: 250px;
    text-align: center;
    padding-top: 20px;
    border-top: 1px solid #ddd;;
}

.content-text p {
  margin-left: 130px;
  margin-right: 130px;
}

</style>