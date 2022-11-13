---
layout: post
title:  "웹 개발 무경험자가 깃헙 블로그 만든 썰 푼다.txt"
author: juyeop
categories: [ ETC ]
image: assets/images/22-10-09/thumbnail.jpg
tags: [ featured ]
---

취업을 하기 전에는
<a href="https://blog.naver.com/kjy13299" target="_blank">네이버</a>, 
<a href="https://juyeop.tistory.com" target="_blank">티스토리</a>에서 일상, 기술 관련으로 블로그 운영을 꽤 열심히 했었다.
하지만 취업 후에는 블로그 운영에 완전히 손을 땠었는데 그게 벌써 1년이 지났다.  

회사를 다니면서 많은 것을 배우고 경험했었는데 이를 막상 글로 정리하지 않으니
머리 속에서 점점 잊혀져갔고 이대로는 안되겠다 싶어서 깃헙 블로그를 제작하기로 했다.
(미루고 또 미루다가 드디어 시작한다.... 그래도 올해 안에는 시작해서 다행일지도 😏)

### Why 깃헙 블로그?
![plant-grass]({{ site.baseurl }}/assets/images/22-10-09/plant-grass.jpg)

깃헙 블로그를 선택한 가장 큰 이유는 잔디를 심기 위해서다ㅋㅋㅋ
회사에서는 깃헙 대신 깃랩을 사용해서 깃헙 관리에 많이 소홀했고 잔디도 역시 텅 비게 되었다.
(2022년이 다 끝나가는데 잔디의 상태가 참.... 🤦🏻‍♂️)

![github-grass]({{ site.baseurl }}/assets/images/22-10-09/github-grass.jpg)

또 다른 이유가 있다면 깃헙이 역시 다른 플랫폼보다 커스텀마이징이 훨씬 자유롭기 때문이다.
테마, 플러그인, 액션 등 다양하게 커스텀을 해보고 싶었다.

### 자 드가자~
![lets-go]({{ site.baseurl }}/assets/images/22-10-09/lets-go.jpg)

고등학교 1학년 때부터 지금까지 AOS 개발만 쭉 진행한 나는 시작 전 솔직히 조금 쫄았다.
깃헙을 많이 사용해보지도 않았고 Web 관련으로는 다뤄본 적이 거의 없었기 때문이다.
해봐야 HTML을 조금 다룰 수 있는 수준이었다.
(주변에 Web 개발을 하는 친구들이 허구한날 yarn start 그리고 localhost를 외칠 때마다 나는 귀를 닫았다)

### 스타트는 레포 생성
![create-repository]({{ site.baseurl }}/assets/images/22-10-09/create-repository.jpg)

가장 먼저 깃헙 레포지토리를 만들어야 한다.
해당 레포의 이름은 꼭 자신의 깃헙 ID 뒤에 .github.io를 붙인 이름이 되어야 한다.
나 같은 경우에는 깃헙 ID가 juyeop03이므로 juyeop03.github.io가 되겠다.

### 세컨드는 Jekyll 설정
지킬은 나 같은 Web 개발 초보자들이 홈페이지 제작을 손 쉽게 할 수 있도록 도와주는 엄청난 친구이다.
우리는 이를 활용해서 블로그의 기본 틀을 제작할 것이다.  

![jekyll-love]({{ site.baseurl }}/assets/images/22-10-09/jekyll-love.jpg)

지킬을 활용하기 위해 우선 로컬에 지킬을 설치해주자.
터미널에 아래 명령어를 실행하면 된다.

```
$ gem install jekyll bundler
```

만약 아래 명령어를 실행 했는데 오류가 난다면 현재 로컬에 Ruby가 설치되어 있지 않을 확률이 높다.
우리는 Ruby의 gem 명령어를 사용해서 지킬을 설치하기 때문에 먼저 Ruby가 설치되어 있어야 한다.
Ruby를 설치하는 방법은 <a href="https://jetalog.net/85" target="_blank">해당 블로그</a>에 정리가 잘 되어 있으므로 참고 바란다.

