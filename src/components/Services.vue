<template>
  <div class="main-container">
    <div class="up">
      <h1>We have been building flexible learning ecosystems over the last 20 years for several organisations, institutions & industries.</h1>
      <p>We are a passionate team of digital marketing enthusiasts dedicated to helping businesses succeed in the digital world. With years of experience and a deep understanding of the ever-evolving online landscape, we stay at the forefront of industry trends and technologies.</p>
    </div>
    <div class="image-container">
      <img src="../../public/firstlogo.png" alt="logo1">
      <img src="../../public/logo2.png" alt="logo2">
    </div>
  </div>
</template>

<style scoped>
.main-container {
  font-family: "Plus Jakarta Sans", sans-serif;
  padding: 40px;
  background-color: rgb(247, 247, 245);

}

.up {
  display: flex;
  flex-direction: row; /* Ensures heading and paragraph are side by side */
  align-items: flex-start; /* Aligns items at the start of the container */
  justify-content: space-between; /* Distributes space between heading and paragraph */
  text-align: left; /* Aligns text to the left */
  margin: 30px;
  margin-left: 75px;
  margin-right: 75px;
}

.up h1 {
  font-size: 2.5rem; /* Responsive font size */
  font-weight: bold;
  margin: 0; /* Removes default margin */
}

.up p {
  color: rgb(181, 180, 178);
  margin-top: 1%; /* Removes default margin */
  max-width: 500px; /* Max width for readability */
}

.image-container {
  display: flex;
  justify-content: center;
  gap: 40px; /* Spacing between images */
  padding-top: 40px;
}

.image-container img {
  max-width: 100%; /* Ensures images scale down if needed */
  height: auto; /* Maintains aspect ratio */
}

/* Media Queries */
@media (max-width: 1000px) {
  .up {
    flex-direction: column; /* Stacks heading and paragraph vertically on smaller screens */
    align-items: center; /* Centers items */
    text-align: center; /* Centers text */
  }

  .up h1 {
    font-size: 2rem; /* Smaller font size on mobile */
    margin-bottom: 10px; /* Adds space below heading */
  }

  .up p {
    font-size: 0.9rem; /* Smaller font size on mobile */
    padding: 0 10px; /* Adds padding for better readability */
  }

  .image-container {
    flex-direction: column; /* Stacks images vertically on mobile */
    gap: 20px; /* Adjusted gap for smaller screens */
    padding-top: 20px;
    margin:auto;
  }

  .image-container img {
    width: 80%; /* Scales images to fit smaller screens */
  }
}

@media (max-width: 480px) {
  .up h1 {
    font-size: 1.5rem; /* Smaller font size on very small screens */
  }

  .up p {
    font-size: 0.8rem; /* Further reduce font size */
    padding: 0 5px; /* Less padding on very small screens */
  }

  .image-container img {
    width: 90%; /* Larger scale for images on very small screens */
  }
}
</style>
