# 마크 다운 과 수학 표현식 이 만나다.

과거 오프라인 에서만 작성 하던 문서 가 웹 으로 확장 되면서 복잡한 표현 들 들 대한 고 들이.

그 중에 하나 인 수식 은 웹 에서 표현 하기 매우 어려웠 어려웠. 별도 의 도구 를 이용해 복잡한 과정 을 거쳐야 했지만 현재 현재 와 와 와 W3C 에서도 [MathML](http://www.w3.org/Math/) 으로 Математика 표현식 에 대한 표준화 를 진행중 에 있습니다.

## Что такое LaTeX?

> LaTeX 은 문서 작성 도구 의 일종 으로, 논문 이나 출판물 등 의 특수 형식 문서 를 작성 하는 데 쓰이는 시스템 시스템. LaTeX 은 TeX 의 확장 성 을 염두 에 둔 개선 판 이다. TeX 의 최초 개발자 는 도널드 크 누스 로, 자신 이 프로그래밍 에 대한 책 을 쓰려다 보니 적당한 조판 시스템 이 이 없어 개발.
>
> 보통 이를 Набор наборов (타입 세팅) 시스템 이라 부르는데 MS 워드 처럼 WYSIWYG (что вы видите, что вы получаете) 방식 으로 문서 를 작성 하는 것과 반대로 마치 프로그래밍 을 하듯 (혹은 마크 업 랭귀지 로 문서 를 작성 하듯 이) 문서 작성 을 하는 과정 을 의미 한다 (WYSIWYM: То, что вы видите, это то, что вы имеете в виду). Через [http://mirror.enha.kr/wiki/LaTeX](http://mirror.enha.kr/wiki/LaTeX)

![img](http://upload.wikimedia.org/wikipedia/commons/thumb/7/78/LaTeX_diagram.svg/400px-LaTeX_diagram.svg.png)

> LaTeX - это система подготовки документов для высококачественной верстки. Он чаще всего используется для средних или крупных технических или научных документов, но его можно использовать практически для любой формы публикации. Через [http://www.latex-project.org/](http://www.latex-project.org/)

## MathJax

![img](http://www.mathjax.org/wp-content/themes/mathjax/images/logo.gif)

MathJax 도 LaTeX 을 적용 해 웹 에서 수학 기호 나 수식 을 사용할 수 있도록 자바 스크립트 스크립트 라이브러리 화 한 것.

> MathJax - это движок отображения JavaScript с открытым исходным кодом для математики, который работает во всех браузерах. Через [http://www.mathjax.org/](http://www.mathjax.org/)

이 라이브러리 는 또한 많은 서비스 와 마크 다운 에디터 에서 활용 되어 지고 지고.

## 하루 패드 에서는 ...

![img](http://pad.haroopress.com/assets/images/logo-small.png)

하루 패드 에서는 마크 다운 을 이용해 이 구문 을 손쉽게 표현할 수 있도록 지원 지원.

**하루 패드 에서 수학 표현식 기능 은 기본적 으로 비활성화 되어 되어.**

### 옵션

옵션 은 환경 설정 (Предпочтение) 윈도우> 일반 (вкладка «Общие») 탭 에> **Включить выражение математики** 을 체크 상태 로 바꾸면 활성화 됩니다.

![img](http://pad.haroopress.com/docs/ko/mathematics-expression/images/001.png)

**Латекс**

```
J_\alpha(x) = \sum\limits_{m=0}^\infty \frac{(-1)^m}{m! \, \Gamma(m + \alpha + 1)}{\left({\frac{x}{2}}\right)}^{2 m + \alpha}

```

### 달러 기호 ($)

대부분 의 서비스 나 애플리케이션 에서 표기법 은 `$`을 통해서 제공 하며 2 가지 방식 을 제공 합니다.

첫번째 는 인라인 방식 으로 `$$$...$$$`와 같이 3 연속 되는 달러 기호 를 통해 표현식 을 묶어 주면 주면.

두번째 는 `$$..$$`으로 감싸 주게 되면 블럭 형태 로 표현 됩니다.

**사용 예시**

```
이 구문은 $$$\sqrt{3x-1}+(1+x)^2$$$ 인라인 표기법 입니다.

아래의 구문은 블럭으로 표현됩니다.

$$
\sqrt{3x-1}+(1+x)^2
$$

```

**결과**

> 이 구문 은 3 x - 1-----√+ ( 1 + x )2 인라인 표기법 입니다.
>
> 아래 의 구문 은 블럭 으로 표현 됩니다.
>
> 
>
> 3 x - 1-----√+ ( 1 + x )2
>
> 

### Рекомендации

수학 표현식 에 대해서 좀더 자세히 알고 싶다면 살펴 보세요.

- [http://www.latex-project.org/](http://www.latex-project.org/)
- [http://www.mathjax.org/](http://www.mathjax.org/)
- [http://ko.wikipedia.org/wiki/LaTeX](http://ko.wikipedia.org/wiki/LaTeX)
- [http://mirror.enha.kr/wiki/LaTeX](http://mirror.enha.kr/wiki/LaTeX)

0

![Вкусно](http://www.delicious.com/static/img/delicious.small.gif)Добавить

54
[вПоделиться](javascript:void(0);)