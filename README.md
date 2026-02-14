# Machine Learning Course

Opgaver og noter fra ML-kurset.

## Struktur

Projektet er organiseret efter sessions, hvor hver session indeholder de tilhørende labs/opgaver.

## Moduler

### Module 1: TensorFlow Basics
- Lab 2.1:
2.1 Install and run TensorFlow.js in the browser
In this lab you will install TensorFlow on a simple single page web application.

Create a new file in your favourite text editor or IDE. In the video lectures I used the Atom editor.
Create a simple HTML file.
Add this script tag to the HTML file:
<script src="https://cdn.jsdelivr.net/npm/@tensorflow/tfjs/dist/tf.min.js"></script>
You can check the official TensorFlow.js setup page to see if this is the latest version.
Open the page in your web browser. In the video lectures I used Chrome but you can use any modern browser.
Open the web console. In Chrome you can access this by right-clicking on the page, selecting Inspect, then selecting the Console tab (other browsers are similar).
Run tf.version in the console to verify TensorFlow is setup and see which version is running.
Run tf.getBackend() to see the backend in use. In most modern browsers, this will be "webgl".
You can also copy and paste the sample code from the official TensorFlow.js setup page into a script tag on your page and refresh it. You should see output related to training a machine learning model. Don't worry about what the code means: we'll cover the TensorFlow.js APIs later in this course!
Great, now you've set up TensorFlow.js in the browser!

Optional extra exercise

If you are an experienced JavaScript (or TypeScript) developer, you might typically use an application bundler such as Webpack to package front end assets such as JavaScript files.

Instead of using the script tag above, install via npm or yarn as listed on the official TensorFlow.js setup page. Integrate into your typical build process. Run the verification steps (from step 6 above) to ensure it is working.

- Lab 2.2:
2.2 Install and run TensorFlow.js on Node.js (check for updates and new versions)
In this lab you will install TensorFlow.js in a Node.js project and run sample code on the command line. If you never plan to run TensorFlow.js in Node.js, feel free to skip this lab.

Note: we will primarily be using TensorFlow.js in the browser in this course, as it allows us to easily visualize the data we are working with. However, the labs can be adapted for Node.js, and in future labs there will be hints for running the labs in Node.js, should you wish to do so.

In this lab we include instructions for the bash command prompt which is a common default shell on Mac and Linux systems. It is also available on Windows using the Windows Subsystem for Linux.

Open a command line prompt (this depends on your system, if in doubt search "command line [operating system name/version").
On the command line, create a new folder for the project. eg. mkdir tensorflow-lab-2.2.
Change directory into the folder, e.g. cd tensorflow-lab-2.2.
Initialise a Node.js project in the folder by running npm init (accept the default options).
If you see "Command 'npm' not found", this suggests Node.js has not been installed. Go to the Node.js website and install for your system before trying again.
Run npm install @tensorflow/tfjs-node to install and save TensorFlow.js as a dependency for the project.
If you have any difficulty, you could install the pure JavaScript package: npm install @tensorflow/tfjs
Create a new JavaScript file named index.js with the following contents:
console.log("Hello World!");
Run node index.js to run the script. It should print "Hello World!". This simply confirms that you are able to run the script with Node.js.
Now update the file to the following:
const tf = require('@tensorflow/tfjs-node');
 
console.log("TensorFlow.js version information: ");
console.log(tf.version);
 
console.log(`TensorFlow.js backend: ${tf.getBackend()}`);
Run the script again with node index.js. You should see output similar to this:
TensorFlow.js version information:
{ 'tfjs-core': '1.0.1',
  'tfjs-data': '1.0.1',
  'tfjs-layers': '1.0.1',
  'tfjs-converter': '1.0.1',
  tfjs: '1.0.1',
  'tfjs-node': '1.0.1' }
TensorFlow.js backend: tensorflow
If you have problems running this, it may be related to the TensorFlow native bindings. Change the require statement to use the pure JavaScript package: const tf = require('@tensorflow/tfjs');. Run the command again and you will see that the backend is no longer tensorflow but cpu.
You can also copy and paste the sample code from the official TensorFlow.js setup page into your script and re-run it. You should see output related to training a machine learning model. Don't worry about what the code means: we'll cover the TensorFlow.js APIs later in this course!

## Kørselvejledning

[Instrukser til hvordan man kører opgaverne]