# cs416hw2 - Web Development: Homework Two

## Project Info:

## Project Structure:
<pre>
cs426hw2/
├── index.html
├── assets/
│   └── css/
│       └── style.css
│   └── images/
│       └── . . .
├── node_modules
│       └── . . .
├── scss
│   └── components/
│   └── sections/
│   └── _custom.scss
│   └── style.scss
└── HW2 Self Evaluation Form.docx
└── hw2-large.png
└── hw2-medium.png
└── hw2-small.png
└── index.html
└── package.json
└── package-lock.json
└── README.md
</pre>

## Dependencies:
1. SASS (previously DART-SASS)
   - https://sass-lang.com/dart-sass
2. BOOTSTRAP 5 
   - https://getbootstrap.com/docs/5.1/getting-started/introduction/
3. BOOTSTRAP ICONS 
   - https://icons.getbootstrap.com/
4. AUTOPREFIXER 
   - https://www.npmjs.com/package/sass-autoprefixer

Install with ```npm -i 'dependency'```

## SASS SETUP
1. Create project directory and initialize github repository
2. ```npm init``` and install dependencies
3. Create npm script to compile scss to css
   - in the format of "commandName":"instrucion"
   - so in this case "compile:sass": "sass --watch scss:assets/css"
   - this command will take sass files and compile them into assets/css
   - the watch flag makes changes to css file automatically  
   - to run command, enter ```npm run compile:sass``` in the terminal
   - you will see a source map file in assets/css, this is what tells the browser how to comsume CSS and how that CSS corresponds to SASS which generated it.
4. Create a custom sass file 
   - **Because it is not good practice to directly override bootstrap.scss files**
   - The custom sass file should be pre-pended with an underscore to indicate this file is a partial
   - a partial file will not be compiled into a css stylesheet. 
   - import standard bootstrap.scss file with ```@import"../node_modules/bootstrap/scss/bootstrap.scss";``` at the top of _custom.scss
   - now import _custom.scss in style.scss with ```@use "custom";```
   
## To Run Projet
1. clone or download code
2. run  ```npm run compile:sass``` from project directory to compile scss to css
3. open index.html in browser to see the results!