지킬 설치를 마쳤다면 이제 우리가 앞서 생성했던 레포지토리에 지킬을 활용하여 블로그의 기본 틀을 제작해야 한다.
로컬에서 레포지토리가 다운로드 된 디렉토리로 이동한 후 아래 명령어를 실행한다.

```
$ jekyll new ./
$ bundle install
```

그러면 아래와 같이 디렉토리 안에 베이스 코드들이 자동으로 추가된다.
지킬이 이렇게 베이스 코드를 제공해주므로 우리는 블로그 제작에 있어 많은 시간을 단축하게 된다.

![jekyll-install]({{ site.baseurl }}/assets/images/22-10-09/jekyll-install.jpg)

그리고 현 상태에서 아래 명령어를 실행하면 로컬에서 개발 서버가 열리게 되며 지킬이 제공해준 베이스 코드 기반의 블로그를 확인할 수 있다.
웹 사이트의 주소는 localhost:4000이다.
(나에게는 아직도 localhost가 많이 어색하다 😇)

```
$ bundle exec jekyll serve
```

![execute-localhost]({{ site.baseurl }}/assets/images/22-10-09/execute-localhost.jpg)

개발 서버를 실행 시키는 위 명령어는 블로그 제작 과정에서 많이 사용되므로 꼭 기억하기 바란다.
반대로 서버를 종료 시키고 싶다면 터미널에서 ctrl + c를 누르면 된다.

### Jekyll 구조 초간단 설명
![explain-jekyll]({{ site.baseurl }}/assets/images/22-10-09/explain-jekyll.jpg)

지킬을 활용하여 블로그를 제작한다면 지킬의 구조를 꼭 이해해야 한다.
먼저 _config.yml 파일은 AOS로 따지면 Manifest 파일과 비슷하며 메타 데이터를 보관하는 역할을 한다.
예를 들어 블로그 이름, 주소, 이메일과 같은 기본 정보들이 해당 파일에 포함된다.

![study-config]({{ site.baseurl }}/assets/images/22-10-09/study-config.jpg)

다음으로 _posts 디렉토리를 살펴보자.
우리는 블로그가 다 만들어지면 이제 당연히 글을 작성할 것이다.
글의 확장자는 마크다운이어야 하며 글의 저장 위치는 꼭 _posts 디렉토리 하위에 포함되어야 한다.
그래야만 지킬이 우리가 작성한 글들을 조회할 수 있다.

![study-posts]({{ site.baseurl }}/assets/images/22-10-09/study-posts.jpg)

또 한가지 중요한 점은 글의 파일명 역시 형식이 정해져 있다는 것이다.
위의 사진에서 볼 수 있듯이 현재 _posts 디렉토리 내에 샘플 글 하나가 있을 것이다.
해당 글의 파일명을 보면 `yyyy-MM-dd-제목` 형식이다.
이처럼 여러분들도 추후에 글을 작성할 때 꼭 해당 형식에 맞게 글의 파일명을 작명해야 한다.

### 고생했다, 우리 이제 이뻐지자
위에서 지금까지 진행한 과정만으로도 블로그 제작은 이미 끝이났다.
_posts 디렉토리 내에 글들을 작성하면 해당 글들이 블로그에 잘 노출되는 것을 확인할 수 있다.

![theme-help]({{ site.baseurl }}/assets/images/22-10-09/theme-help.jpg)

하지만 우리는 지금보다 더 이쁜 블로그를 만들고 싶다.
만약 자신이 Web 개발의 경험이 있다면 HTML, CSS 등을 직접 수정해서 블로그를 꾸미면 된다.
하지만 나 같이 Web 초보들은 그러지 못하기 때문에 오픈 소스의 힘을 빌리고자 한다.

