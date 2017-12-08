# MarkdownBlog

A static makrdown blog system that allow you to build your own blog with [Github Pages](https://pages.github.com/)  
Unlike Jekll or Hexo, MarkdownBlog don't need the Nodejs to compile.  
**To be short** : 
1. put your markdown file into '/static/data/article' folder
2. register your file in the '/static/data/article_info.json
Then is all done.

## How to use
1. Fork this lib to your own repo
2. Go to Settings change the repository name to 'your-name.github.io'
3. Then go to https://your-name.github.io, you will see the template (if not please wait for a minute)

## Configration
config file is in '/static/config/config.json', currently there are only a few options (I will add more trust me).
- page_title: string, this will be the title for the page
- enable_resume: boolean, set true if you want the resume link show on the top right, otherwise false
- nav_text: length 3 array, this is the text of the link in the top right (if 'enable_resume' set to false, second value will be ignore)
- me_animation: boolean, set true if you want the little plane animation to show in the 'me' page
- me_image: string, this option only works when you set the 'me_animation' to false, then it will use the image-file you put here
- me_text: string, this the the text you can put to replace 'Hello' in the 'me' page

## What then
After setting your configration (of course you can use defualt), then you can blogging la~
Go to '/static/data/', thats all you need to manage, only this folder.
1. put your markdown file (.md) into the 'article' folder (you can also create sub-folder under 'article')
2. regist your file in 'article_info.json', this is the confusing part (if you know json will be easy for you)
  - filename: your markdown file name end with '.md'
  - title: the article title you wanna show in the very top of that article (will be h1)
  - type: one article can belong to one type only, one type can have multiple aritlces, this will show inthe left side bar for guidence
  - data: the date you write the article, this will show at the top rigth of the artilce
  - **Put all these info as "key":"value" pair seperated by comma ',' into a curly braket '{}', then put it into the article array also sperated by comma ','** Then it's all set!
e.g you have two articles, the registration file will be something like this.
```json
{
    "articles": [
        {
            "filename": "class/my_first_article.md",
            "title": "My first article",
            "type" : "Class1",
            "date": "1970-01-01"
        },
        
        {
            "filename": "class/my_second_article.md",
            "title": "My Second article",
            "type" : "Class2",
            "date": "1970-01-03"
        }
    ]
}
```
## Tips
#### How to add image.
Put all you image into the '/static/data/img/' folder, then anywhere if you wanna use the image, just using the filename.
- If you wanna add image into the markdown file, there are two ways
  1. Using the outside image then \[\](image-src-url)
  2. Put your image into the img folder then include uisng \[\](image-file-name.jpb)

 




