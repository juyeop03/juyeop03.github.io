---
layout: post
title: "A person without experienced in web development tells a story about made a github blog.txt"
author: juyeop
categories: [ ETC ]
image: assets/images/22-10-30/thumnail.jpg
tags: []
---

Before get a job I managed blog hardly in
<a href="https://blog.naver.com/kjy13299" target="_blank">naver</a>, 
<a href="https://juyeop.tistory.com" target="_blank">tistory</a> about daily life and technology.
However after get a job I completely let go of manage blog.
That is already passed 1 year.

I leanred so many things while working at the company.
But I don't organized about it to article then it was more and more forgotten from my head.
(Postpone and postpone I'm starting finally.... But it is relief to start before next year 😏)

### Why github blog?
![plant-grass]({{ site.baseurl }}/assets/images/22-10-09/plant-grass.jpg)

The main reason to selected github blog is to plant grass hahaha.
At company I used gitlab instead of github, so managed github is negligent and my grass was also empty.
(2022 year is coming to end but my grass state was oops.... 🤦🏻‍♂️)

![github-grass]({{ site.baseurl }}/assets/images/22-10-09/github-grass.jpg)

Another reason to selected github blog is able to customizing freely than other platform.
I want to customizing variously like theme, plugin, action etc.

### Let's start~
![lets-go]({{ site.baseurl }}/assets/images/22-10-09/lets-go.jpg)

Before start I was little scared because I developed only AOS from first grade of high school until now.
I don't used github many times and I don't developed web almost.
As much as possible I can develop only html.
(While my around of friends who develop web, they said yarn start and localhost everyday then I closed my ears)

### Start is create repository
![create-repository]({{ site.baseurl }}/assets/images/22-10-09/create-repository.jpg)

First we should make github repository.
This repository name must to be add .github.io after your github id.
In my case, my github id was juyeop03 then my repository name must to be juyeop03.github.io.

### Second is setting jekyll
Jetkyll is amazing friend that help like me who web development beginner people can to develop homepage easily.
We used it and develop based of blog.

![jekyll-love]({{ site.baseurl }}/assets/images/22-10-09/jekyll-love.jpg)

To used jekyll first we should to install jekyll in local.
Do execute below command in terminal.

```
$ gem install jekyll bundler
```

If error occur when execute command then ruby was not installed in your local, probability highly.
Because of we install jekyll by use ruby's gem command then we should to install ruby first.
Method of install ruby is well written in this 
<a href="https://jetalog.net/85" target="_blank">blog</a>, reference this.

If you finished install jekyll, we should develop base of blog in repository with use jekyll.
Move to repository in local and execute below command.

```
$ jekyll new ./
$ bundle install
```

Then base code added automatically in directory like below.
Jekyll give base code to us then we save many times to develop blog.

![jekyll-install]({{ site.baseurl }}/assets/images/22-10-09/jekyll-install.jpg)

And execute below command then develop server is opened in local.
we can see blog of based code provided by jekyll.
Web site url is localhost:4000.
(localhost is awkward to me yet 😇)

```
$ bundle exec jekyll serve
```

![execute-localhost]({{ site.baseurl }}/assets/images/22-10-09/execute-localhost.jpg)

Surely remember above command that execute develop server becasue it is often used when develop blog.
On the contrary if you want to end server you can press ctrl + c in terminal.

### Explain jekyll strcture to so easily
![explain-jekyll]({{ site.baseurl }}/assets/images/22-10-09/explain-jekyll.jpg)

If you make blog use jekyll you must understand jekyll structure.
First _config.yml file role is save meta data like manifest file from aos.
Example basic information included in there like blog name, address, email.

![study-config]({{ site.baseurl }}/assets/images/22-10-09/study-config.jpg)

Next look the _posts directory.
Of course we going to write article when blog is developed finish.
Article extension must be markdown and that must save in _posts directory subordinate.
Only then jekyll can inquiry our article.

![study-posts]({{ site.baseurl }}/assets/images/22-10-09/study-posts.jpg)

Also one important thing is article file name have form.
You can see above photo there is one sample article in _posts directory.
That article file name form is `yyyy-MM-dd-title`.
Like this, later if we write article we must named that article file name like form.

### Go through a haridship, Let's get pretty
Develop blog is already finished by above process.
When you write article in _posts directory then that is show well in blog.

![theme-help]({{ site.baseurl }}/assets/images/22-10-09/theme-help.jpg)

But we want to develop more pretty blog then now.
If you have web development experience then you can decorate blog with modify HTML, CSS.
But web development beginner like me can't do it then we bring open source power.

We have a open source sacred place github.
First search jekyll-theme.
Then so many github blogs made with jekyll to be show then you can select theme of blog what you want.
(Don't forget press that repository star 😉)

![github-jekyll-theme]({{ site.baseurl }}/assets/images/22-10-09/github-jekyll-theme.jpg)

Try to apply what you selected theme in our blog.
First we should download theme.
After then copy what we download theme in our blog local directory.
In this process dupplicate file is creating mustly but we can replaced existing file to new file then don't embarrassed.

![replace-file]({{ site.baseurl }}/assets/images/22-10-09/replace-file.jpg)

Because of we downloaded theme in github that was also made based of jekyll then you execute develop server in local then you can see theme apply in blog.
(I used <a href="https://github.com/wowthemesnet/mundana-theme-jekyll" target="_blank">mundana-theme</a> made by wowthemesnet developer)

![sample-blog]({{ site.baseurl }}/assets/images/22-10-09/sample-blog.jpg)

If you enter blog but 404 or another error occur then check base url setting is empty in _config.yml file.
All of default value in config file was set by theme developer info then we should modify it to fit us.

![sample-baseurl]({{ site.baseurl }}/assets/images/22-10-09/sample-baseurl.jpg)

This is basic method of apply theme, but it can difference of theme developer then you should read readme what you selected theme.

### Now open google, call friends
![friend-help]({{ site.baseurl }}/assets/images/22-10-09/friend-help.jpg)

Apply theme is completed and it is finish stage.
Setting value in config file to fit you and if you want to change design element modify it.
You can change main color, add new feature anything do it what you want to freely.

But this process need little web development skill unwillingly.
I modified blog little by ask other web developer friends and search in google.

---

![happy-day]({{ site.baseurl }}/assets/images/22-10-09/happy-day.jpg)

Develop github blog is not difficult and I had funny experience after a long time.
I have some tasks yet like connect search engine but I will going to do it little when I have time.

<b>Helpful for develop blog</b>
- <a href="https://jetalog.net/86?category=808871" target="_blank">Develop github blog with jekyll</a>
- <a href="https://velog.io/@dum6894/API-formsfree로-이메일-발송-기능을-추가하기" target="_blank">[API] Add email send feature with formsfree</a>
- <a href="https://ansohxxn.github.io/blog/utterances" target="_blank">[Github Blog] Develop comment feature with utterances ( + disqus not recommended review)</a>