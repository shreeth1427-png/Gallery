# Ex.08 Design of Interactive Image Gallery
# Date:
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
gallary.html
<!DOCTYPE html>
<html>
<head>
  <title>Image Gallery</title>
  <style>
    body {
  background: #de5f16;
  font-family: Arial, sans-serif;
  margin: 0;
  display: flex;
  flex-direction: column;
  align-items: center;
}

h2 {
  margin: 20px;
}

.gallery {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 15px;
  padding: 20px;
}

.gallery img {
  width: 200px;
  height: 250px;
  object-fit: cover;
  border-radius: 10px;
  cursor: pointer;
  transition: transform 0.2s;
}

.gallery img:hover {
  transform: scale(1.05);
}


.popup {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.8);
  display: none;
  justify-content: center;
  align-items: center;
}

.popup img {
  width: 60%;
  max-width: 400px;
  border-radius: 12px;
  box-shadow: 0 0 20px #000;
}

.popup span {
  position: absolute;
  top: 20px;
  right: 40px;
  font-size: 30px;
  color: white;
  cursor: pointer;
  font-weight: bold;
}

script.js

const popup = document.getElementById('popup');
const popupImg = document.getElementById('popupImg');
const closeBtn = document.getElementById('close');

document.querySelectorAll('.gallery img').forEach(img => {
  img.addEventListener('click', () => {
    popup.style.display = 'flex';
    popupImg.src = img.src;
  });
});

closeBtn.addEventListener('click', () => {
  popup.style.display = 'none';
});

popup.addEventListener('click', e => {
  if (e.target === popup) popup.style.display = 'none';
});

  </style>
</head>
<body>
  <h2> Image Gallery</h2>

  <div class="gallery">
    <img src="ajith.jpg" alt="Photo 1">
    <img src="dhanush.jpg" alt="Photo 2">
    <img src="karthi.jpg" alt="Photo 3">
    <img src="vijay.jpg" alt="Photo 4">
  </div>

  <div class="popup" id="popup">
    <span id="close">&times;</span>
    <img id="popupImg" src="">
  </div>
  <center>
    <h3>&copy;tejashree Designed by:</h3>
    <h2>TEJASHREE</h2>
  </center>

  <script src="script.js"></script>
</body>
</html>
```
# OUTPUT:
<img width="1898" height="977" alt="image" src="https://github.com/user-attachments/assets/99169ef7-b540-446c-9869-270514fce39e" />

# RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
