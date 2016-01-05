# React 튜토리얼 따라해보기
http://reactkr.github.io/react/docs/tutorial-ko-KR.html
0.14.0 alpha1 한글판을 읽으면서 하나씩 따라해보는 중...

현재 0.14.5 버전이 있지만, 일단 0.14.0 으로 시작함.

0.14.0은 JSXTransformer-0.14.0-alpha.js을 사용하고 있고, 0.14.5는 babel을 사용하여 설명을 하고 있음.

현재 0.14.0은 다운로드 링크가 깨져 있어서 CDN 주소에서 다운 받아서 활용 (https://cdnjs.com/libraries/react/0.14.0-alpha1)

## 작업중인 파일 설명
* helloworld.html
* tutorial-1.html
* tutorial-2.html
* tutorial-3.html
* tutorial-4.html

## 작업중 발생한 문제점들

### tutorial-2.html 내용

<pre>
return (
            &lt;h1&gt;댓글&lt;/h1&gt;
            &lt;CommentList /&gt;
            &lt;CommentForm /&gt;
       )
</pre>
이와 같이 return 하면 "Adjacent JSX elements must be wrapped in an enclosing tag" 의 오류가 발생함.

<pre>
return (
        &lt;div&gt;
            &lt;h1&gt;댓글&lt;/h1&gt;
            &lt;CommentList /&gt;
            &lt;CommentForm /&gt;
        &lt;/div/&gt;
       )
</pre>
이와 같이 **&lt;div&gt;로 한번 감싸서 하나의 컴포넌트를 return!!**

참고 : http://stackoverflow.com/questions/31284169/uncaught-error-parse-error-line-38-adjacent-jsx-elements-must-be-wrapped-in-a





