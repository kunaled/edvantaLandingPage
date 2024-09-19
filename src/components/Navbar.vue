<script setup>
import { ref, computed } from "vue";
import { ChevronDown, Bell } from 'lucide-vue-next';

const isOpen = ref(false);
const toggleMenu = () => {
  isOpen.value = !isOpen.value;
};

// Computed property to check if the screen width is large
const isLargeScreen = computed(() => window.innerWidth > 768);

// Watch for window resize to update the isOpen state
window.addEventListener('resize', () => {
  if (isLargeScreen.value) {
    isOpen.value = true; // Always open on large screens
  } else {
    isOpen.value = false; // Collapse on smaller screens
  }
});

// Set initial state
if (isLargeScreen.value) {
  isOpen.value = true;
}
</script>


<template>
  <div class="main-container">
    <nav class="navbar" style="display: relative;">
      <div class="logo">
        <img src="../../public/Group.png" alt="Logo">
        <h2>edvanta</h2>
        
      </div>

       <div class="hamburger-container" @click="toggleMenu">
    <div :class="['bar', { 'open': isOpen }]"></div>
    <div :class="['bar', { 'open': isOpen }]"></div>
    <div :class="['bar', { 'open': isOpen }]"></div>
  </div>
  <nav v-if="isOpen" class="dropdown-menu" >
      <ul class="nav-links">
        <li><a href="#">Service <ChevronDown /></a></li>
        <li><a href="#">Agency <ChevronDown /></a></li>
        <li><a href="#">Case Study<ChevronDown /></a></li>
        <li><a href="#">Resources<ChevronDown /></a></li>
        <li><a href="#">Contact<ChevronDown /></a></li>
      </ul >
      </nav >
      <div class="buttons" id="hidebtn" >
        <button class="get-started">Get Started</button>
       <div class="icon-container">
    <Bell />
  </div>
      </div>
    </nav>

    <div class="hero">
      <div class="left">
        <h1 style="padding-top:30px">Stay ahead of the curve<br> with our forward-thinking</h1>
        <p style="padding-top:50px">An award-winning SEO agency with disciplines in digital marketing, design, and <br>website development. Focused on understanding you.</p>
        <div class="hero-buttons">
          <button class="btn schedule-call">Schedule Call</button>
          <button class="btn view-case-study">View Case Study</button>
        </div>

    <div class="trusted-logos">
      <h3 style="font-weight:bold;">Trusted by the world's <br>biggest brand</h3>
      <img style="width: 70px;" src="../../public/afterpay.png" alt="Afterpay">
      <img src="../../public/basecamp.png" alt="Basecamp">
      <img src="../../public/maze.png" alt="Maze">
    </div>
      </div>
      <div class="right">
      <img src="../../public/hero1.png" alt="">
      </div>
    </div>

  </div>
</template>
<style scoped>
.main-container {
  font-family: "Plus Jakarta Sans", sans-serif;
  padding: 40px;
  background-color: rgb(247, 247, 245);
}

.logo {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 10px;
}

.logo h2 {
  font-weight: bold;
  font-size: 1.5rem; /* Responsive font size */
}

.icon-container {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  background-color: black;
  border: 2px solid black;
  border-radius: 50%;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.icon-container svg {
  width: 24px;
  height: 24px;
  color: white;
}

.get-started {
  border: 1px solid #000;
  background-color: transparent;
  width: 150px;
  height: 40px;
  border-radius: 15px;
}

.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap; /* Allows items to wrap on small screens */
}

.nav-links {
  display: flex;
  list-style-type: none;
  gap: 20px;
}

.nav-links a {
  display: flex;
  text-decoration: none;
  color: #000;
  font-weight: bold;
}

.buttons {
  display: flex;
  align-items: center;
  gap: 10px;
}

.hero {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap; /* Allows hero content to stack on small screens */
  padding: 80px;
}

.hero .left {
  flex: 1;
}

.hero .right {
  flex: 1;
  display: flex;
  justify-content: center;
}

.hero .left h1 {
  font-size: 2.5rem;
  font-weight: bold;
}

.hero .left p {
  font-size: 1rem;
  margin: 20px 0;
  color: rgb(181, 180, 178);
}

