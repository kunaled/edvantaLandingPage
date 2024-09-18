<script setup>
import { ref } from 'vue';
import { Plus, Minus } from 'lucide-vue-next';

const questions = [
  {
    title: 'Why digital marketing is important for my business?',
    content: 'Digital marketing allows businesses to reach and engage with a wider audience, generate leads, drive website traffic, and increase brand visibility. It provides measurable results, allows for targeted marketing efforts, and enables businesses to adapt and optimize their strategies based on data and insights.'
  },
  {
    title: 'How can I measure the success of my digital marketing campaigns?',
    content: 'Success can be measured using various metrics such as website traffic, conversion rates, ROI, and engagement rates. Tools like Google Analytics and social media insights help track and analyze these metrics.'
  },
  {
    title: 'What are the key components of a digital marketing strategy?',
    content: 'A digital marketing strategy typically includes components like SEO, content marketing, social media marketing, email marketing, and paid advertising. Each component plays a role in reaching and engaging your target audience.'
  }
];

const activeIndex = ref(null);

const toggleContent = (index) => {
  activeIndex.value = activeIndex.value === index ? null : index;
};
</script>

<template>
  <div class="main-container">
    <div class="left-container">
      <h1>Digital Marketing FAQs</h1>
      <p>
        As a leading digital marketing agency, we are dedicated to providing comprehensive educational resources and answering frequently asked questions to help our clients.
      </p>
      <div class="hero-buttons">
        <button class="btn schedule-call">More Questions</button>
        <button class="view-case-study">Contact Us</button>
      </div>
    </div>
    <div class="right-container">
      
      <div v-for="(question, index) in questions" :key="index" class="header-content">
        <h4 @click="toggleContent(index)">{{ question.title }}</h4>
        <component :is="activeIndex === index ? Minus : Plus" @click="toggleContent(index)" />
        <transition name="fade">
          <div v-if="activeIndex === index" class="content">
            <p>{{ question.content }}</p>
          </div>
        </transition>
      </div>
    </div>
  </div>
</template>

<style scoped>
.main-container {
  font-family: "Plus Jakarta Sans", sans-serif;
  padding: 40px;
  display: flex;
  justify-content: space-between; /* Align left and right containers side by side */
  gap: 20px; /* Space between the containers */
  background-color: white;
  margin: 30px;
  border-radius: 30px;
}

.left-container {
  width: 35%;
  text-align: left;
  margin-left: 40px;
}

.left-container h1 {
  font-weight: bold;
  font-size: 2.5rem;
  margin-bottom: 10px;
}

.left-container p {
  color: rgb(181, 180, 178);
  font-size: 1rem;
}

.hero-buttons {
  display: flex;
  flex-direction: row;
  gap: 10px;
  margin-top: 20px;
}

.hero-buttons .btn {
  border: 1px solid #000;
  background-color: transparent;
  width: 40%;
  height: 40px;
  border-radius: 25px;
  text-align: center;
  padding: 0;
}

.view-case-study {
  background-color: transparent;
  color: #000;
  text-decoration: underline;
}

.right-container {
  width: 35%;
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.header-content {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  gap: 10px;
  cursor: pointer;
}

.header-content h4 {
  margin: 0;
  padding: 10px 0;
  border-bottom: 2px solid #333;
}

.content {
  padding: 10px;
  border-radius: 5px;
  color: rgb(181, 180, 178);

}

.fade-enter-active, .fade-leave-active {
  transition: opacity 0.5s;
}

.fade-enter, .fade-leave-to /* .fade-leave-active in <2.1.8 */ {
  opacity: 0;
}

/* Responsive Styles */
@media (max-width: 768px) {
  .main-container {
    flex-direction: column;
    padding-right: 100px;
  }

  .left-container, .right-container {
    width: 100%;
  }

  .hero-buttons {
    flex-direction: column;
  }

  .hero-buttons .btn {
    width: 100%;
  }

  .right-container h1 {
    font-size: 1.2rem;
  }
}

@media (min-width: 768px) and (max-width: 1024px) {
  .left-container h1 {
    font-size: 2rem;
  }

  .left-container p {
    font-size: 1.1rem;
  }

  .hero-buttons {
    gap: 15px;
  }

  .right-container h1 {
    font-size: 1.4rem;
  }
}

@media (min-width: 1024px) {
  .left-container h1 {
    font-size: 3rem;
  }

  .left-container p {
    font-size: 1.2rem;
  }

  .hero-buttons {
    gap: 20px;
  }

  .right-container h1 {
    font-size: 1.8rem;
  }
}
</style>
