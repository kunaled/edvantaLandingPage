<template>
  <div class="main-container">
    <div class="container">
      <div class="background-image">
        <div class="txtbtn">

        <div class="text-overlay">
          <h1>Making learning accessible engaging effective and always outcome driven.​
</h1>
        </div>
        <div class="button-container">
          <button class="btn">All work[20]</button>
          <button class="btn">UI/UX Design[10]</button>
          <button class="btn">Digital Marketing[5]</button>
          <button class="btn">Branding[5]</button>
        </div>
        </div>
        <div class="bottom-image">
          <img src="../../public/Circle1.png" alt="Bottom Image">
          <img src="../../public/Circle2.png" alt="Bottom Image">
          <img src="../../public/Circle2.png" alt="Bottom Image">
          <img src="../../public/Circle3.png" alt="Bottom Image">
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.main-container {
  font-family: "Plus Jakarta Sans", sans-serif;
  margin: 0;
  padding: 10px; /* Padding around the main container */
  box-sizing: border-box; /* Ensure padding is included in the total width/height */
  background-color: rgb(247, 247, 245);

}


.background-image {
  position: relative;
  border-radius: 25px;
  background-color: black;
  height: calc(100vh); /* Reduced height to account for top and bottom padding */
  width: calc(100vw - 30px); /* Reduced width to account for left and right padding */
  background-image: url('../../public/backgroundN.png');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  overflow: hidden;
  padding: 10px; /* Padding around the background image */
  box-sizing: border-box; /* Ensure padding is included in the total width/height */
}

.text-overlay {
  position: absolute;
  top: 8%;
  left: 50%;
  transform: translateX(-50%);
  width: 90%; /* Adjusted width for better alignment */
  text-align: center;
  font-size: 2rem; /* Responsive font size */
  color: white;
  font-weight: bold;
}

.button-container {
  position: absolute;
  top: 30%;
  width: 100%;
  left: 50%;
  transform: translate(-50%, -50%);
  display: flex;
  flex-wrap: wrap; /* Allow buttons to wrap */
  gap: 25px; /* Adjusted gap */
  justify-content: center; /* Center buttons horizontally */
}

.btn {
  color: white;
  cursor: pointer;
  transition: background-color 0.3s ease;
  border: 1px solid rgb(247, 234, 234);
  background-color: transparent;
  width: 180px; /* Adjusted width for responsiveness */
  height: 50px;
  font-weight: bold;
  border-radius: 25px;
  font-size: 1rem; /* Adjusted font size for buttons */
}

.btn:hover {
  background-color: #90ee90;
}

.btn:focus, .btn:active {
  background-color: #577907;
  outline: none;
}

.bottom-image {
  display: flex;
  position: absolute;
  bottom: 10%;
  gap: 12%; /* Gap between images */
  top: 40%;

  overflow: auto; /* Add scrollbars if content overflows */
  padding: 10px; 
  scrollbar-width: none;
}



/* Media Queries */
@media (max-width: 1024px) {
  .background-image {
    height: calc(70vh - 20px); /* Adjusted height */
    position: relative;
  }

  .text-overlay {
    position: absolute;
    font-size: 1.8rem; /* Smaller font size */
  }


  .txtbtn{
    display: flex;
    }
  .btn {
    width: 120px; /* Adjusted button width */
    font-size: 0.9rem; /* Smaller font size */
  }
}
.bottom-image {
  display: flex;
  position: absolute;
  bottom: 10%;
  gap: 17%; /* Gap between images */
  top: 40%;

  overflow: auto; /* Add scrollbars if content overflows */
  padding: 10px; 
  scrollbar-width: none;
}

@media (max-width: 700px) {

  .txtbtn{
    display: flex;
    }
  .text-overlay {
    font-size: 1rem; /* Smaller font size */
    width: 90%; /* Full width */
    top: 10%; /* Adjusted top position */
  }

  .button-container {
    flex-direction: row; /* Stack buttons vertically */
    align-content: center;
    gap: 10px; /* Gap between buttons */
    top: 45%; /* Adjusted top position */
  }

  .bottom-image {
    flex-direction: row;
    gap: 20px; /* Gap between images */
    overflow: auto;
    padding-top: 50px;
  }

  .bottom-image img {
    margin-top: 30%;
    bottom: 0%;
    height: 60%;
  }
}

@media (max-width: 480px) {

  .txtbtn{
    display: flex;
    }
  .text-overlay {
    padding-bottom: 20px;
    font-size: 1.2rem; /* Even smaller font size */
  }

  .btn {
    width: 80px; /* Smaller button width */
    font-size: 0.8rem; /* Smaller font size */
  }

}
</style>
