# Ex.08 Design of Interactive Image Gallery
## Date:

## AIM:
To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for positioning and styling.

### Step 4:
Write JavaScript program for implementing interactivity.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
#html
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Interactive Image Gallery</title>

  <!-- Link to External CSS -->
  <link rel="stylesheet" href="styles.css">
</head>
<body>

  <!-- Gallery Heading -->
  <h1 class="gallery-heading">Interactive Image Gallery</h1>

  <!-- Image Gallery -->
  <div class="gallery">
    <div class="gallery-item">
      <img src="image1.jpg" alt="Image 1" class="gallery-img">
      <div class="image-name">CAR</div>
    </div>
    <div class="gallery-item">
      <img src="image2.jpg" alt="Image 2" class="gallery-img">
      <div class="image-name">TAJ MAHAL</div>
    </div>
    <div class="gallery-item">
      <img src="image3.jpg" alt="Image 3" class="gallery-img">
      <div class="image-name">LIZARD</div>
    </div>
    <div class="gallery-item">
      <img src="image4.jpg" alt="Image 4" class="gallery-img">
      <div class="image-name">TREE</div>
    </div>
    <div class="gallery-item">
      <img src="image5.jpg" alt="Image 5" class="gallery-img">
      <div class="image-name">RACER</div>
    </div>
    <div class="gallery-item">
      <img src="image6.jpg" alt="Image 6" class="gallery-img">
      <div class="image-name">CITY</div>
    </div>
    <div class="gallery-item">
      <img src="image7.jpg" alt="Image 7" class="gallery-img">
      <div class="image-name">BEACH</div>
    </div>
    <div class="gallery-item">
      <img src="image8.jpg" alt="Image 8" class="gallery-img">
      <div class="image-name">FACTORY</div>
    </div>
  </div>

  <!-- Modal for Enlarged Image -->
  <div id="modal" class="modal">
    <span class="close-btn" onclick="closeModal()">&times;</span>
    <img id="modal-img" src="" alt="Enlarged Image">
  </div>

  <!-- Link to External JavaScript -->
  <script src="script.js"></script>
</body>
</html>
```
#css
```
/* Global Styles */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Arial, sans-serif;
  background-color: #065f36;
  text-align: center;
}

.gallery-heading {
  margin: 20px 0;
  font-size: 2.5em;
  color: #333;
}

/* Gallery Container */
.gallery {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 15px;
  padding: 20px;
  max-width: 1100px;
  margin: 0 auto;
}

/* Gallery Item Styles */
.gallery-item {
  position: relative;
  overflow: hidden;
}

.gallery-img {
  width: 100%;
  height: 200px;
  object-fit: cover;
  border-radius: 10px;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  cursor: pointer;
}

.gallery-img:hover {
  transform: scale(1.05);
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
}

/* Image Name Styles */
.image-name {
  position: absolute;
  bottom: 10px;
  left: 50%;
  transform: translateX(-50%);
  color: white;
  font-size: 18px;
  font-weight: bold;
  background-color: rgba(13, 255, 21, 0.6);
  padding: 5px 10px;
  border-radius: 5px;
  opacity: 0;
  transition: opacity 0.3s ease;
}

.gallery-item:hover .image-name {
  opacity: 1;
}

/* Modal Styles */
.modal {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(122, 122, 122, 0.8);
  display: none;
  justify-content: center;
  align-items: center;
}

.modal img {
  max-width: 90%;
  max-height: 90%;
  object-fit: contain;
}

.close-btn {
  position: absolute;
  top: 20px;
  right: 20px;
  color: lightblue;
  font-size: 30px;
  cursor: pointer;
}
```
#js
```
const galleryImages = document.querySelectorAll('.gallery-img');
const modal = document.getElementById('modal');
const modalImg = document.getElementById('modal-img');

function openModal(event) {
  modalImg.src = event.target.src;
  modal.style.display = 'flex';
}

function closeModal() {
  modal.style.display = 'none';
}

galleryImages.forEach(image => {
  image.addEventListener('click', openModal);
});

const closeButton = document.querySelector('.close-btn');
closeButton.addEventListener('click', closeModal);

modal.addEventListener('click', (event) => {
  if (event.target === modal) {
    closeModal();
  }
});
```
## OUTPUT:
![WEB PHOTO GALLARY](https://github.com/user-attachments/assets/1c22a33b-1dc9-4671-9201-2c32baf5fc8f)

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
