---
layout: post
title: About
permalink: /about/
---

{% include nav/home.html %}

## As a conversation Starter

Here are some important places in my life.

<comment>
Flags are made using Wikipedia images.
</comment>

<style>
    /* Style looks pretty compact, 
       - grid-container and grid-item are referenced the code 
    */
    .grid-container {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(150px, 1fr)); /* Dynamic columns */
        gap: 10px;
    }
    .grid-item {
        text-align: center;
    }
    .grid-item img {
        width: 100%;
        height: 100px; /* Fixed height for uniformity */
        object-fit: contain; /* Ensure the image fits within the fixed height */
    }
    .grid-item p {
        margin: 5px 0; /* Add some margin for spacing */
    }

    .image-gallery {
        display: flex;
        flex-wrap: nowrap;
        overflow-x: auto;
        gap: 10px;
        }

    .image-gallery img {
        max-height: 150px;
        object-fit: cover;
        border-radius: 5px;
    }
</style>

<!-- This grid_container class is used by CSS styling and the id is used by JavaScript connection -->
<div class="grid-container" id="grid_container">
    <!-- content will be added here by JavaScript -->
</div>

<script>
    // 1. Make a connection to the HTML container defined in the HTML div
    var container = document.getElementById("grid_container"); // This container connects to the HTML div

    // 2. Define a JavaScript object for our http source and our data rows for the Living in the World grid
    var http_source = "https://upload.wikimedia.org/wikipedia/commons/";
    var living_in_the_world = [
        {"flag": "0/01/Flag_of_California.svg", "greeting": "", "description": "California - I was born in California and have lived here my whole life"},
        {"flag": "thumb/f/f7/Flag_of_Pennsylvania.svg/640px-Flag_of_Pennsylvania.svg.png", "greeting": "", "description": "Pennsylvania - My dad was born in Pennsylvania and this heavily influences my favorite football team (the Steelers)"},
        {"flag": "thumb/9/96/Flag_of_Connecticut.svg/640px-Flag_of_Connecticut.svg.png", "greeting": "", "description": "Connecticut - My mom was born here and grew up here for the first 20 years of her life. We visit Connecticut every other summer to reunite with family members"},
       // {"flag": "e/ef/Flag_of_Hawaii.svg", "greeting": "Aloha", "description": "Hawaii - 2 years"},
    ];

    // 3a. Consider how to update style count for size of container
    // The grid-template-columns has been defined as dynamic with auto-fill and minmax

    // 3b. Build grid items inside of our container for each row of data
    for (const location of living_in_the_world) {
        // Create a "div" with "class grid-item" for each row
        var gridItem = document.createElement("div");
        gridItem.className = "grid-item";  // This class name connects the gridItem to the CSS style elements
        // Add "img" HTML tag for the flag
        var img = document.createElement("img");
        img.src = http_source + location.flag; // concatenate the source and flag
        img.alt = location.flag + " Flag"; // add alt text for accessibility

        // Add "p" HTML tag for the description
        var description = document.createElement("p");
        description.textContent = location.description; // extract the description

        // Add "p" HTML tag for the greeting
        var greeting = document.createElement("p");
        greeting.textContent = location.greeting;  // extract the greeting

        // Append img and p HTML tags to the grid item DIV
        gridItem.appendChild(img);
        gridItem.appendChild(description);
        gridItem.appendChild(greeting);

        // Append the grid item DIV to the container DIV
        container.appendChild(gridItem);
    }
</script>

### Some things about me


- 🏀 Basketball is my favorite sport and has been my favorite sport my whole life
- 🏈 I love watching football and played last year for the Del Norte freshman team 
- 🎮 Video games are one of my favorite ways to pass my free time with my friends 
- 🎓 I am in the high school class of 2027
- 🎶 I love listening to music, my favorite genres at the moment are RnB and underground rap 
- 📸 Sports photography is a hobby of mine when I am not playing
- 👨‍👦‍👦 I have 2 step siblings and 2 biological siblings
- 🏂 My family and I love snowboarding and we go many times a year.


### Culture, and Friends

Here are some things about my culture, friends, and sports.


- I am Hungarian, English, and Irish.
- I have many friends in school but the two friends that I have kept close since second grade are Grant and Samuel. (can be seen in the last picture in the gallery)
- The gallery of pics has some of me, my family, and my friends.


<comment>
Gallery of Pics, scroll to the right for more ...
</comment>
<div class="image-gallery">
  <img src="{{site.baseurl}}/images/about/IMG_4441.PNG" alt="Image 1">
  <img src="{{site.baseurl}}/images/about/IMG_4982.PNG" alt="Image 2">
  <img src="{{site.baseurl}}/images/about/IMG_6340.PNG" alt="Image 3">
  <img src="{{site.baseurl}}/images/about/IMG_7389.PNG" alt="Image 4">
  <img src="{{site.baseurl}}/images/about/IMG_7483.PNG" alt="Image 5">
  <img src="{{site.baseurl}}/images/about/IMG_7388.PNG" alt="Image 6">
  <img src="{{site.baseurl}}/images/about/IMG_7267.PNG" alt="Image 7">
  <img src="{{site.baseurl}}/images/about/IMG_6596.jpg" alt="Image 8">
  <img src="{{site.baseurl}}/images/about/IMG_5514.JPG" alt="Image 9">
  <img src="{{site.baseurl}}/images/about/IMG_5501.PNG" alt="Image 10">
  <img src="{{site.baseurl}}/images/about/IMG_5498.PNG" alt="Image 11">
  <img src="{{site.baseurl}}/images/about/IMG_5490.PNG" alt="Image 12">
  <img src="{{site.baseurl}}/images/about/DSC01753.jpeg" alt="Image 13">
  <img src="{{site.baseurl}}/images/about/Screenshot 2024-09-06 230622.png" alt="Image 14">
    
</div>


<script src="https://utteranc.es/client.js"
        repo="{{ site.github_username }}/{{ site.github_repo | default: site.baseurl | remove: "/" }}"
        issue-term="title"
        theme="github-light"
        crossorigin="anonymous"
        async>
</script>
