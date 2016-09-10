+++

date = "2016-08-29T22:27:19+09:00"
draft = true
title = "First Post"

+++

# 1. HUGO Blog

  This is my first post about how do I build this hugo blog. I used to try to build a Hugo blog during January 2016 via [DigitalOcean.com](https://m.do.co/c/aabb124120d0) (CentOS 7) but there has some unexpected issues:
  
  - Unable access into console.
  - Mouse unable control the cursor in the virtual operating system.
  - Internet line always interrupted.
  - The theme [hugo-theme-air](https://github.com/syui/hugo-theme-air) is not complete and not workable.

  Today I am trying to continue build my hugo blog in Windows 10 as I occassionally saw the hugo-theme-air has maintaned and updated. You can read the reference to know about what is HUGO.
  
# 2. Build Hugo Blog in Windows 10

## 2.1 Create a Github Repo

  Firstly, you need to create a GitHub Pages at [GitHub](https://github.com). I just simply created mine as [englianhu.github.io](https://github.com/englianhu/englianhu.github.io) and then activate it. You are feel free to refer to [GitHub Pages](https://pages.github.com/) for further information.

  After that, I've just simply download as a ｮStudio project via [ｮStudio](http://www.rstudio.com) IDE. You are feel free to read [Setup ｮStudio Server on Digital Ocean --- CentOS 7](https://github.com/scibrokes/setup-rstudio-server) if you are using centOS 7 on DigitalOcean.com.

  Here is my path for the Hugo blog `> C:\Users\scibr\Documents\GitHub\englianhu\englianhu.github.io`.

## 2.2 Download Hugo Apps

  Secondly, you need to go to [spf13/hugo](https://github.com/spf13/hugo/releases) to download the latest (currently version 1.6 is the most updated version) version. Click [here](https://github.com/spf13/hugo/releases/download/v0.16/hugo_0.16_windows-64bit.zip) to download the HUGO server Windows 64 bit.
  
  Due to the Hugo.exe is a standalone app, therefore I just simply locate it at `> C:\Users\scibr\Documents\GitHub\englianhu` and then move the folder `englianhu.github.io` to path `C:\Users\scibr\Documents\GitHub\englianhu.github.io` to save the github relevant files. After that, I open *Shell* inside Tools in ｮStudio IDE menu bar (new session).
  
  Follow by run below codes to create a website:
  
```
> C:\Users\scibr\Documents\GitHub\englianhu>hugo new site englianhu.github.io
```
  
  After create a structure of the website, run below codes:

```
> C:\Users\scibr\Documents\GitHub\englianhu>cd englianhu.github.io\themes
> C:\Users\scibr\Documents\GitHub\englianhu\englianhu.github.io\themes>git clone https://github.com/spf13/hyde.git
```

  Remember the Hugo.exe is an standalone app and I move it to `C:\Users\scibr\Documents\GitHub\englianhu\englianhu.github.io\themes>` in order to run the app as below codes.

## 2.3 Browse via LocalHost Before Post

```
> C:\Users\scibr\Documents\GitHub\englianhu\englianhu.github.io\themes>hugo server --theme=hugo-theme-air --buildDrafts --watch
```
  
  Well, now we try to browse the [http://127.0.0.1:1313/](http://127.0.0.1:1313/) localhost.
  
![*figure 2.3.1 : Hugo blog layout*](figure/20160910_121813.gif)

## 2.4 Post to Hugo Blog

  When you modified your post content and decide to post on your blog. Now you just run below codes and a folder `public` will be created.

```
> C:\Users\scibr\Documents\GitHub\englianhu\englianhu.github.io>hugo
> C:\Users\scibr\Documents\GitHub\englianhu\englianhu.github.io>cd public
> C:\Users\scibr\Documents\GitHub\englianhu\englianhu.github.io>git add -A && git commit -m "first post"
> C:\Users\scibr\Documents\GitHub\englianhu\englianhu.github.io>git push origin master
> C:\Users\scibr\Documents\GitHub\englianhu\englianhu.github.io>cd ..
> C:\Users\scibr\Documents\GitHub\englianhu\englianhu.github.io>git add -A && git commit -m "init hugo coder"
> C:\Users\scibr\Documents\GitHub\englianhu\englianhu.github.io>git push origin master
```

  The files will upload to github repo and your blog and 1st post has been successful.

# 3. Conclusion

  It is very simple to build a hugo blog. You might try to build yours.

# 4. Reference

1. [使用hugo搭建个人博客站点](http://blog.coderzh.com/2015/08/29/hugo/)
2. [利用 Hugo & GitHub 搭建个人博客静态网站](http://blog.bpcoder.com/2015/12/hugo-create-blog/)

