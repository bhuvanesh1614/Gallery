# Ex.08 Design of Interactive Image Gallery
# Date:08-10-2025
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
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Interactive Photo Gallery</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f4f4f4;
      margin: 0;
      padding: 20px;
    }
    h1 {
      text-align: center;
    }
    .gallery {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
      gap: 15px;
      margin-top: 20px;
    }
    .gallery img {
      width: 100%;
      height: auto;
      cursor: pointer;
      border-radius: 8px;
      transition: transform 0.3s ease;
    }
    .gallery img:hover {
      transform: scale(1.25);
    }
    .lightbox {
      position: fixed;
      top: 0; left: 0;
      width: 100%; height: 100%;
      background: rgba(0,0,0,0.8);
      display: none;
      justify-content: center;
      align-items: center;
    }
    .lightbox img {
      max-width: 90%;
      max-height: 80%;
      border-radius: 10px;
    }
    body{
        background-image:linear-gradient(90deg,yellow,rgb(10, 157, 215),rgb(61, 247, 61));
    }
  </style>
</head>
<body>

<h1>MY PHOTO GALLERY </h1>
<div class="gallery">
  <img src="du.png" alt="Photo 1">
  <img src="ja.png" alt="Photo 2">
  <img src="dh.png" alt="Photo 3">
  <img src="pa.png" alt="Photo 4">
  <img src="ru.png" alt="Photo 5">
</div>

<div class="lightbox" id="lightbox">
  <img src="" alt="Enlarged photo">
</div>

<script>
  const galleryImages = document.querySelectorAll('.gallery img');
  const lightbox = document.getElementById('lightbox');
  const lightboxImg = lightbox.querySelector('img');

  galleryImages.forEach(img => {
    img.addEventListener('click', () => {
      lightboxImg.src = img.src;
      lightbox.style.display = 'flex';
    });
  });

  lightbox.addEventListener('click', () => {
    lightbox.style.display = 'none';
  });
</script>

</body>
</html>
```
# OUTPUT:
![alt text](<Screenshot 2025-10-08 150458.png>)
# RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