우리에겐 오픈 소스의 성지인 깃헙이 있다.
먼저 jekyll-theme를 검색한다.
그러면 지킬을 활용해서 만든 수많은 깃헙 블로그들이 나오게 되며 이 중에서 우리는 자신이 원하는 테마의 블로그를 선택하면 된다.
(선택한 레포에 스타를 누르는 것을 잊지마라 😉)

![github-jekyll-theme]({{ site.baseurl }}/assets/images/22-10-09/github-jekyll-theme.jpg)

이제 선택한 테마를 우리 블로그에 적용 시켜보자.
먼저 테마를 다운로드 해야 한다.
그 후 다운로드 받은 테마들을 로컬에 있는 우리 블로그의 디렉토리에 모두 붙여 넣는다.
이 과정에서 중복 파일이 꼭 생길텐데 그때는 당황하지 말고 새로운 파일로 기존 파일을 대치하면 된다.

![replace-file]({{ site.baseurl }}/assets/images/22-10-09/replace-file.jpg)

깃헙에서 다운로드 받은 테마 역시 지킬을 기반으로 만들어졌기 때문에 로컬에서 개발서버를 실행한 후 접속하면 블로그에 테마가 적용된 것을 볼 수 있다.
(나는 wowthemesnet 개발자 분께서 제작하신 <a href="https://github.com/wowthemesnet/mundana-theme-jekyll" target="_blank">mundana-theme</a>를 사용했다)

![sample-blog]({{ site.baseurl }}/assets/images/22-10-09/sample-blog.jpg)

만약 블로그에 접속을 했는데 404가 뜨거나 오류가 난다면 _config.yml 파일의 baseurl이 빈 값으로 설정되어 있는지 확인해라.
config 파일 내 모든 값들은 테마를 제작한 개발자분의 정보로 설정되어 있기 때문에 이를 우리에 맞게 수정시켜야 한다.

![sample-baseurl]({{ site.baseurl }}/assets/images/22-10-09/sample-baseurl.jpg)

기본적인 테마 적용 방법은 이러나, 테마를 제작한 개발자분들마다 조금씩 적용법이 다를 수 있기 때문에 자신이 선택한 테마의 Readme를 꼭 한번씩 읽기 바란다.

### 이제 구글 켜, 친구 불러
![friend-help]({{ site.baseurl }}/assets/images/22-10-09/friend-help.jpg)

테마 적용도 완료했고 이제 막바지 단계이다.
config 파일 내 값들을 자신의 블로그에 맞게 설정하고 디자인적인 요소에서도 자신이 바꾸고 싶은 부분이 있다면 수정해라.
메인 컬러를 바꾸든, 신규 기능을 추가하든 자신이 원하는대로 자유롭게 진행하면 된다.

다만, 이 과정에서는 조금의 Web 개발 실력이 어쩔 수 없이 필요하다.
나는 구글링과 주변에 Web 개발을 하는 친구들에게 물어보며 블로그를 조금씩 수정했다.

---

![happy-day]({{ site.baseurl }}/assets/images/22-10-09/happy-day.jpg)

깃헙 블로그 제작의 난이도는 어렵지 않았으며 오랜만에 재밌는 경험을 했던 것 같다.
아직 검색 엔진 연동과 같이 손 봐야 할 것들이 꽤 있지만 시간이 날 때마다 조금씩 해볼 예정이다.

<b>블로그 제작 과정에서 도움이 된 문서</b>
- <a href="https://jetalog.net/86?category=808871" target="_blank">Jekyll을 이용해 GitHub에 블로그 만들기</a>
- <a href="https://velog.io/@dum6894/API-formsfree로-이메일-발송-기능을-추가하기" target="_blank">[API] formsfree로 이메일 발송 기능을 추가하기</a>
- <a href="https://ansohxxn.github.io/blog/utterances" target="_blank">[Github 블로그] utterances 으로 댓글 기능 만들기 (+ disqus 비추후기)</a>