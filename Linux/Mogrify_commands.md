# Mogrify

### Resize all similar format images in a folder
```
mogrify -resize 112x112! needs_resize/*.jpg
```
### find Resize all similar format images in a folder
```
find . -name '*.jpg' -exec mogrify -resize 112x112\> {} \;
```
### Convert jpg image to png
```
mogrify -format jpg *.png 
``` 