---
layout: page
title: Running the Fastai Course on my Local Machine
permalink: 
---

I was working through the first few chapters of the <a href='https://course.fast.ai/'>Fast.ai Fastbook course</a> using the recommended free tier on <a href='https://www.paperspace.com/'>paperspace</a>. It worked well well except it was usually about 5-10 minutes before a virtual machine was available and I frequently got dropped 30-60 minutes after getting access. It wasn't a big deal but it usually meant a 10-15 min pause before I could get back to work. The course recommends using  preconfigured PAAS solutions instead running locally because of the difficulty setting up your environment, which can be a real pain. Alas, curiosity got the best of me, I really wanted to try to run the fastai package on my local machine. 

I have an Intel 7th gen Core I5 with 32 GB of memory, a 1 TB SSD, and an Nvidia GTX1060 GPU with 3 GB of memory. Not a stellar machine but good enough to support my learning path. I read a number of articles and posts for configuring my Anaconda environment to run fastai locally. The best post was one I found was on the fast.ai forums by <a href='https://forums.fast.ai/t/missing-graphviz-please-run-conda-install-fastbook/77260/3?u=robbdunlap'>heraldb</a>. The solution worked perfectly for me. The essense of the post is:

1 - Make sure your Conda is up-to-date

    $ conda update -n base conda

2 - Create a new Conda environment (environments tab of Anaconda -> click on the "create" icon at the bottom of the page)

3 - Open a terminal in your Anaconda environment - this <a href='https://stackoverflow.com/a/45197778/11041785'>SO</a> post has a good description if this is new to you 

3 - Install the appropriate packages in this order
    
    $ conda install -c fastai -c pytorch fastai
    $ conda install -c fastai fastbook

This worked perfectly for me. My machine is about half as fast as the VM I was using on Paperspace. We'll see if that's acceptable later on as the model building process gets more resource intensive. 
