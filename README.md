# Installing

```
npm i -g imgfy
```

[![NPM](https://nodei.co/npm/imgfy.png?downloads=true&downloadRank=true&stars=true)](https://nodei.co/npm/imgfy/)

# Usage: imgfy [options]

  Options:

    -h, --help               output usage information
    -o, --open               Open url in browser
    -c, --content <content>  Content file dir

# Demo proposal:

## content.json's content:
```
{
  "template": {
    "backgroundImage": "url(http://res.cloudinary.com/cagatayc/image/upload/profile.jpg)",
    "backgroundColor": "#cccccc",
    "backgroundRepeat": "no-repeat"
  },
  "images": [
    {
      "id": 1,
      "src": "http://res.cloudinary.com/cagatayc/image/upload/racoon.png",
      "property": {
        "position": "absolute",
        "top": "152px",
        "left": "122px",
        "maxHeight": "37px"
      }
    },
    {
      "id": 2,
      "src": "http://res.cloudinary.com/cagatayc/image/upload/racoon.png",
      "property": {
        "position": "absolute",
        "top": "141px",
        "left": "210px",
        "maxHeight": "37px"
      }
    }
  ]
}
```

```
imgfy -c content.json -o
```

## Output: (My eyes looking with love, Please dont afraid )
![imgfy demo image](demo.png)

# Programmatically.

## File system example:

```
var app = require('./index');

var file = 'content.json'; // YOUR AWESOME CONTENT!
var open = true;

app(null, file, open)
  .then((value) => {
    console.log(value);
  })
  .catch((err) => {
    console.log(err);
  })


```

## Direct content example:

```
var app = require('imgfy');

var content = {

}

app(content, false, true) // Open in browser.
  .then((value) => {
    console.log(value);
  })
  .catch((err) => {
    console.log(err);
  })

```

Maintenance & Development [Çağatay Çalı](http://github.com/cagataycali)

Made with :heart:
