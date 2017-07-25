# Как нарисовать диаграмму, используя Haroopad

우리 는 일상 생활 에서 일련 의 작업 들의 논리적 인 모습 을 다이어그램 으로 표현 표현 하는 경우 가. 가장 많이 사용 하는게 다이어그램 인데 대부분 의 위지윅 문서 도구 에서는 도형 기능 을 이용해 이용해 하고 하고 그릴.

하지만 하루 패드 와 같은 마크 다운 문서 에서는 그 방법 이 그리 쉽지 않을 뿐더러 위지윅 을 을 어울리지 어울리지 않습니다.

먼저 한번 보시죠.

## Синтаксис диаграммы?

아래 의 두가지 예시 는 다이어그램 을 그리는 문법 입니다.

```
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;

```

위 의 구문 의 특징 을 살펴보면 `graph TD;`와 `A-->B;`의 두가지 패턴 을 확인할 수 수.

`graph TD`는 그래프 방향 지시어 입니다. 그래프 를 `Top-Down`을 의미 합니다.

그리고 `A-->B;`는 A 노드 가 B 를 향한다 는 의미 입니다.

```
A
B
```

위 의 예시 에 방향 지시어 를 `graph LR`로 바꾸면 다음 과 같이 같이.

```
graph LR;
  A-->B;

```

꽤 간단한 방법 으로 단순한 노드 의 관계 를 표시 하였습니다. 좀더 복잡한 예시 와 결과 를 살펴 봅니다.

```
graph LR;
    A[Hard edge]-->|Link text|B(Round edge);
    B-->C{Decision};
    C-->|One|D[Result one];
    C-->|Two|E[Result two];

```

```
graph LR;
    A[Hard edge]-->|Link text|B(Round edge);
    B-->C{Decision};
    C-->|One|D[Result one];
    C-->|Two|E[Result two];

```

위 의 문법 은 이곳 을 통해 좀더 자세히 알 수 수.

- [https://github.com/knsv/mermaid/wiki](https://github.com/knsv/mermaid/wiki)

## Как нарисовать?

하루 패드 에서는 매우 단순한 방법 으로 다이어그램 을 표현 합니다.

위와 같은 구문 을 팬스 코드 블럭 (блокированный кодовый блок) 안에 넣으면 됩니다.

```
​```mermaid
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
​```

```

물론 그냥 문법 으로 표시 되도록 한다면 팬스 코드 블럭 에 `markdown`언어 를 지정 해주면 해주면.

```
​```markdown
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
​```

```

## Как продвигать

**Диаграмма последовательности**

```
sequenceDiagram
    Alice->Bob: Hello Bob, how are you?
    Note right of Bob: Bob thinks
    Bob-->Alice: I am good thanks!
    Bob-->John the Long: How about you John?
    Bob-->Alice: Checking with John...
    Alice->John the Long: Yes... John, how are you?
    John the Long-->Alice: Better then you!

```

**стайлинг**

```
graph LR;
    A[Hard edge]-->B(Round edge);
    B-->C{Decision};
    C-->D[Result one];
    C-->E[Result two];
    style A fill:#FF0000;
    style B fill:#00FF00;
    style C fill:#0000FF;
    style D fill:#FFF000;
    style E fill:#0FFFF0;

```

**Точечный синтаксис**

```
digraph
{
a -> b -> c -- d -> e;
a -- e;
}

```

## Благодаря

인어 라는 뜻 의 `Mermaid`하루 패드 에서 다이어그램 을 지원할 수 수 는 는 는 Knut Sveidqvist 씨 가 개발 한[Https://github.com/knsv](https://github.com/knsv) 덕분 입니다.

Русалка 는 좀더 가볍게 브라우저 기반 으로 이와 유사한 몇가지 오픈 소스 가 있었지만 있었지만 동작 에 필요한 리소스 비용 과 퍼포먼스 동작 에 필요한 리소스 비용 과 했으나 하게 하게 되었습니다 하루 패드 되었습니다 되었습니다 하게 되었습니다.

0

![Вкусно](http://www.delicious.com/static/img/delicious.small.gif)Добавить

54
[вПоделиться](javascript:void(0);)