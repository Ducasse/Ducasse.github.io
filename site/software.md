{
"title" : "Software",
"layout" : "index",
"publishDate" : "2025-06-01"
}

I like to code (in Pharo) and this helps me learn new things, get feedback on dev, and generate ideas for my research.
Here are the main software artefacts I'm developing or contributing too.
For more projects, have a look at [https://github.com/Ducasse](https://github.com/Ducasse).

## Pharo 

 Of course I'm contributing to Pharo. Cleaning and improving it a lot since day one!
More recently, I started to work on the refactoring engine and I enjoy it. I'm also working on extensions for the great completion framework of Pharo written by G. Polito. [https://github.com/pharo-project/pharo](https://github.com/pharo-project/pharo)
 
## Pillar 

Pillar is a compilation chain architecture. It was originally a markup (for SmallWiki written by Lukas Renggli) with a syntax close 
to the original Ward Cunningham Wiki, then it became a document compilation chain and a markup thanks to Guillermo Polito, and now it is using as input documents written in Microdown. I enhance and maintain Pillar. Now we can test books :).
[https://github.com/pillar-markup/pillar](https://github.com/pillar-markup/pillar)

## Microdown 

I designed with K. Osterbye Microdown. 
Microdown is a superset and a subset of GitHub Markdown. Using it, we can write full books, slides, static website, and of course, Pharo doc and class comments. 
[https://github.com/pillar-markup/microdown](https://github.com/pillar-markup/microdown)

## Foliage 

Originally written by Norbert Hartl, Foliage a static web site renderer (the one rendering this website).
It was using Microdown as a input, converting them into Pillar documents. 
I released its version 2.0. With it Foliage is using Microdown all the way. I maintain and enhance Foliage. 
[https://github.com/Ducasse/Foliage](https://github.com/Ducasse/Foliage)

## Citezen 

Originally written by Roel Wuyts, and enhanced by Damien Pollet, Citezen is a library to parse and manipulate bib files. 
I enhance and maintin it because I used it to automatically generate my publication website.
[https://github.com/Ducasse/Citezen](https://github.com/Ducasse/Citezen)

## DLittle 

I was so fedup to try to parse Yaml (what a bad language - people should all follow Lisp and Scheme lectures). I do not buy the argument that because the industry uses it, it is good. Mass products often show the inverse. So I played and designed a simple extension of a lispish syntax to represent structured data. It smells a lot like an s-expr. And I use it to keep by book collection. [https://github.com/Ducasse/DLittle](https://github.com/Ducasse/DLittle)

```
(author : Aldiss / Brian 
  (serie : helliconia  
  	(title: Le printemps d''helliconia (read: no)  (style: SF) (price: 1))
  	(title: Helliconia, l''ete (read: no)  (style: SF) (price: 1))
 	(title: L''hiver d''helliconia (read: no)  (style: SF) (price: 1))
  (serie : books
    	(title: L''instant de l''eclipse (read: no)  (style: fantaisie) (price: 1))
```

## Cavrois: an organic window manager
With  Alexis Cnockaert, we developed an organic window manager that is now integrated to Pharo. 
With it you place your tools attached them creation strategies, and then your new tools get in the places you said. 


## ObjVlisp 

I wrote a on the reflective kernel of objVlisp (similar to the one of book Smalltalk-78 but with two classes) and I maintain its small implementation.  [ PDF ](https://books.pharo.org/booklet-ReflectiveCore/)
[https://github.com/Ducasse/ObjVLispSkeleton](https://github.com/Ducasse/ObjVLispSkeleton)

## Phsyche
I love Scheme so I wrote a limited not compliant, simple little Scheme implementation to show my son an interpreter. 
[ Physche PDF ](https://books.pharo.org/booklet-AMiniSchemeInPharo/)

## Moose 

Moose is a software analysis platform created by S. Demeyer and me back in 1997. I enhanced it and maintained up to  2012. 
I ported it to Pharo. Now, nice people are improving it and taking care of my baby. I thank them for that. [https://modularmoose.org](https://modularmoose.org)

