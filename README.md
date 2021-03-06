# Welcome to my blog
This blog is written in markdown and the html files generated by a custom Python based program. 
Below you can find instructions on how to use it for your own.
The live version is available at [https://jumpfifzero.github.io](https://jumpfifzero.github.io).

# Preparing the build
After cloning this repo and cd'ing into it, do the following:

Install stuff
```
sudo apt-get install python3-venv
python3 -m venv env
```

Activate the virtual environment. This is needed to locally install the python libraries.

```
source env/bin/activate
```

Install the necessary packages. You may see some errors but the setup will continue fine.
```
pip3 install -r requirements.txt
```

# Writing a post
Just create a file under _posts with your favorite text editor.

# Building a post
At the moment there is no command to build all posts. This needs to be done one by one:
```
python3 build.py _posts/<name_of_your_md_file>.md
```
This will generate an html version with a sluggified name in folder posts.

The index.html is not at the moment automatically updated.

# Preview a post
After build, use the following to preview.
```
python3 -m http.server
```

Open a browser on localhost/posts

# Publishing
If your blog is hosted on github in a repo called your_username.github.io you just need to `git commit` and `git push origin master`. 
Use the git commit/push to control what gets published.



Tiago Almeida 2016
