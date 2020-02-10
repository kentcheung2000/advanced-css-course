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