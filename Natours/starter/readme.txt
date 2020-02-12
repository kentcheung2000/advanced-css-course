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