# github.io-Gallery# Activity 01 
## Date: 22.03.2025

## AIM
Design and implement an interactive image gallery using JavaScript, HTML, and CSS.

## ALGORITHM
### STEP 1
Create an HTML file (index.html)

### STEP 2
Create a CSS file (style.css)

### STEP 3
Create a JS file (script.css)

### STEP 3
Include a navigation bar with links to different sections.

### STEP 5
Define global styles for fonts, colors, and layout.

### STEP 6
Style the Gallery, image, and footer.

### STEP 7
Use CSS Grid for layout design.

### STEP 8
Add hover effects and transitions for interactivity.

### STEP 9
Add Images and Media.

### STEP 10
Use optimized images for a professional look.

### STEP 11
Open the HTML file in a browser to check layout and functionality.

### STEP 12
Fix styling issues and refine content placement.

### STEP 13
Deploy the Portfolio.

### STEP 14
Upload to GitHub Pages for free hosting.

## PROGRAM
index.html
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Advanced Image Gallery</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="gallery-container">
        <h1 class="gallery-title">Explore The Nature</h1>
        <div class="gallery">
            <div class="image-wrapper">
                <img src="images/image1.jpg" alt="Image 1">
                <div class="caption">Nature's Serenity</div>
            </div>
            <div class="image-wrapper">
                <img src="images/image2.jpg" alt="Image 2">
                <div class="caption">Scary Lights</div>
            </div>
            <div class="image-wrapper">
                <img src="images/image3.jpg" alt="Image 3">
                <div class="caption">Light Of Darkt</div>
            </div>
            <div class="image-wrapper">
                <img src="images/image4.jpg" alt="Image 4">
                <div class="caption">Mountain Peaks</div>
            </div>
            <div class="image-wrapper">
                <img src="images/image5.jpg" alt="Image 5">
                <div class="caption">Silent Forest</div>
            </div>
        </div>
        <div class="navigation">
            <button id="prevBtn">&lt;</button>
            <button id="nextBtn">&gt;</button>
        </div>
    </div>
    <footer>
        <p> Roop Sagar S L - 212223040175</p>
    </footer>
    <script src="script.js"></script>
</body>
</html>x
```

style.css
```
body {
    font-family: 'Arial', sans-serif;
    margin: 0;
    padding: 0;
    background: linear-gradient(135deg, #e0f2fe, #d1c4e9);
    display: flex;
    flex-direction: column;
    min-height: 100vh;
    color: #333;
}
.gallery-container {
    width: 90%;
    max-width: 1200px;
    margin: 50px auto;
    text-align: center;
    position: relative;
}
.gallery-title {
    font-size: 2.5em;
    margin-bottom: 30px;
    color: #4a148c;
    text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.1);
}
.gallery {
    display: flex;
    overflow-x: auto;
    scroll-snap-type: x mandatory;
    -webkit-overflow-scrolling: touch;
    scrollbar-width: none;
    -ms-overflow-style: none; 
    padding-bottom: 20px;
}
.gallery::-webkit-scrollbar {
    display: none; 
}
.image-wrapper {
    flex: 0 0 80%; 
    min-width: 300px;
    height: 500px;
    margin: 0 15px;
    position: relative;
    border-radius: 10px;
    overflow: hidden;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
    scroll-snap-align: start;
    transition: transform 0.3s ease;
}
.image-wrapper:hover {
    transform: scale(1.05);
}
.image-wrapper img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    transition: transform 0.3s ease;
}
.caption {
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    background-color: rgba(0, 0, 0, 0.7);
    color: white;
    padding: 20px;
    text-align: center;
    opacity: 0;
    transition: opacity 0.3s ease;
    transform: translateY(100%);
}
.image-wrapper:hover .caption {
    opacity: 1;
    transform: translateY(0);
}
.navigation {
    position: absolute;
    top: 50%;
    left: 0;
    right: 0;
    display: flex;
    justify-content: space-between;
    transform: translateY(-50%);
}
.navigation button {
    background-color: rgba(255, 255, 255, 0.8);
    border: none;
    font-size: 2em;
    padding: 10px 20px;
    cursor: pointer;
    border-radius: 50%;
    color: #4a148c;
    transition: background-color 0.3s ease;
}
.navigation button:hover {
    background-color: rgba(255, 255, 255, 1);
}
footer {
    text-align: center;
    padding: 20px 0;
    background-color: #f0f0f0;
    margin-top: auto; 
}
```

script.js
```
document.addEventListener('DOMContentLoaded', () => {
    const gallery = document.querySelector('.gallery');
    const prevBtn = document.getElementById('prevBtn');
    const nextBtn = document.getElementById('nextBtn');
    const imageWrappers = document.querySelectorAll('.image-wrapper');
    let currentIndex = 0;
    function updateGallery() {
        gallery.scrollTo({
            left: imageWrappers[currentIndex].offsetLeft,
            behavior: 'smooth'
        });
    }
    nextBtn.addEventListener('click', () => {
        if (currentIndex < imageWrappers.length - 1) {
            currentIndex++;
            updateGallery();
        }
    });
    prevBtn.addEventListener('click', () => {
        if (currentIndex > 0) {
            currentIndex--;
            updateGallery();
        }
    });
});
```

## OUTPUT

![Screenshot 2025-03-22 122214](https://github.com/user-attachments/assets/13bfd7b4-ed95-42ef-93ff-96c8170cd4fe)

![Screenshot 2025-03-22 122226](https://github.com/user-attachments/assets/b8195353-d56e-4a7a-be24-922b8fbc46ff)

![Screenshot 2025-03-22 122241](https://github.com/user-attachments/assets/2b6ee45a-e7bc-4d4c-8885-905b71a78a17)

![Screenshot 2025-03-22 122303](https://github.com/user-attachments/assets/cb2f94e6-9a4d-483a-bc1f-1eb26237e6d6)

## RESULT
The program for creating Portfolio using HTML and CSS is executed successfully.
