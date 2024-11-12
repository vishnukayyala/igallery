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
'''
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
'''

## OUTPUT:

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
