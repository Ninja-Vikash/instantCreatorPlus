# InstantCreator+

InstantCreator+ represents the latest advancement, surpassing its predecessors and establishing itself as the pinnacle version.

**Key Features:**
- **Updated code**
- Quickly generates files with their initial code.
- Automates the creation of `index.html` and `style.css` files, complete with boilerplate HTML and CSS resetting code.

Get started effortlessly with InstantCreator+ for a seamless and efficient front-end development experience! 🚀✨

### How to use it

1. Create a folder for your project.
2. Create `main.js`.
3. Initialize npm in your directory using:
   ```
   npm init -y
   ```
   
   > Use `npm init -y` to skip configuration prompts during initialization.

4. Paste the following code into your `main.js` file:
    ```
    const fs = require("fs");
    const path = require("path");

    // -------------------- CODE FOR HTML WRITING
    const HTMLFile = `<!DOCTYPE html> 
    <html lang="en"> 
    <head> 
    <meta charset="UTF-8"> 
    <meta name="viewport" content="width=device-width, initial-scale=1.0"> 
    <title>instantCreator</title> 
    <link rel="stylesheet" href="style.css"> 
    </head> 
    <body> 
    <!-- Thanks for using instantCreator --> 
    <main>
        <h1>Welcome to <span>instantCreator</span>.</h1>

        <figure>
            <img src="assets/html.svg" alt="">
        </figure>
    </main> 
    </body>
    </html>

    `;
    fs.writeFile("index.html", HTMLFile, () => {
    console.log("HTML File written!");
    });

    // -------------------- CODE FOR CSS WRITING
    const CSSFile = `@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@200;400;500;700;900&display=swap'); 

    * { 
    margin: 0; 
    padding: 0; 
    box-sizing: border-box; 
    font-family: 'Poppins';
    } 

    body, 
    html { 
    height: 100%; 
    width: 100%;
    }

    main {
    background-color: #09001c;
    height: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    }

    main h1 {
    color : white;
    font-size: 34px;
    font-weight: 400;
    }

    main h1 span {
    font-weight: 600;
    }

    main figure :nth-child(1) {
    height: 400px;
    animation: rotateX 7s linear infinite;
    }

    @keyframes rotateX {
    to{
        transform: rotateY(360deg);
    }
    }
    `;

    fs.writeFile("style.css", CSSFile, () => {
    console.log("CSS File written!");
    });

    // --------------------- CODE FOR DIRECTORY CREATING
    fs.mkdir(path.join(__dirname, "assets"), () => {
    console.log("Directory created successfully!");
    });

    // --------------------- CODE FOR SVG WRITING
    const SVGFile = `
    <svg xmlns="http://www.w3.org/2000/svg" x="0px" y="0px" width="100" height="100" viewBox="0 0 64 64">
    <path fill="orange" d="M10.814,11.264l3.267,37.028c0.142,1.608,1.237,2.974,2.776,3.462l11.784,3.734	c2.185,0.692,4.531,0.692,6.716,0l11.784-3.734c1.539-0.488,2.634-1.853,2.776-3.462l3.267-37.028C53.34,9.51,51.958,8,50.197,8	H13.803C12.042,8,10.66,9.51,10.814,11.264z"></path><path d="M47.142,51.753c1.539-0.488,2.634-1.853,2.776-3.462l1.434-16.255 c-2.739-0.248-5.177,1.79-5.42,4.541l-0.878,9.946c-0.035,0.402-0.309,0.743-0.694,0.865l-7.704,2.441 c-2.469,0.782-4.09,3.28-3.565,5.816c0.021,0.101,0.061,0.191,0.087,0.289c0.736-0.078,1.467-0.223,2.18-0.449L47.142,51.753z" opacity=".15"></path><path fill="#fff" d="M10.814,11.264l2.182,24.731c0.865-0.079,1.761-0.417,2.691-1.397 c1.317-1.388,1.912-3.315,1.744-5.221l-1.349-15.288C16.031,13.503,16.492,13,17.079,13H23c2.761,0,4.997-2.239,4.997-5H13.803 C12.042,8,10.659,9.51,10.814,11.264z" opacity=".3"></path><path fill="#ffce29" d="M32,15v33.334c0,1.333,1.28,2.293,2.56,1.92l9.204-2.682c0.793-0.231,1.363-0.927,1.433-1.75	l2.618-30.652c0.1-1.167-0.821-2.17-1.993-2.17H34C32.895,13,32,13.895,32,15z"></path><path fill="#fff" d="M32,33v-5h9.928c0.58,0,1.038,0.491,0.998,1.069l-0.9,12.986c-0.028,0.405-0.298,0.753-0.684,0.88	L32,46.021v-5.325l5.179-1.775l0.379-5.898L32,33z M43.312,22.075l0.227-2.999C43.584,18.495,43.124,18,42.542,18H32l-0.014,4.986	l10.328,0.013C42.837,23,43.273,22.597,43.312,22.075z"></path><path fill="#eee" d="M32,40.716v5.305l-9.344-3.075c-0.384-0.126-0.654-0.472-0.685-0.875l-0.375-4.99	c-0.044-0.58,0.415-1.075,0.997-1.075h3.057c0.519,0,0.952,0.397,0.996,0.914l0.174,2.027L32,40.716z M25.811,22.991H32v-4.982	H21.566c-0.575,0-1.032,0.484-0.998,1.059l0.766,13.001c0.031,0.529,0.469,0.941,0.998,0.941H32v-5.006h-5.811L25.811,22.991z"></path><ellipse cx="32" cy="61" opacity=".3" rx="20" ry="3"></ellipse><polyline fill="none" stroke="#fff" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" stroke-width="3" points="14.857,17.256 14.349,11.5 19.067,11.5"></polyline>
    </svg>
    `;

    fs.writeFile("./assets/html.svg", SVGFile, () => {
    console.log("SVG File written!");
    });
    ```

    > Code for InstantCreator+.

5. To run the code, execute the following command in your terminal:
    ```
    node main.js
    ```
    
## Benefits

- HTML file with boilerplate and Introduction text
- CSS file with style for Introduction
- **A single page webpage to preview in browser**

### Prerequisites

Ensure you have Node.js installed on your PC, as npm won't work without it.

### InstantCreator

InstantCreator+ is the new version of instantCreator.
