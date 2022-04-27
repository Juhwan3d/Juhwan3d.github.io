---
title: First Posting!
date: 2022-04-27
categories: [Private, blog]
tags: [study, test]
---

## 첫 블로그, 첫 포스팅

난 블로그를 만들어 본게 이번이 처음이다. <sub>(대학 입학할 때 개인 블로그 제출하라고 해서 급하게 만든 네이버 블로그를 제외하면)</sub> 당연히 jekyll, github page, markdown 등등 모두 처음 사용해본다. 심지어 HTML, CSS도 관련 지식이 없다.. 
그러다 보니 지금 사용중인 이 jekyll theme <sub>[_chirpy theme_](https://github.com/cotes2020/jekyll-theme-chirpy/)</sub>를 적용하는 것도 쉽지 않은 일이었다. <sub>꼬박 하루를 날렸다..</sub>
원래는 [Notion](https://www.notion.so/)으로 간단하게 만들려고 했었는데, Notion이 생각보다 너무 단순하고 쉬웠다. 그래서 좀 어려운 방식에 도전해 보고 싶어서 github page로 만들었다. 덕분에 [jekyll](https://jekyllrb.com/)도 설치하고, [WSL](https://docs.microsoft.com/en-us/windows/wsl/)로 ruby, rubygem, bundler 등등 설치하는 재미가 있었다.
테마를 적용하는 과정에선 생각보다 어려움이 많았는데, 다른 것들은 구글링으로 자료를 찾을 수 있었지만, 왼쪽 하단의 social link를 커스텀하는 방법은 도저히 찾을 수 없었다. 기본 테마 설정은 github, twitter, email, rss 이렇게 4가지인데, 난 twitter를 하지 않고, instagram, artstation 등의 링크를 넣고 싶었다. 다행히 chirpy theme에서 사용 중인 font awesome의 버전이 instagram, artstation의 아이콘을 모두 포함하고 있는 버전이라 아이콘을 추가하는 일은 어렵지 않았다. '/_data/contact.yml'{: .filepath}에 접근해서 아래와 같은 코드를 삽입해주기만 하면 됐다.

-
  type: instagram
  icon: 'fab fa-instagram'
-
  type: artstation
  icon: 'fab fa-artstation'

간단하게 icon을 추가해서 이제 링크만 연결하면 되겠다! 했는데, 이게 쉽지 않은 일이었다. '/_config.yml'{: .filepath}의 social 부분을 아무리 수정해도 변함이 없었고, '/_site/index.html'{: .filepath}의 350번 줄 즈음에 사이드바 버튼 부분에 아무리 링크를 추가해도 빌드 때마다 초기화 되었다. 그렇게 포기하려고 할 때 즈음 '/_includes/sidebar.html'{: filepath} 파일이 눈에 띄었다. 누가봐도 사이드바에 관련된 파일명. 설레는 마음으로 파일을 열었을 땐 contact 엔트리 목록이 날 반겼다... 엔트리 목록에 원하는 사이트 타입과 주소를 넣고 빌드 후 확인 해보니 정상적으로 동작했다..! 진짜 너무 짜릿한 순간이었다.

아무튼 그렇게 해서 블로그 초기 설정이 대충 마무리 됐다. 사실 포스트도 영어로 깔끔하게 쓰고 싶었는데 영어로 글을 쓰는 재주는 없어서 포기했다.. 사실 markdown으로 글 작성 하는 것도 아직 버겁다.

## 앞으로 계획

이 블로그를 다른 사람이 볼지는 모르겠지만, 앞으로 포스팅 계획을 세워보려고 한다. 우선, 모델링 작업물들을 작업 과정과 어려웠던 점 등을 정리해서 올려볼 생각이다. 추가로 언리얼이나 c++같은 공부도 하게 된다면 공부 기록도 할 생각이다. 블로그를 개설한 이유가 재밌을거 같아서도 있지만, 공부 기록을 정리하려는 목적도 있었기 때문에, 기록하는 형식으로 포스팅 하려고 한다.


markdown으로 처음 써보는 글이라 잘 써졌을 지 모르겠다. 지금은 vscode로 쓰는 중인데, 블로그에 푸시해보고 엄청 수정해야 할 것 같다ㅎㅎ;