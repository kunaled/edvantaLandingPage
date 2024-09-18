<script setup>
import { ArrowLeft, ArrowRight } from 'lucide-vue-next';
</script>

<template>
  <div class="main-container">
    <div class="heading">
      <h1>“ They thoroughly analyze our industry and target audience, allowing them to develop customized campaigns that effectively reach and engage our customers. Their creative ideas and cutting-edge techniques have helped us stay ahead of the competition.”</h1>
    </div>
    <div class="bottom-area">
      <div class="profile">
        <img src="../../public/Ellipse.png" alt="ellipse" class="profile-image">
        <div class="profile-text">
          <h1>Michael Kaizer</h1>
          <p>CEO of Basecamp Corp</p>
        </div>
      </div>
      <div class="navigation">
        <div class="icon">
          <ArrowLeft />
        </div>
        <p><span class="number">01</span>/05</p>
        <div class="icon">
          <ArrowRight />
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.main-container {
  font-family: "Plus Jakarta Sans", sans-serif;
  padding: 20px;
  padding-left: 40px;
  background-color: rgb(247, 247, 245);

}

.heading {
  font-size: 4vw;
  font-weight: bold;
  margin-bottom: 20px;
}

.bottom-area {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-top: 20px;
}

.profile {
  display: flex;
  align-items: center;
}

.profile-image {
  width: 50px;
  height: 50px;
  margin-right: 10px;
}

.profile-text {
  text-align: left;
}

.profile-text h1 {
  font-weight: bold;
  font-size: 1.2rem;
  margin: 0;
}

.profile-text p {
  color: rgb(181, 180, 178);
  font-size: 1rem;
  margin: 0;
}

.navigation {
  display: flex;
  align-items: center;
  gap: 15px;
}

.icon {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 35px;
  height: 35px;
  background-color: black;
  color: white;
  border-radius: 50%;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.number {
  text-decoration: underline;
}

@media (min-width: 768px) {
  .heading {
    font-size: 3rem;
  }

  .profile-text h1 {
    font-size: 1.5rem;
  }

  .profile-text p {
    font-size: 1.2rem;
  }

  .navigation {
    gap: 20px;
  }

  .icon {
    width: 40px;
    height: 40px;
  }
}

@media (min-width: 1024px) {
  .main-container {
    padding: 40px;
    padding-left: 80px;
  }

  .heading {
    font-size: 48px;
  }

  .profile-text h1 {
    font-size: 1.8rem;
  }

  .profile-text p {
    font-size: 1.4rem;
  }

  .navigation {
    gap: 30px;
  }

  .icon {
    width: 50px;
    height: 50px;
  }
}
</style>
