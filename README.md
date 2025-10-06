# Ex.08 Design of Interactive Image Gallery
## Date: 05-10-2025

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
hakai.html

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gallery</title>
    <link rel="stylesheet"
        href="https://fonts.googleapis.com/css2?family=Inter:wght@400;700&family=Playfair+Display:wght@700&display=swap">
    <link rel="stylesheet" href="hakai.css">
</head>

<body>
    <div class="container">
        <div class="main-items" ><img src="MyPhoto.jpg" alt="MyPhoto"></div>
        <div class="main-items"><img src="https://variety.com/wp-content/uploads/2023/06/MCDIRMA_EC014.jpg"
                alt="Robert Downey Jr. as Iron Man"></div>
        <div class="main-items"><img
                src="ec77djag.png"
                alt="Chris Evans as Captain America"></div>
        <div class="main-items"><img src="https://variety.com/wp-content/uploads/2022/08/patty-thor-2.png"
                alt="Chris Hemsworth as Thor"></div>
        <div class="main-items"><img
                src="https://www.hollywoodreporter.com/wp-content/uploads/2021/07/MCDAVEN_EC081-H-2021.jpg?w=1296"
                alt="Jeremy Renner as Hawkeye"></div>
    </div>
    <h2>&copy; Image Gallery | designed by: <br> <strong>JEFFRIN I | 25009198</strong></h2>
    <div id="modal" class="modal">
        <span class="close"></span>
        <img id="modalImg" class="modal-content">
    </div>
    <script>
        var modal = document.getElementById('modal');
        var modalImg = document.getElementById('modalImg');
        document.querySelectorAll('.main-items img').forEach(img =>
            img.onclick = () => {
                modal.style.display = 'block';
                modalImg.src = img.src;
            }
        );
        modal.addEventListener('click', (e) => {
            if (e.target === modal) {
                modal.style.display = 'none';
            }
        });

    </script>
</body>

</html>

hakai.css

* {
    padding: 0px;
    margin: 0px;
    box-sizing: border-box;
}

body {
    background-color: skyblue;
    overflow-x: hidden;
}

.main-items img {
    width: 300px;
    height: auto;
    cursor: pointer;
    padding: 10px;
    border-radius: 10%;
}

.modal {
    display: none;
    position: fixed;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    overflow: auto;
    background-color: rgba(0, 0, 0, 0.9);
    padding-top: 60px;
}

.modal img {
    margin: auto;
    display: block;
    max-width: 80vw;
    max-height: 80vh;
}

.container {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: center;
    margin-top: 150px;
    background-color: lemonchiffon;
    padding: 50px 0px 50px 0px;
}

.close {
    position: absolute;
    top: 15px;
    right: 35px;
    color: white;
    font-size: 40px;
    font-weight: bold;
    transition: 0.3s;
}

.close:hover,
.close:focus {
    color: #bbb;
    text-decoration: none;
    cursor: pointer;
}

h2 {
    letter-spacing: normal;
    position: absolute;
    left: 70%;
    top:70%;
    color:rgb(179, 5, 5);
    font-family: inter;
}

```
## OUTPUT:
![alt text](<jeff/Screenshot (76).png>)
![alt text](<Screenshot (77).png>)

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