.hero-buttons {
  display: flex;
  gap: 15px;
  padding-top: 50px;
}

.btn {
  padding: 12px 24px;
  border: none;
  cursor: pointer;
  font-size: 1rem;
}

.schedule-call {
  background-color: #000;
  color: #fff;
  width: 250px;
  min-width: 100px;
  border-radius: 25px;
}

.view-case-study {
  background-color: transparent;
  color: #000;
  text-decoration: underline;
  text-decoration-color: rgb(181, 180, 178);
}


/* Adjusted responsive styles for the button */
@media (max-width: 768px) {
  .view-case-study {
    font-size: 0.9rem; /* Adjust font size for medium screens */
         margin: auto;
  width: 50%;
  }
  .schedule-call{
      margin: auto;
      width: 50%;
  }
}

@media (max-width: 480px) {
  .view-case-study {
    font-size: 0.8rem; /* Smaller font size for small screens */
    width: 150px;
    margin-left: 50px;
     /* Adjust button width */
  }
}
  .view-case-study {
    font-size: 0.9rem; /* Adjust font size for medium screens */
         margin: auto;
  width: 50%;
  }
  .schedule-call{
      margin: auto;
      width: 50%;
  }
.trusted-logos {
  display: flex;
  flex-wrap: wrap; /* Allows logos to wrap on small screens */
  gap: 30px;
  padding-top: 100px; /* Adjust spacing as needed */
}

.trusted-logos img {
  width: 80px; /* Adjusted size for responsiveness */
  opacity: 0.7;
  height: 35px;
}

/* Media Queries */
@media (max-width: 1200px) {
  .trusted-logos {
    padding-top: 50px;
  }
    .view-case-study {
    font-size: 0.9rem; /* Adjust font size for medium screens */
         margin: auto;
  width: 50%;
  }
  .schedule-call{
      margin: auto;
      width: 50%;
  }
}

@media (max-width: 788px) {
  .nav-links {
    flex-direction: column;
    align-items: left;

    gap: 10px;
    
  }
  #hidebtn{
    display: absolute;
  }
  .hamburger-container {
  display: flex;
  flex-direction: column;
  cursor: pointer;
  width: 40px;
  height: 30px;
  justify-content: space-around;
  position:relative;
  z-index: 100;
}

.bar {
  height: 4px;
  background-color: #333;
  transition: all 0.3s ease;
}

.bar.open:nth-child(1) {
  transform: rotate(45deg) translate(5px, 5px);
}

.bar.open:nth-child(2) {
  opacity: 0; /* Hide the middle bar */
}

.bar.open:nth-child(3) {
  transform: rotate(-45deg) translate(5px, -5px);
}

.dropdown-menu {
  position: absolute;
  top: 80px; /* Adjust based on your layout */
  right: 0;  /* Aligns the menu to the right */
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
  width: auto; /* Let it auto adjust width based on content */
  z-index: 99;
  display: flex;
  justify-content: flex-end; /* Aligns the content to the right */
  background-color: rgb(247, 247, 245);
  border-radius: 14px;
}


.dropdown-menu ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

.dropdown-menu li {
  padding: 10px 20px;
}

.dropdown-menu a {
  text-decoration: none;
  color: #333;
}

.dropdown-menu li:hover {
  background-color: #f0f0f0;
}

  .buttons {
    flex-direction: row;
    gap: 10px;
  }

  .hero {
    flex-direction: column;
    padding: 20px;
  }

  .hero .left h1 {
    font-size: 2rem;
  }

  .hero .left p {
    font-size: 0.9rem;
  }

  .hero-buttons {
    flex-direction: column;
    gap: 10px;
  }

  .trusted-logos {
    flex-direction: column;
    align-items: center;
    gap: 20px;
  }
}

@media (max-width: 480px) {
  .logo h2 {
    font-size: 1.2rem;
  }

  .icon-container {
    width: 30px;
    height: 30px;
  }

  .icon-container svg {
    width: 20px;
    height: 20px;
  }

  .get-started {
    width: 120px;
    height: 35px;
  }

  .btn {
    padding: 10px 20px;
    font-size: 0.9rem;
  }

  .trusted-logos img {
    width: 50px;
  }
}
</style>
