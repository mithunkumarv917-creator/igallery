# Ex.08 Design of Interactive Image Gallery
## Date:16/10/2025

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
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Interactive Photo Gallery</title>
  <style>
    .gallery img {
      width: 200px;
      margin: 10px;
      cursor: pointer;
      transition: transform 0.3s;
      border-radius: 8px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.3);
    }
    .gallery img:hover {
      transform: scale(1.1);
    }
    #lightbox {
      position: fixed;
      top:0; left:0; right:0; bottom:0;
      background: rgba(0,0,0,0.8);
      display:none;
      justify-content:center;
      align-items:center;
      z-index: 999;
    }
    #lightbox img {
      max-width: 90%;
      max-height: 90%;
      border-radius: 10px;
      box-shadow: 0 0 15px white;
    }
  </style>
</head>
<body>
{% load static %}

<h1>Interactive Photo Gallery</h1>
<div class="gallery">
  {% for img in images %}
<img src="{% static img %}" alt="Photo" onclick="openLightbox(this.src)">
  {% endfor %}
</div>

<div id="lightbox" onclick="closeLightbox()">
  <img id="lightbox-img" src="" alt="Large view">
</div>

<script>
  function openLightbox(src) {
    document.getElementById('lightbox-img').src = src;
    document.getElementById('lightbox').style.display = 'flex';
  }
  function closeLightbox() {
    document.getElementById('lightbox').style.display = 'none';
  }
</script>

</body>
</html>

```

## OUTPUT:
<img width="1918" height="932" alt="Screenshot 2025-10-09 123354" src="https://github.com/user-attachments/assets/0782436e-e6f9-4179-a68a-ae2425c4badb" />
<img width="1911" height="937" alt="Screenshot 2025-10-09 123405" src="https://github.com/user-attachments/assets/d8803be0-2d7e-4fe1-9cea-f9cb12bc7e3e" />
<img width="1919" height="950" alt="Screenshot 2025-10-09 123416" src="https://github.com/user-attachments/assets/7a46a936-3e37-4de4-834b-2aa53d5a1278" />
<img width="1915" height="947" alt="Screenshot 2025-10-09 123429" src="https://github.com/user-attachments/assets/b51d439b-d2d6-4b6b-9b64-8bfa3484d4d3" />


## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
