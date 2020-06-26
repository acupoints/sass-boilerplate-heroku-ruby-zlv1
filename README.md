# Generate sample files

```bash
# sass-boilerplate parent-dir
rm -rf normalize.scss/
git clone https://github.com/kristerkari/normalize.scss.git
# sass-boilerplate dir
compass create --bare --sass-dir "sass" --css-dir "css" --javascripts-dir "js" --images-dir "img"

mkdir img js css; touch index.html js/main.js js/plugin.js

mkdir sass/partials; touch sass/styles.scss sass/partials/_variables.scss
cp ../normalize.scss/_normalize.scss sass/partials/

echo // Declare a few sample variables > sass/partials/_variables.scss
echo \$color1: \#ff0000\; // Red >> sass/partials/_variables.scss
echo \$color2: \#ffbf00\; // Orange >> sass/partials/_variables.scss
echo \$color3: \#ffff00\; // Yellow >> sass/partials/_variables.scss
echo \$color4: \#7fff00\; // Green >> sass/partials/_variables.scss
echo \$color5: \#007fff\; // Light Blue >> sass/partials/_variables.scss
echo \$color6: \#00ffff\; // Cyan >> sass/partials/_variables.scss
echo \$color7: \#0000ff\; // Blue >> sass/partials/_variables.scss
echo \$color8: \#7f00ff\; // Purple >> sass/partials/_variables.scss
echo \$color9: \#ff00ff\; // magenta >> sass/partials/_variables.scss
echo \$color10: \#000\; // Black >> sass/partials/_variables.scss
echo \$color11: \#fff\; // White >> sass/partials/_variables.scss

echo @import \"compass\"\; > sass/styles.scss
echo @import \"./partials/variables\"\; >> sass/styles.scss
echo // Import your module here >> sass/styles.scss
echo >> sass/styles.scss
echo //@import \"./partials/normalize\"\; >> sass/styles.scss
echo // Organize your code here >> sass/styles.scss

```