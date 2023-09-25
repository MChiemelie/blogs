---
title: "JavaScript - An Introduction"
seoTitle: "JavaScript - An Introduction"
seoDescription: "JavaScript is a versatile programming language used to develop applications ranging from web, mobile, servers, games, robotics, and cloud computing."
datePublished: Mon Sep 25 2023 20:40:46 GMT+0000 (Coordinated Universal Time)
cuid: clmzcs8jb000409mda5mn8f6l
slug: javascript-intro
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1695589661151/4aad3c04-efeb-47d9-82a2-54f8f7a5d7d3.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1695673805321/0ae2349c-3d17-4329-95e2-257966a32e9d.png
tags: javascript

---

# **What is JavaScript?**

JavaScript is a *programming language that is used to create dynamic and interactive web pages and web-based applications. It plays a critical role as a primary component of modern web applications and is widely supported by all major web browsers, making it a universal* language on the web.

> **JavaScript** is a [programming language](https://en.wikipedia.org/wiki/Programming_language) that is one of the core technologies of the [World Wide Web](https://en.wikipedia.org/wiki/World_Wide_Web), alongside [HTML](https://en.wikipedia.org/wiki/HTML) and [CSS](https://en.wikipedia.org/wiki/CSS). As of 2023, 98.7% of [websites](https://en.wikipedia.org/wiki/Website) use JavaScript on the [client](https://en.wikipedia.org/wiki/Client_(computing)) side for [webpage](https://en.wikipedia.org/wiki/Web_page) behavior, often incorporating third-party [libraries](https://en.wikipedia.org/wiki/Library_(computing)). All major [web browsers](https://en.wikipedia.org/wiki/Web_browser) have a dedicated [JavaScript engine](https://en.wikipedia.org/wiki/JavaScript_engine) to execute the [code](https://en.wikipedia.org/wiki/Source_code) on [users](https://en.wikipedia.org/wiki/User_(computing))' devices.
> 
> [Wikipedia](https://en.wikipedia.org/wiki/JavaScript)

**HTML** provides *structure* and *content,* such as text, images, buttons, and links, CSS improves the *appearance* of these elements and the webpage *layout*. JavaScript adds ***functionality*** to elements like buttons and links, making them ***interactive*** and ***dynamic***. It also aids in styling and layout enhancements while ***enabling elements to perform tasks and calculations.***

%[https://twitter.com/denicmarko/status/1344232974984900610] 

JavaScript is highly recognized and extends beyond the web, with applications in mobile development, desktop applications, server-side programming, games, blockchain and cryptocurrencies, and even cloud functions and serverless computing. Though there are other platforms as well, these are some of the most common areas where JavaScript is used regularly.

> JavaScript is a scripting or programming language that allows you to implement complex features on web pages — every time a web page does more than just sit there and display static information for you to look at — displaying timely content updates, interactive maps, animated 2D/3D graphics, scrolling video jukeboxes, etc. — you can bet that JavaScript is probably involved. It is the third layer of the layer cake of standard web technologies, two of which ([HTML](https://developer.mozilla.org/en-US/docs/Learn/HTML) and [CSS](https://developer.mozilla.org/en-US/docs/Learn/CSS)).
> 
> [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/What_is_JavaScript)

---

# Where and how **we use JavaScript.**

Initially, JavaScript was created to function solely within web browsers. However, it has proven to be much more versatile than originally intended. JavaScript can now be executed in a multitude of environments, such as the browser's console, Node.js runtime, and more. In this article, we will delve into the various applications and platforms where JavaScript can be utilized.

1. **Web Browsers:** JavaScript primarily operates within web browsers, empowering developers to elevate the functionality and interactivity of websites. This versatile language facilitates the creation of dynamic web pages, enables the seamless handling of user input, and facilitates communication with web servers.
    
    <div data-node-type="callout">
    <div data-node-type="callout-emoji">💡</div>
    <div data-node-type="callout-text">In this example, index.html contains a heading, a paragraph, and a button; styles.css refines the layout of the webpage and improves the visual appeal of the text and buttons. However, the real magic happens with the script.js file, each time you click the button, the displayed quote undergoes a delightful transformation<a target="_blank" rel="noopener noreferrer nofollow" href="http://transformation.Here" style="pointer-events: none">.</a></div>
    </div>
    
    ```xml
    <!DOCTYPE html>
    <html lang="en">
      <head>
        <meta charset="UTF-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
        <link rel="stylesheet" href="/styles.css">
        <title>Quotes 💭</title>
      </head>
      <body>
        <h1>Qoutable Quotes 💭</h1>
        <p id="quote"></p>
        <button id="generate">Generate Quote</button>
        <script src="/script.js"></script>
      </body>
    </html>
    ```
    
    ```css
    @import url("https://fonts.googleapis.com/css2?family=IBM+Plex+Sans&display=swap");
    
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    
    body {
      font-family: "IBM Plex Sans", sans-serif !important;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      height: 100vh;
      gap: 2%;
      text-align: center;
      background: #e7e7eb;
    }
    
    button {
      padding: 0.5rem;
      border: none;
      border-radius: 0.15rem;
      color: white;
      background: rgb(115, 63, 193);
    }
    ```
    
    ```javascript
    // A list of quotes
    const quotes = [
       "The only way to do great work is to love what you do. - Steve Jobs",
       "Life is what happens when you're busy making other plans. - John Lennon",
       "In the middle of every difficulty lies opportunity. - Albert Einstein",
       "Success is not final, failure is not fatal: It is the courage to continue that counts. - Winston Churchill"
    ];
    
    // Function to generate a random quote
    function generateQuote() {
       const randomIndex = Math.floor(Math.random() * quotes.length);
       const randomQuote = quotes[randomIndex];
       document.getElementById("quote").textContent = randomQuote;
    }
    
    // Event listener for the button click
    document.getElementById("generate").addEventListener("click", generateQuote);
    
    // Initial quote generation
    generateQuote();
    ```
    
    <div data-node-type="callout">
    <div data-node-type="callout-emoji">💡</div>
    <div data-node-type="callout-text">View the website <a target="_blank" rel="noopener noreferrer nofollow" href="https://quotes-chiemelie.vercel.app/" style="pointer-events: none">here</a>. Contribute and add your favourite quote(s) to the source code <a target="_blank" rel="noopener noreferrer nofollow" href="https://github.com/MChiemelie/quotes" style="pointer-events: none">here</a>.</div>
    </div>
    
2. **Browser Console:** The browser console serves as a useful tool within our web browser, enabling the execution of JavaScript code directly. Its primary functions include testing and debugging scripts, inspecting web page elements, and experimenting with JavaScript commands.
    
    For example, in my browser console, I recently performed a mathematical calculation involving two numbers, denoted as 'x' (with a value of 3) and 'y' (with a value of 5). The calculation was straightforward: 'sum = x + y'.
    
    To demonstrate this, I employed a JavaScript function explicitly designed to add two numbers. Here's the code I used:
    
    ```javascript
    //The below JavaScript function adds two numbers
    function sum (a, b){
        console.log(a + b); // Adds a and b and logs the output
    }
    
    sum(3, 5); // pass in the actual values for a and b
    ```
    
    Upon running this code in the console, it successfully performed the addition operation and returned the value, which can be seen in the image below:
    
    ![My browser with the console open showing how I implemented the code.](https://cdn.hashnode.com/res/hashnode/image/upload/v1695549056541/52f32d2e-e69b-4d6b-a208-c2f81fda686d.png align="center")
    
    You can see the output as labelled A on the console. This concise example illustrates how the browser console facilitates JavaScript code execution and how it aids in performing tasks like mathematical calculations, making it an invaluable tool for web development and debugging.
    
3. **Node.js Runtime**: [Node.js](https://nodejs.org/en) is a server-side runtime environment that empowers JavaScript to operate on web servers. This capability enables the development of robust and high-performance server applications, APIs, and real-time web applications.
    
    Here's an example of a JavaScript function that calculates a person's grade based on their score:
    
    ```javascript
    function calculateGrade(score) {
       if (score >= 90 && score <= 100) {
          console.log("Grade A+");
       } else if (score >= 80 && score < 90) {
          console.log("Grade A");
       } else if (score >= 70 && score < 80) {
          console.log("Grade B");
       } else if (score >= 60 && score < 70) {
          console.log("Grade C");
       } else if (score >= 50 && score < 60) {
          console.log("Grade D");
       } else if (score >= 40 && score < 50) {
          console.log("Grade E");
       } else if (score >= 0 && score < 40) {
          console.log("Grade F");
       } else if (score < 0) {
          console.log("Grade cannot be less than 0!");
       } else if (score > 100) {
          console.log("Grade cannot be greater than 100!");
       } else {
          console.log("Invalid!");
       }
    }
    
    calculateGrade(74); // Provide the actual score to determine the grade
    ```
    
    <div data-node-type="callout">
    <div data-node-type="callout-emoji">💡</div>
    <div data-node-type="callout-text">To execute the above code in your terminal, ensure that <a target="_blank" rel="noopener noreferrer nofollow" href="https://nodejs.org/en" style="pointer-events: none">Node</a> is installed.</div>
    </div>
    
    Open your terminal in your preferred Integrated Development Environment (IDE) such as VSCode and execute the following command:
    
    ```shell
    node index.js
    ```
    
    In the image below, you can observe the results displayed in the terminal. "A" signifies the command used to run the script using Node, while "B" represents the script's output.
    
    ![My IDE (VSCode) with the terminal open showing how I implemented the code using Node](https://cdn.hashnode.com/res/hashnode/image/upload/v1695562316573/d1f0e8bf-f962-4a90-81d9-565ea85f24b2.png align="center")
    
    This demonstrates how Node.js extends JavaScript's capabilities beyond web browsers to enable server-side scripting, making it a valuable tool for various applications, including web development and server applications.
    
4. **Mobile App Development:** JavaScript plays a pivotal role in the domain of mobile app development. Through frameworks such as [React Native](https://reactnative.dev/), developers gain the ability to craft cross-platform mobile applications using JavaScript and React. This approach significantly streamlines development processes, cutting down both time and effort.
    
    [![A section of the React Native documentation showing various companies using React Native.](https://cdn.hashnode.com/res/hashnode/image/upload/v1695524912227/2cdf5ab0-ee4d-4fb9-96e6-71f59af21e7e.png align="center")](https://reactnative.dev/)
    
    The above image was extracted from the React Native documentation. It showcases prominent software companies leveraging React Native to construct mobile applications.
    
5. **Desktop Applications:** JavaScript, in conjunction with HTML and CSS, serves as a versatile tool for crafting cross-platform desktop applications through the utilization of frameworks such as [Electron](https://www.electronjs.org/). This methodology empowers developers to seamlessly generate native desktop applications compatible with diverse operating systems.
    
    [![A section of the Electron documentation showing various companies using Electron.](https://cdn.hashnode.com/res/hashnode/image/upload/v1695524957425/9f170b34-b700-40b2-a887-6cd22bb0ccf2.png align="center")](https://www.electronjs.org/)
    
    The above image below was extracted directly from the official [Electron](https://www.electronjs.org/) documentation. It shows very popular software that uses Electron for building their desktop applications.
    
6. **Internet of Things (IoT):** JavaScript finds practical applications in robotics, empowering us to program IoT devices and craft applications that seamlessly interface with sensors and actuators. Platforms such as [Johnny-Five](https://johnny-five.io/) play a pivotal role in facilitating JavaScript-based robotics and IoT development.
    
    [![A section of the Johnny-Five Documentation.](https://cdn.hashnode.com/res/hashnode/image/upload/v1695525131327/d62d9b28-0d34-4583-a0bf-ae0bd5c212ed.png align="center")](https://johnny-five.io/)
    
7. **Game Development:** Game developers harness JavaScript's capabilities through libraries and engines like [Babylon.js](https://www.babylonjs.com/), [Three.js](https://threejs.org/) and [Phaser](https://phraser.tech/). These tools facilitate the creation of both 2D and 3D games that can run in web browsers.
    
    [![A section of Awwwards.com showing website and applications using Three.js](https://cdn.hashnode.com/res/hashnode/image/upload/v1695525202168/cf8326fa-913f-4465-808d-efc28347f859.png align="center")](https://www.awwwards.com/websites/three-js/)
    
8. **Blockchain and Cryptocurrency:** JavaScript plays a role in blockchain application development and smart contract creation. Ethereum, for example, employs [Solidity](https://soliditylang.org/), a JavaScript-like language, for writing smart contracts.
    
    [![A section of Solidity showing how to write a contract.](https://cdn.hashnode.com/res/hashnode/image/upload/v1695525246933/213836e4-cda8-4f06-a629-b9fa2e66051e.png align="center")](https://soliditylang.org/)
    
9. **Augmented Reality (AR) and Virtual Reality (VR):** JavaScript can be used in the development of AR and VR experiences. Frameworks like [A-Frame](https://aframe.io/) and [AR.js](https://ar-js-org.github.io/AR.js-Docs/) empower developers to build web-based AR and VR applications.
    
    [![A section of A-Frame with a showcase of web applications built with A-Frame](https://cdn.hashnode.com/res/hashnode/image/upload/v1695525293815/a2acd5c9-bea8-40d2-886c-4bf53dbc7884.png align="center")](https://aframe.io/)
    
10. **Cloud Functions and Serverless Computing:** JavaScript is compatible with serverless computing platforms such as [AWS Lambda](https://aws.amazon.com/lambda/), [Google Cloud Functions](https://cloud.google.com/functions), and [Azure Functions](https://azure.microsoft.com/en-us/products/functions). It enables the creation of serverless functions and microservices, facilitating scalable and event-driven applications.
    
    [![ a section of MircoSoft Azure Documentation showing what you can build with Function. FAQs showing that MircoSoft Azure Support JavaScript along with other programming languages.](https://cdn.hashnode.com/res/hashnode/image/upload/v1695525351801/a3c30fa2-d030-43c3-a4b4-d904490b88d1.png align="center")](https://azure.microsoft.com/en-us/products/functions)
    

JavaScript's adaptability and extensive ecosystem make it a versatile language suitable for a multitude of applications and platforms. Its ubiquity in the world of programming ensures its continued relevance and utility in various domains beyond web development.

---

### Let's run a simple JavaScript code!

Follow the below set of instructions,

1. Open your web browser (e.g., Google Chrome, Mozilla Firefox, or Safari).
    
2. Navigate to any website or simply open a new tab.
    
3. Right-click anywhere on the web page or press `Ctrl + Shift + J` or `Cmd + Option + J` on macOS to open the browser's developer tools. Click on `Inspect`.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1695654003776/0b8b61ed-58cf-4dbd-a4f1-afbf1b2f6e99.png align="center")
    
    This will open the browser console, then click on `Console`.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1695654176110/847f04c9-77e3-47e9-b9ea-d3967f3a49c6.png align="center")
    
4. In the console, paste the below JavaScript code:
    

```javascript
//  JavaScript says Hi👋🏽
function greet (name) {
  console.log(`Hi 👋🏽, ${name}.`);
}

greet("Chiemelie"); // You should replace Chiemelie with your name.
```

1. After pasting the code, you can press the `Enter` to execute it.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1695654220659/fefd7b1b-11d1-4672-afe5-796ddcef65fd.png align="center")
    
2. You should see the output in the console, which will be: "Hi 👋🏽, Chiemelie.".
    

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text">You should replace my name <code>Chiemelie</code> with your name to see the greeting with your name in the console.</div>
</div>

### Conclusion

JavaScript is a dynamic and very powerful language that can be used to build a wide range of applications for different platforms. It has a very large ecosystem of libraries and frameworks and a robust community of millions of developers who build and maintain applications written in JavaScript. Proficiency in JavaScript is a lucrative skill and valuable asset as JavaScript developers are in high demand in the Tech industry.

If you found this blog post helpful, please consider sharing it with others who might benefit. You can also follow me for more content on Javascript, React.js, Next.js and other web development topics.

To sponsor my work, please visit: [Chiemelie's Sponsor Page](https://chiemelie.hashnode.dev/sponsor) and explore the various sponsorship options.

Connect with me on [X (Twitter)](https://twitter.com/ChiemelieJM), [**LinkedIn**](https://www.linkedin.com/in/melikamchiemelie/), and [**GitHub**](https://github.com/MChiemelie).

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1695591942063/08b9a163-45df-4200-af85-69f7c48183c8.png align="center")

Thank you for reading and see you at the next one :)