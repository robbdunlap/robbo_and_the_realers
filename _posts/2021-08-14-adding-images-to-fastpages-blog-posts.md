# Adding a Photo to a Fastpages Blog Post

I was confused by Fastpages' instruction on <a href="https://fastpages.fast.ai/fastpages/jupyter/2020/02/21/introducing-fastpages.html#Images-w/Captions">how to add a photo to a post</a>. This is how I do it when writing a post in markdown:

1. Add the image to the "/images/" folder in your fastpages blog directory and push the file to GitHub (note - don't put the image in the "/copies_from_nb/" subfolder within the "/images/" folder)
2. Navigate to the blog images folder on GitHub and open the image
3. Right-click on the image and select "copy image address"
4. Insert the image address into the blog post using either markdown or html syntax:<br>
<br>
<br>

Markdown style
```markdown
![image](https://github.com/robbdunlap/robbo_and_the_realers/blob/master/images/uaf.png?raw=true)
```

<br>
<br>

HTML style
```html
<img src="https://github.com/robbdunlap/robbo_and_the_realers/blob/master/images/uaf.png?raw=true)">
```

<br>
<br>

Interstingly, if you paste the link to the image in a browser window then it will convert the link slightly when the image displays. You can also use the resultant html address to display the image in a post.

