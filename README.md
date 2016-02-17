# AlbumDownload
Javascript image album download


// basic example for download image album from website
// eg  http://www.letsplan.in/best-indian-wedding-themes/
// past this code in console and allow images will be downloaded

```
function downloadURI(uri) 
{
    var link = document.createElement("a");
    link.download = uri.substring(url.lastIndexOf('/')+1);
    link.href = uri;
    link.click();
}
```
```
function checkImagePath(){
  var domains = document.getElementsByClassName('landscape');
  var imagesCount = 0;
  for(var i = 0; i < domains.length; i++){
      var anchors = domains[i].getElementsByTagName('a');
    for (var j = 0; j < anchors.length; j++) {
          console.log(anchors[j].href);
          imagesCount ++;
      }
  }
  console.log("Total Images:"+imagesCount);
}
```

```
function downloadYourImages(){
  var domains = document.getElementsByClassName('landscape');
  for(var i = 0; i < domains.length; i++){
      var anchors = domains[i].getElementsByTagName('a');
    for (var j = 0; j < anchors.length; j++) {
          downloadURI(anchors[j].href);
      }
  }   
}
```

// after adding this command use 
// checkImagePath(); and check image path
// if that return correct path then write
// downloadYourImages();
// enjoy download image gallary
