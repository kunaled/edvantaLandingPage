<script setup>
import { Facebook, Twitter, Linkedin, Instagram, PhoneCall, Mail, MapPin } from 'lucide-vue-next';
</script>

<template>
  <footer class="footer">
    <div class="cta-section">
      <h2>Ready to work with us?</h2>
      <button class="cta-button" style="color:black">Get Started</button>
    </div>
    <div class="footer-content">
      <div class="footer-brand">
        <div class="logo">
          <img src="../../public/Group.png" alt="edvanta logo" class="brand-logo" />
          <h1>edvanta</h1>
        </div>
        <p style=" color: rgb(181, 180, 178);">
          We offer a comprehensive suite of digital marketing services that
          cover all aspects of our online presence. From SEO and social media
          marketing to content creation and PPC advertising, they have the
          expertise and resources to handle our diverse marketing needs.
        </p>
        <div class="social-icons">
          <a href="#"><Facebook/></a>
          <a href="#"><Twitter/></a>
          <a href="#"><Linkedin/></a>
          <a href="#"><Instagram/></a>
        </div>
      </div>
      <div class="footer-navigation">
        <h3>Navigation</h3>
        <ul>
          <li><a href="#">Service</a></li>
          <li><a href="#">Agency</a></li>
          <li><a href="#">Case Study</a></li>
          <li><a href="#">Resource</a></li>
          <li><a href="#">Contact</a></li>
        </ul>
      </div>
      <div class="footer-legal">
        <h3>Licence</h3>
        <ul>
          <li><a href="#">Privacy Policy</a></li>
          <li><a href="#">Copyright</a></li>
          <li><a href="#">Email Address</a></li>
        </ul>
      </div>
      <div class="footer-contact">
        <h3>Contact</h3>
        <p><PhoneCall /> (406) 555-0120</p>
        <p><Mail /> Hey@edvanta.com</p>
        <p><MapPin /> 2972 Westheimer Rd. Santa Ana, Illinois 85486</p>
      </div>
    </div>
  </footer>
</template>

<style scoped>

.footer {
  font-family: "Plus Jakarta Sans", sans-serif;
  padding: 40px;
  background-color: rgb(247, 247, 245);
}

.logo {
  display: flex;
  align-items: center;
}

h1 {
  font-weight: bold;
  margin-left: 10px;
}

ul {
  margin-top: 10px;
}

.cta-section {
  background-color: #000;
  color: #fff;
  padding: 30px;
  border-radius: 15px;
  margin-bottom: 30px;
  display: flex;
  flex-direction: row;
  align-items: center;
  text-align: center;
  background-image: url('../../public/imageback.png');
}

.cta-section h2 {
  margin: 20px;
  font-size: 4rem;
}
a {
 color: rgb(181, 180, 178);
}

p {
  display: flex;
  padding-top: 20px;
  align-items: center;
}

.cta-section {
  background-color: #000;
  color: #fff;
  padding: 30px;
  border-radius: 15px;
  margin-bottom: 30px;
  display: flex;
  flex-direction: row;
  justify-content: space-between; /* Updated */
  text-align: left;
  background-image: url('../../public/imageback.png');
}

.cta-section h2 {
  margin: 20px;
  font-size: 4rem;
  flex: 1; /* Ensures h2 takes up available space */
}

.cta-button {
  background-color: #fff;
  border: none;
  padding: 10px 20px;
  font-size: 1.2rem;
  cursor: pointer;
  border-radius: 25px;
  transition: background-color 0.3s;
  margin-left: 20px; /* Adjusted margin */
}

.cta-button:hover {
  background-color: #ccc;
}

.footer-content {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  gap: 30px;
}

h3 {
  font-weight: bold;
}

.footer-brand, .footer-navigation, .footer-legal, .footer-contact {
  flex: 1;
  min-width: 200px;
}
.footer-contact p {
  gap: 15px;
}
.footer-brand {
  max-width: 300px;
}

.footer-brand img {
  max-width: 100px;
}

.footer-brand p {
  margin: 15px 0;
  color: #333;
  font-size: 0.9rem;
}

.social-icons {
  display: flex;
  gap: 15px;
  margin-top: 15px;
}

.social-icons a {
  color: #333;
  font-size: 1.2rem;
}

.footer-navigation ul, .footer-legal ul {
  list-style: none;
  padding: 0;
}

.footer-navigation ul li, .footer-legal ul li {
  margin-bottom: 10px;
}

.footer-navigation ul li a, .footer-legal ul li a {
  color: #333;
  text-decoration: none;
  font-size: 0.9rem;
}

.footer-contact p {
  color: #333;
  font-size: 0.9rem;
  display: flex;
  align-items: center;
}

.footer-contact i {
  margin-right: 5px;
}

/* Responsive Styles */
@media (max-width: 768px) {
  .cta-section {
    padding: 20px;
  }

  .cta-section h2 {
    font-size: 1.5rem;
  }

  .cta-button {
    font-size: 1rem;
  }

  .footer-content {
    flex-direction: column;
    align-items: center;
    gap: 20px;
  }

  .footer-brand, .footer-navigation, .footer-legal,.footer-contact {
    max-width: 100%;
    text-align: center;
  
  }

  .footer-brand img {
    max-width: 80px;
  }

  .footer-navigation ul, .footer-legal ul {
    padding: 0;
  }
  .footer-contact p {
    text-align: left;
    
  }
}

@media (max-width: 480px) {
  .cta-section {
    padding: 15px;
  }

  .cta-section h2 {
    font-size: 1.25rem;
  }

  .cta-button {
    font-size: 0.9rem;
  }

  .footer-content {
    gap: 15px;
  }

  .footer-brand img {
    max-width: 60px;
  }

  .footer-contact p {
    font-size: 0.85rem;
  }
}
</style>
