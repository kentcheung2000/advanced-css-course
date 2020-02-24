Install SCSS
npm install node-sass  --save-dev
npm install jquery  --save

Compile SCSS
npm run compile:sass

Install live-server
sudo npm install live-server -g

Run Live server
live-server

Emmet
.classname to producde <div class="classname></div>
section.sectionname to produce <section class="sectioname"></section>

Emmet
.composition>(img.composition__photo.composition__photo--p1)*3
produce
 <div class="composition">
  <img src="" alt="" class="composition__photo composition__photo--p1">
  <img src="" alt="" class="composition__photo composition__photo--p1">
  <img src="" alt="" class="composition__photo composition__photo--p1">
</div>

.row>.col-1-of-4>.feature-box
produce
<div class="row">
  <div class="col-1-of-4">
    <div class="feature-box"></div>
  </div>
</div>

ul>li*3
produce
<ul>
  <li>3 day tours</li>
  <li>Up to 30 people</li>
  <li>2 tour guides</li>
  <li>Sleep in cozy hotels</li>
  <li>Difficult: easy</li>
</ul>


Build sass
1)
Json file
 "watch:sass": "node-sass sass/main.scss css/style.css -w",
 "compile:sass": "node-sass sass/main.scss css/style.comp.css"

2)
npm run compile:sass

3)
npm install concat --save-dev

4)
concat -o output.css ./1.css ./2.css ./3.css

5)
"scripts": {
    "watch:sass": "node-sass sass/main.scss css/style.css -w",
    "compile:sass": "node-sass sass/main.scss css/style.comp.css",
    "concat:css": "concat -o css/style.concat.css css/icon-font.css css/style.comp.css" 
},

6)
npm run concat:css

7)
npm install autoprefixer --save-dev

8)
npm install postcss-cli --save-dev

9)
"scripts": {
    "watch:sass": "node-sass sass/main.scss css/style.css -w",
    "compile:sass": "node-sass sass/main.scss css/style.comp.css",
    "concat:css": "concat -o css/style.concat.css css/icon-font.css css/style.comp.css",
    "prefix:css": "postcss --use autoprefixer -b 'last 10 versions' css/style.concat.css -o css/style.prefix.css"
},

10)
npm run prefix:css

11)
"scripts": {
    "watch:sass": "node-sass sass/main.scss css/style.css -w",
    "compile:sass": "node-sass sass/main.scss css/style.comp.css",
    "concat:css": "concat -o css/style.concat.css css/icon-font.css css/style.comp.css",
    "prefix:css": "postcss --use autoprefixer -b 'last 10 versions' css/style.concat.css -o css/style.prefix.css",
    "compress:css": "node-sass css/style.prefix.css css/style.css --output-style compressed"
},

12)
npm run compress:css

13)
npm install npm-run-all --save-dev

14)
npm run build:css

15)
"scripts": {
    "watch:sass": "node-sass sass/main.scss css/style.css -w",
    "devserver": "live-server",
    "start": "npm-run-all --parallel devserver watch:sass",
    "compile:sass": "node-sass sass/main.scss css/style.comp.css",
    "concat:css": "concat -o css/style.concat.css css/icon-font.css css/style.comp.css",
    "prefix:css": "postcss --use autoprefixer -b 'last 10 versions' css/style.concat.css -o css/style.prefix.css",
    "compress:css": "node-sass css/style.prefix.css css/style.css --output-style compressed",
    "build:css": "npm-run-all compile:sass concat:css prefix:css compress:css"
},

16)
npm run start