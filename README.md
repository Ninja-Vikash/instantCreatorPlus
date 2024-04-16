# InstantCreator+

[![npm Button](https://img.shields.io/badge/npm-CB3837?style=for-the-badge&logo=npm&logoColor=white)](https://www.npmjs.com/)

---
<img heigh="30px" width="30px" src="https://github.com/Ninja-Vikash/asset-cloud/blob/main/icon%20%26%20png/nodejs.png" align="left">
InstantCreator+ represents the latest advancement, surpassing its predecessors and establishing itself as the pinnacle version.

---

**Key Features:**
- **Updated code**
- Quickly generates files with their initial code.
- Automates the creation of `index.html` and `style.css` files, complete with boilerplate HTML and CSS resetting code.

Get started effortlessly with InstantCreator+ for a seamless and efficient front-end development experience! 🚀✨

### How to use it

1. Create a folder for your project.
2. Create `main.js`.
3. Initialize npm in your directory using:
   ```bash
   npm init -y
   ```
   
   > Use `npm init -y` to skip configuration prompts during initialization.
4. Change type to module in `package.json`
   ```json
     "type": "module",
   ```
5. Install dependencies
   ```bash
   npm i chalk
   ```
6. Paste the following code into your `main.js` file:
    ```js
    import fs from 'fs'
    import chalk from 'chalk';

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
       <!---------------- You are using instantCreator+ ----------------> 
      <main>
        <h1>Welcome to <span>instantCreator</span>.</h1>

         <figure>
            <img src="assets/html.svg" alt="">
         </figure>
         
         <div>
            <p>powered by</p>
            <img src="assets/nodejs.svg" alt="">
         </div>
      </main> 

      <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.5/gsap.min.js" integrity="sha512-7eHRwcbYkK4d9g/6tD/mhkf++eoTHwpNM9woBxtPUBWm67zeAfFC+HrdoE2GanKeocly/VxeLvIqwvCdk7qScg==" crossorigin="anonymous" referrerpolicy="no-referrer"></script>
      <script src="script.js"></script>
    </body>
    </html>`;

    fs.writeFile("index.html", HTMLFile, () => {
      console.log(chalk.blue("\u2713 DONE "+ chalk.white(": HTML file creation!")));
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
      overflow: hidden;
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
      font-weight: 300;
      }

      main h1 span {
      font-weight: 500;
      }

      main figure img {
      height: 400px;
      }

      main div {
      position: absolute;
      bottom: 10px;
      display: flex;
      align-items: center;
      gap: 16px;
      }

      main p {
      color: #ccc;
      }

      main div > img {
      width: 80px;
      }`;

    fs.writeFile("style.css", CSSFile, () => {
       console.log(chalk.blue("\u2713 DONE "+ chalk.white(": CSS file creation!")));
    });
      
    // -------------------- CODE FOR JS WRITING
    const scriptJS = `gsap.from("figure img", {
      opacity: 0,
      y: 100,
      scale: 0.8,
      duration: 2,
    })

    gsap.from("main div", {
      opacity: 0,
      y: 200,
      duration: 5
    })`

    fs.writeFile("script.js", scriptJS, ()=>{
      console.log(chalk.blue("\u2713 DONE "+ chalk.white(": JS file creation!")));
    })


    // --------------------- CODE FOR DIRECTORY CREATING
    fs.mkdir("assets", () => {
       console.log(chalk.blue("\u2713 DONE "+ chalk.white(": Directory creation!")));
    });

    // --------------------- CODE FOR SVG WRITING
    const SVGFile = `
    <svg xmlns="http://www.w3.org/2000/svg" x="0px" y="0px" width="100" height="100" viewBox="0 0 64 64">
    <path fill="orange" d="M10.814,11.264l3.267,37.028c0.142,1.608,1.237,2.974,2.776,3.462l11.784,3.734	c2.185,0.692,4.531,0.692,6.716,0l11.784-3.734c1.539-0.488,2.634-1.853,2.776-3.462l3.267-37.028C53.34,9.51,51.958,8,50.197,8	H13.803C12.042,8,10.66,9.51,10.814,11.264z"></path><path d="M47.142,51.753c1.539-0.488,2.634-1.853,2.776-3.462l1.434-16.255 c-2.739-0.248-5.177,1.79-5.42,4.541l-0.878,9.946c-0.035,0.402-0.309,0.743-0.694,0.865l-7.704,2.441 c-2.469,0.782-4.09,3.28-3.565,5.816c0.021,0.101,0.061,0.191,0.087,0.289c0.736-0.078,1.467-0.223,2.18-0.449L47.142,51.753z" opacity=".15"></path><path fill="#fff" d="M10.814,11.264l2.182,24.731c0.865-0.079,1.761-0.417,2.691-1.397 c1.317-1.388,1.912-3.315,1.744-5.221l-1.349-15.288C16.031,13.503,16.492,13,17.079,13H23c2.761,0,4.997-2.239,4.997-5H13.803 C12.042,8,10.659,9.51,10.814,11.264z" opacity=".3"></path><path fill="#ffce29" d="M32,15v33.334c0,1.333,1.28,2.293,2.56,1.92l9.204-2.682c0.793-0.231,1.363-0.927,1.433-1.75	l2.618-30.652c0.1-1.167-0.821-2.17-1.993-2.17H34C32.895,13,32,13.895,32,15z"></path><path fill="#fff" d="M32,33v-5h9.928c0.58,0,1.038,0.491,0.998,1.069l-0.9,12.986c-0.028,0.405-0.298,0.753-0.684,0.88	L32,46.021v-5.325l5.179-1.775l0.379-5.898L32,33z M43.312,22.075l0.227-2.999C43.584,18.495,43.124,18,42.542,18H32l-0.014,4.986	l10.328,0.013C42.837,23,43.273,22.597,43.312,22.075z"></path><path fill="#eee" d="M32,40.716v5.305l-9.344-3.075c-0.384-0.126-0.654-0.472-0.685-0.875l-0.375-4.99	c-0.044-0.58,0.415-1.075,0.997-1.075h3.057c0.519,0,0.952,0.397,0.996,0.914l0.174,2.027L32,40.716z M25.811,22.991H32v-4.982	H21.566c-0.575,0-1.032,0.484-0.998,1.059l0.766,13.001c0.031,0.529,0.469,0.941,0.998,0.941H32v-5.006h-5.811L25.811,22.991z"></path><ellipse cx="32" cy="61" opacity=".3" rx="20" ry="3"></ellipse><polyline fill="none" stroke="#fff" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" stroke-width="3" points="14.857,17.256 14.349,11.5 19.067,11.5"></polyline>
    </svg>
    `;

    const SVGNodejs =`
    <svg xmlns="http://www.w3.org/2000/svg" x="0px" y="0px" width="100" height="100" viewBox="0 0 48 48">
    <path fill="#388e3c" d="M17.204 19.122l-4.907 2.715C12.113 21.938 12 22.126 12 22.329v5.433c0 .203.113.39.297.492l4.908 2.717c.183.101.41.101.593 0l4.907-2.717C22.887 28.152 23 27.965 23 27.762v-5.433c0-.203-.113-.39-.297-.492l-4.906-2.715c-.092-.051-.195-.076-.297-.076-.103 0-.205.025-.297.076M42.451 24.013l-.818.452c-.031.017-.049.048-.049.082v.906c0 .034.019.065.049.082l.818.453c.031.017.068.017.099 0l.818-.453c.03-.017.049-.048.049-.082v-.906c0-.034-.019-.065-.05-.082l-.818-.452C42.534 24.004 42.517 24 42.5 24S42.466 24.004 42.451 24.013"></path><path fill="#37474f" d="M35.751,13.364l-2.389-1.333c-0.075-0.042-0.167-0.041-0.241,0.003 c-0.074,0.044-0.12,0.123-0.12,0.209L33,20.295l-2.203-1.219C30.705,19.025,30.602,19,30.5,19c-0.102,0-0.205,0.025-0.297,0.076 h0.001l-4.907,2.715C25.113,21.892,25,22.08,25,22.282v5.433c0,0.203,0.113,0.39,0.297,0.492l4.908,2.717 c0.183,0.101,0.41,0.101,0.593,0l4.907-2.717C35.887,28.106,36,27.918,36,27.715V13.788C36,13.612,35.904,13.45,35.751,13.364z M32.866,26.458l-2.23,1.235c-0.083,0.046-0.186,0.046-0.269,0l-2.231-1.235C28.051,26.412,28,26.326,28,26.234v-2.47 c0-0.092,0.051-0.177,0.135-0.224l2.231-1.234h-0.001c0.042-0.023,0.088-0.034,0.135-0.034c0.047,0,0.093,0.012,0.135,0.034 l2.23,1.234C32.949,23.587,33,23.673,33,23.765v2.47C33,26.326,32.949,26.412,32.866,26.458z"></path><path fill="#2e7d32" d="M17.204,19.122L12,27.762c0,0.203,0.113,0.39,0.297,0.492l4.908,2.717 c0.183,0.101,0.41,0.101,0.593,0L23,22.329c0-0.203-0.113-0.39-0.297-0.492l-4.906-2.715c-0.092-0.051-0.195-0.076-0.297-0.076 c-0.103,0-0.205,0.025-0.297,0.076"></path><path fill="#4caf50" d="M17.204,19.122l-4.907,2.715C12.113,21.938,12,22.126,12,22.329l5.204,8.642 c0.183,0.101,0.41,0.101,0.593,0l4.907-2.717C22.887,28.152,23,27.965,23,27.762l-5.203-8.64c-0.092-0.051-0.195-0.076-0.297-0.076 c-0.103,0-0.205,0.025-0.297,0.076"></path><path fill="#37474f" d="M47.703 21.791l-4.906-2.715C42.705 19.025 42.602 19 42.5 19c-.102 0-.205.025-.297.076h.001l-4.907 2.715C37.114 21.892 37 22.084 37 22.294v5.411c0 .209.114.402.297.503l4.908 2.717c.184.102.409.102.593 0l2.263-1.253c.207-.115.206-.412-.002-.526l-4.924-2.687C40.052 26.412 40 26.325 40 26.231v-2.466c0-.092.05-.177.13-.221l2.235-1.236h-.001c.042-.023.088-.034.135-.034.047 0 .093.012.135.034l2.235 1.237c.08.044.13.129.13.221v2.012c0 .086.046.166.121.209.075.042.167.042.242-.001l2.398-1.393c.148-.086.24-.245.24-.417v-1.88C48 22.085 47.886 21.892 47.703 21.791zM10.703 21.791l-4.906-2.715C5.705 19.025 5.602 19 5.5 19c-.102 0-.205.025-.297.076h.001l-4.907 2.715C.114 21.892 0 22.084 0 22.294v7.465c0 .086.046.166.121.209.075.042.167.042.242-.001l2.398-1.393C2.909 28.488 3 28.329 3 28.157v-4.393c0-.092.05-.177.13-.221l2.235-1.236H5.365c.042-.023.088-.034.135-.034.047 0 .093.012.135.034l2.235 1.237C7.95 23.588 8 23.673 8 23.765v4.393c0 .172.091.331.24.417l2.398 1.393c.075.043.167.043.242.001C10.954 29.925 11 29.845 11 29.759v-7.464C11 22.085 10.886 21.892 10.703 21.791z"></path>
    </svg>
   `;

    fs.writeFile("./assets/html.svg", SVGFile, () => {
       console.log(chalk.blue("\u2713 DONE "+ chalk.white(": SVG file creation!")));
    });

    
    fs.writeFile("./assets/nodejs.svg", SVGNodejs, () => {
       console.log(chalk.blue("\u2713 DONE "+ chalk.white(": SVG file creation!")));
    });

    setTimeout(() => {
      console.log(chalk.green("\u2713 Deployment done!"))
    }, 500);
    ```

    > Code for InstantCreator+.

> [!WARNING]\
> Make sure you have run `npm i chalk`

5. To run the code, execute the following command in your terminal:
    ```
    node main.js
    ```
    
## Benefits

- HTML file with boilerplate and Introduction text
- CSS file with style for Introduction
- SCRIPT file with GSAP starter code
- **A single page webpage to preview in browser**

### Prerequisites

Ensure you have Node.js installed on your PC, as npm won't work without it.

### InstantCreator+

InstantCreator+ is the new version of <a href="https://github.com/Ninja-Vikash/instantCreator">instantCreator</a>.
