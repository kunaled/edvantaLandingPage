<script setup>
import { ref } from 'vue';
import { ArrowRight } from 'lucide-vue-next';

// State to track which button is active
const activeButtonId = ref(null);

// Data for dynamic content
const items = ref([
  {
    id: 'item1',
    title: 'How a Digital Marketing Agency Can Boost Your Business',
    content: 'We are the top digital marketing agency for branding corp. We offer a full range of services including...',
    readTime: '5 min read',
  },
  {
    id: 'item2',
    title: 'The Latest Trends and Strategies with a Digital Marketing Agency',
    content: 'Working with this digital marketing agency has been a true partnership. They have taken the time to understand our business and industry',
    readTime: '5 min read',
  },
  {
    id: 'item3',
    title: 'Maximizing ROI with the Expertise of a Digital Marketing Agency',
    content: 'What sets this digital marketing agency apart is their commitment to transparency and collaboration. They keep us informed every step of the way,',
    readTime: '5 min read',
  }
]);

// Toggle function for the arrow button
function toggleArrowButton(buttonId) {
  activeButtonId.value = activeButtonId.value === buttonId ? null : buttonId;
}
</script>

<template>
  <div class="main-container">
    <div class="upper-div">
      <h1 class="main-title">
        Digital Marketing & SEO <br />Service That Grow Traffic & Increase
        Revenue
      </h1>
      <div class="intro-text">
        <p>
          We are the top digital marketing agency for branding corp. We offer a
          full range of services to help clients improve their search engine
          rankings and drive more traffic to their websites.
        </p>
        <button class="seemore-btn">See more</button>
      </div>
    </div>
    <div class="lower-div">
      <div v-for="item in items" :key="item.id" class="item">
        <p class="para" style="color: rgb(181, 180, 178); right:1%; position:absolute; top:2%">{{ item.readTime }}</p>
        <h1 class="item-title">{{ item.title }}</h1>
        <div class="item-div">
          <p>{{ item.content }}</p>
          <button @click="toggleArrowButton(item.id)" :class="{ 'active': activeButtonId === item.id }"><ArrowRight/></button>
        </div>
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

.upper-div {
  display: flex;
  flex-direction: row;
  align-items: flex-start;
  padding-left: 30px;
}

.main-title {
  font-weight: bold;
  font-size: 47px;
  line-height: 1.2;
}

.intro-text {
  padding-left: 100px;
}

.intro-text p {
  color: rgb(181, 180, 178);
  padding-top: 10px;
}

.seemore-btn {
  border: 1px solid #000;
  background-color: transparent;
  width: 150px;
  height: 40px;
  border-radius: 25px;
  margin-top: 40px;
  cursor: pointer;
}

.lower-div {
  display: flex;
  flex-wrap: wrap;
  gap: 20px; /* Increased space between items for better spacing */
  padding-top: 50px;
}

.item {
  position: relative;
  background-color: white;
  flex: 1 1 calc(33% - 20px); /* Responsive width, 3 items per row */
  padding: 20px;
  box-sizing: border-box;
  border-radius: 20px;
  display: flex;
  flex-direction: column;
  height: 20vw;
}

.item-title {
  font-weight: bold;
  font-size: 30px;
  margin: 0;
}

.item-div {
  display: flex;
  align-items: center;
  gap: 10px;
  margin-top: auto;
}

.item-div p {
  margin: 0;
  text-align: left;
  flex: 1;
  color: rgb(181, 180, 178);
}

button {
  border: 2px solid #000;
  background-color: transparent;
  border-radius: 25px;
  color: #000;
  cursor: pointer;
  padding: 10px 20px;
  display: flex;
  align-items: center;
  justify-content: center;
}

button.active {
  background-color: #000;
  color: #fff;
}

button.active svg {
  color: #fff;
}

/* Responsive Styles */
@media (max-width: 1200px) {
  .lower-div {
    flex-direction: column;
    align-items: center;
  }

  .item {
    flex: 1 1 100%; /* Full width on smaller screens */
    margin-left: 0; /* Remove left margin */
  }
}

@media (max-width: 768px) {
  .main-title {
    font-size: 36px;
  }
  .intro-text {
    padding-left: 20px; /* Reduced padding for smaller screens */
  }

  .item-title {
    font-size: 24px;
  }

  .seemore-btn {
    width: 120px;
    height: 35px;
  }
}
</style>
