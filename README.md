The site is in the site folder.
It generates the site at https://ducasse.github.io

The folder generated contains the static HTML produced by 

```
| p |
p := FOPublisher new. 
p baseUri: 'Ducasse.github.io'.
p sourcePath: '/Users/ducasse/Test2/MySite/Ducasse.github.io/site'.
p targetPath: '/Users/ducasse/Test2/MySite/Ducasse.github.io/generated'.
p publish.
```






