
From <https://roamgom.github.io/>

# Markdown 작성하기

## 마크다운이란?

Github, Github Pages에서 보는 README를 보면 모두 `.md` 또는 `.markdown` 파일명으로 써져 있는걸 알 수 있습니다. 주로 기술 블로그 포스팅이나 프로젝트에 대한 설명을 써놓는게 대부분인데 특수기호, 문자를 이용하여 매우 간단한 문법으로 웹에서 빠른 컨텐츠 작성이 가능하죠. ~~Github 덕분이라 할수도..~~

**Markdown** 은 2004년 존 그루버에 의해 만들어 졌고, 플랫폼 상관없이 모든 에디터에서 작성이 가능합니다. 개발자들 사이에서 많이 쓰이는 Sublime Text, Atom, VSCode 같은 좋은 도구도 많지만 저는 [**typora**](https://typora.io/) 를 적극! 추천합니다. (자세한 설명은 뒤에서 😀)

<br>



우선 장단점부터 설명하자면



> **장점**
>
> 1. 문법이 간결하다.
> 2. 텍스트 형태로 저장되기 때문에 용량이 적고 관리하기 용이하다.
> 3. 별도의 도구 없이 모든 에디터에서 작성가능하다.
> 4. 지원하는 프로그램과 플랫폼이 다양하다.



> **단점**
>
> 1. 표준이 지정되어 있지 않아 도구에 따라 변환방식이 달라 결과에 차이가 있다.
> 2. HTML의 모든 마크업을 표현하는데 부족하다.

<br>



Github에서 오픈소스를 찾다보면, `README.md` 의 내용은 우리가 매일보는 HTML 웹페이지로 보입니다.

<img src="/img_src/tensorflow.png">

_이렇게 보이죠_

'문서를 HTML로 작성했네?'라고 생각할 수 있지만, 창에 보이는 `Raw` 라는 버튼을 눌러보면

<img src="/img_src/tensorflow_md.png">

_생각한 것과 다르게 나오네요_ 🤔



이는 Github에서 마크다운으로 작성한 파일을 HTML로 자동 렌더링해주기 때문입니다.

이 덕분에 빠르게 Repository에 대한 문서와 블로그 글과 같은 게시물을 빠르게 작성할 수 있는겁니다.



이제, 마크다운 문법을 알아보도록 하죠.

<br>

<br>

## 마크다운 문법

#### 문단 구분

기본적으로 마크다운은 모든 문법에서 문단 사이의 빈줄(엔터 두번)으로 구분합니다.

```
문단 하나

문단 둘
```



<br>

<br>



#### 헤더(Headers)

헤더는 HTML에서 쓰는 `<h1>, <h2>, ..., <h6>` 와 같이 큰제목을 쓸 때 사용합니다.

> 큰제목 | 작은 제목

```
문서의 큰 제목입니다
=====================

문서의 작은 제목입니다
---------------------
```

문서의 큰 제목입니다
=====================

문서의 작은 제목입니다
---------------------



<br><br>



> 글머리

```
# H1 제목
## H2 제목
### H3 제목
#### H4 제목
##### H5 제목
###### H6 제목
```

# H1 제목

## H2 제목

### H3 제목

#### H4 제목

##### H5 제목

###### H6 제목

###### # H7은?



<br><br>



#### 문단

> 블럭인용구

```
> 블럭인용
>> 블럭 1
>>> - 내용 1-1
>>> - 내용 1-2
>> 블럭 2
>>> 내용 2-1
>>> 내용 2-2
```

> 블럭인용
> > 블럭 1
> >
> > > - 내용 1-1
> > > - 내용 1-2
> >
> > 블럭 2
> >
> > > 내용 2-1
> > >
> > > 내용 2-2



<br>

<br>



#### 강조

> 이탤릭체

```
*이탤릭체* 또는 _이탤릭체_
```

*이탤릭체*  또는 _이탤릭체_



> 굵은 글씨

```
**굵은 글씨** 또는 __굵은 글씨__ 아니면 ***굵은 이탤릭체***
```

**굵은 글씨** 또는 __굵은 글씨__ 아니면 ***굵은 이탤릭체***



> 밑줄

```
<u>밑줄</u>
```

<u>밑줄</u>



> 취소선

```
~~취소선~~
```

~~취소선~~



> 주석

```
한 부분[^1]에 주석을 달 수 있습니다.
예를 들면, 이렇게[^2] 말이죠.

---

[^1]: 어때요.
[^2]: 참 쉽죠?
```

한 부분[^1]에 주석을 달 수 있습니다.
예를 들면, 이렇게[^2]말이죠.

---

[^1]: 어때요
[^2]: 참 쉽죠?

※ 2018-02-12: Github README에서는 주석 처리가 잘 안되는 것 같네요. 자세한 결과는 [블로그](https://roamgom.github.io/)를 참고해 주세요.


<br><br>



#### 구분선

```
---
- - -
----------------
* * *
*****
***
가로선
```

---
- - -
----------------
* * *
*****
***
가로선



<br><br>



#### 목록

> 순서 목록(번호)

```
1. 첫번째 목록
2. 두번째 목록
3. 세번째 목록
```

1. 첫번째 목록
2. 두번째 목록
3. 세번째 목록

※ **기본 내림차순으로 작성됩니다**

<br>



> 순서 없는 목록(글머리)

```
* 목록
* 목록
	* 내용
	* 내용
		* 본문
			* 그 다음?
- 목록
- 목록
	- 내용
	- 내용
		- 본문
			- 그 다음?
* 목록
* 목록
	- 내용
		+ 본문
	- 내용
		+ 본문
```

* 목록
* 목록
	* 내용
	* 내용
		* 본문
			* 그 다음?


* 목록
* 목록
	- 내용
		+ 본문
	- 내용
		+ 본문



<br><br>



#### 코드

> 코드 문맥, 블럭

탭(Tab) 1개 또는 공백 4개를 사용합니다.

```
​```
여러개의
코드 문맥
​```
`파일명 블럭` 또는 `변수명 블럭`
```

```
여러개의
코드 문맥
```
`파일명 블럭` 또는 `변수명 블럭`



> 언어 별 코드

```
​```python
def hola():
    print("Hola!")
hola()
​```
```

```python
def hola():
    print("Hola!")
hola()
```


<br><br>



#### URL 링크

> 인라인(Inline) 링크

```
[Google 링크](https://google.com "구글로 이동")
```

[Google 링크](https://google.com)

> 자동링크

```
<https://roamgom.github.io/>
```

<https://roamgom.github.io/>



<br><br>



#### 이미지

> 이미지 링크

```
![이미지 설명](/경로/이미지.jpg)
```

<img src="/img_src/profile_image.jpg">



> 이미지 사이즈 조절

```
<img src="/경로/이미지.jpg" width="가로" height="세로">
```

<img src="/img_src/profile_image.jpg" width="30">



<br><br>



#### 표(테이블)

>  표 만들기

```
| 1 | 2 | 3 | 4 | 5 |
|---|---|---|---|---|
| a | b | c | d | e |
| f | g | h | i | j |
| k | l | m | n | o |
```

| 1    | 2    | 3    | 4    | 5    |
| ---- | ---- | ---- | ---- | ---- |
| a    | b    | c    | d    | e    |
| f    | g    | h    | i    | j    |
| k    | l    | m    | n    | o    |

테이블 생성하는데 시간이 많이 걸리네요.

[**이 사이트**](http://www.tablesgenerator.com/markdown_tables) 를 사용하면 쉽게 테이블을 생성할 수 있습니다 🤗



<br><br>

----



제가 알고 있는 마크다운 문법은 이렇게 정리되네요. ~~상당하쥬?~~

양은 많아 보이지만 막상 사용하다보면 충분히 적응할 수 있을거에요.



자신이 배운 내용, 프로젝트에 대한 설명은 이제 마크다운 하나로 해결할 수 있습니다!!

...

<br>



아, 앞서 추천한 [**typora**](https://typora.io/) 에 대해 소개를 잊을뻔 했네요.

<br>

### typora



<img src="/img_src/typora.gif">



typora 사이트에 들어가서 특징을 보면 매우 특이합니다.

앞서 얘기한 기본 마크다운 문법 뿐 아니라, 수식, 도표 같은 형식도 지원해줍니다.



<img src="/img_src/typora_about.png">



무엇보다 마음에 드는 부분은 마크다운 문서를 작성하면서 결과 화면을 같이 볼 수 있다는 점이네요.

<img src="/img_src/typora_type.gif">

<br>



자, 이렇게 마크다운에 대한 문법을 알아보았으니

모두 깃헙 문서와 블로그 글을 쓰러 가시죠! 😎

<br>

<br>

<br>

<br>

----

_주석_
