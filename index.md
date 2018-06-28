---
layout: default
use_math: true
---

# Git 사용법 - 작성자의 능력의 한계로 기본 사용법만 알려 드립니다.
## git 설치
### 우분투의 경우
터미널 창을 열고 sudo apt-get install git을 입력 한 후 엔터를 치면 됩니다.

### 윈도우의 경우
아래 링크로 가서 설치 파일을 다운 받은 후 실행하면 됩니다.
[https://www.git-scm.com/](https://www.git-scm.com/)

## 주요 명령어 모음
### git init
git init은 저장소를 초기화 하는 명령어로 원하는 workspace에 들어간 후 git init 명령을 실행하면 해당 폴더에 .git이라는 숨겨진 폴더가 생성 되며 해당 폴더의 버전 관리를 하게 됩니다.

### git status
git status는 현재 작업한 내용을 조회 할수 있는 명령어로 git으로 관리되는 프로젝트안의 파일의 변경/삭제 이력을 보여 줍니다.

### git add
작업한 폴더의 작업 내용을 추가 하는 명령어로 본래 사용법은 **git add [작업한 파일 명]** 입니다. 귀찮으면 **git add .** 으로 하면 됩니다. .의 의미는 폴더에 있는 모든 파일을 add 한다는 의미입니다.

### git commit
git commit은 add한 작업 내용의 설명을 입히는 작업입니다. 사용은 **git commit -m "내용설명"** 으로 하면됩니다.

### git push
git push는 작업한 내용을 github로 업뎃하는 명령입니다.

### github 올리는 순서
로컬에서 작업한 내용을 github 저장소로 업데이트를 하려면 다음과 같은 순서로 해야 정상적으로 반영이 됩니다.
**파일 작성 후 저장->git add.->git commit->git push**

### 이외에 추가적으로 알아야(정리해야 할) 명령어 : git branch, git checkout 등등

# Formula Redeging Test

## $$ \overrightarrow V = [v_1, v_2, v_3 \ldots v_n], v \in R^m $$

# Header 1

This is a normal paragraph following a header. GitHub is a code hosting platform for version control and collaboration. It lets you and others work together on projects from anywhere.

## Header 2

> This is a blockquote following a header.
>
> When something is important enough, you do it even if the odds are not in your favor.

### Header 3

```js
// Javascript code with syntax highlighting.
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
```

```ruby
# Ruby code with syntax highlighting
GitHubPages::Dependencies.gems.each do |gem, version|
  s.add_dependency(gem, "= #{version}")
end
```

#### Header 4

*   This is an unordered list following a header.
*   This is an unordered list following a header.
*   This is an unordered list following a header.

##### Header 5

1.  This is an ordered list following a header.
2.  This is an ordered list following a header.
3.  This is an ordered list following a header.

###### Header 6

| head1        | head two          | three |
|:-------------|:------------------|:------|
| ok           | good swedish fish | nice  |
| out of stock | good and plenty   | nice  |
| ok           | good `oreos`      | hmm   |
| ok           | good `zoute` drop | yumm  |

### There's a horizontal rule below this.

* * *

### Here is an unordered list:

*   Item foo
*   Item bar
*   Item baz
*   Item zip

### And an ordered list:

1.  Item one
1.  Item two
1.  Item three
1.  Item four

### And a nested list:

- level 1 item
  - level 2 item
  - level 2 item
    - level 3 item
    - level 3 item
- level 1 item
  - level 2 item
  - level 2 item
  - level 2 item
- level 1 item
  - level 2 item
  - level 2 item
- level 1 item

### Small image

![Octocat](https://assets-cdn.github.com/images/icons/emoji/octocat.png)

### Large image

![Branching](https://guides.github.com/activities/hello-world/branching.png)


### Definition lists can be used with HTML syntax.

<dl>
<dt>Name</dt>
<dd>Godzilla</dd>
<dt>Born</dt>
<dd>1952</dd>
<dt>Birthplace</dt>
<dd>Japan</dd>
<dt>Color</dt>
<dd>Green</dd>
</dl>

```
Long, single-line code blocks should not wrap. They should horizontally scroll if they are too long. This line should be long enough to demonstrate this.
```

```
The final element.
```
