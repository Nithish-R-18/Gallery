# Ex.08 Design of Interactive Image Gallery
# Date: 06.10.2025
# AIM:
To design a web application for an inteactive image gallery with minimum five images.

# DESIGN STEPS:
## Step 1:
Clone the github repository and create Django admin interface.

## Step 2:
Change settings.py file to allow request from all hosts.

## Step 3:
Use CSS for positioning and styling.

## Step 4:
Write JavaScript program for implementing interactivity.

## Step 5:
Validate the HTML and CSS code.

## Step 6:
Publish the website in the given URL.

# PROGRAM :
```
photo.html

<html>
<head>
  <title>Interactive Photo Gallery</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <h1>Interactive Photo Gallery</h1>

  <div class="gallery">
    <img src="image1.jpg" alt="Photo 1">
    <img src="image2.jpg" alt="Photo 2">
    <img src="image3.jpg" alt="Photo 3">
    <img src="image4.jpg" alt="Photo 4">
    <img src="image5.jpg" alt="Photo 5">
  </div>

  <!-- Lightbox -->
  <div class="lightbox" id="lightbox">
    <span class="close-btn" id="close">&times;</span>
    <img id="lightbox-img" src="" alt="">
  </div>

  <script src="script.js"></script>
</body>
</html>

style.css

body {
  font-family: Arial, sans-serif;
  background: #f5f5f5;
  margin: 0;
  padding: 20px;
}

h1 {
  text-align: center;
  color: #333;
}

.gallery {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 15px;
  margin-top: 30px;
}

.gallery img {
  width: 100%;
  height: 180px;
  object-fit: cover;
  border-radius: 10px;
  cursor: pointer;
  transition: transform 0.3s, box-shadow 0.3s;
}

.gallery img:hover {
  transform: scale(1.05);
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.3);
}

/* Lightbox Styles */
.lightbox {
  display: none;
  position: fixed;
  z-index: 10;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background: rgba(0,0,0,0.8);
  justify-content: center;
  align-items: center;
}

.lightbox img {
  max-width: 90%;
  max-height: 80%;
  border-radius: 10px;
  box-shadow: 0 0 15px #000;
}

.close-btn {
  position: absolute;
  top: 20px;
  right: 30px;
  color: white;
  font-size: 30px;
  font-weight: bold;
  cursor: pointer;
}

scripts.js

const galleryImages = document.querySelectorAll('.gallery img');
const lightbox = document.getElementById('lightbox');
const lightboxImg = document.getElementById('lightbox-img');
const closeBtn = document.getElementById('close');

// Open lightbox when image is clicked
galleryImages.forEach(img => {
  img.addEventListener('click', () => {
    lightbox.style.display = 'flex';
    lightboxImg.src = img.src;
  });
});

// Close lightbox on button click
closeBtn.addEventListener('click', () => {
  lightbox.style.display = 'none';
});

// Close lightbox when clicked outside the image
lightbox.addEventListener('click', (e) => {
  if (e.target !== lightboxImg) {
    lightbox.style.display = 'none';
  }
});

```
# OUTPUT:
![alt text](<Screenshot 2025-10-06 194739.png>)

# RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
