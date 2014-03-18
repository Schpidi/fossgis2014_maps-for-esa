# Maps for ESA

Presentation for FOSSGIS 2014 in Berlin.

## Running presentation

Point your browser to the [online 
presentation](http://schpidi.github.io/fossgis2014_maps-for-esa) or serve 
locally.

```bash
git clone git@github.com:Schpidi/fossgis2014_maps-for-esa.git
cd fossgis2014_maps-for-esa
npm install
grunt serve
```

## Creating presentation

After creating a new repository at GitHub run the following.

```bash
git clone git@github.com:Schpidi/fossgis2014_maps-for-esa.git
git branch -m master gh-pages
git submodule add https://github.com/Schpidi/reveal.js.git
cd reveal.js/
git checkout eox_box
git pull origin eox_box
cd ..
git add reveal.js/

ln -s reveal.js/Gruntfile.js Gruntfile.js
ln -s reveal.js/package.json package.json
npm install

echo "node_modules/" >> .gitignore
git add Gruntfile.js package.json .gitignore
git commit -m "Adding reveal.js."

cp reveal.js/index.html .
# Edit index.html to your liking
git commit index.html "Adding presentation."
```
