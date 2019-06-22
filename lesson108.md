## 탐욕적(Greedy)방식-기본적으로, 게으른(Lazy)방식-?
- *?, +?, {n,}?

### i로 시작하고 n으로 끝나는 모든 문자 탐욕적 방식
- 예문
	`internationalization`
- 정규 표현식
	`i\w+n`
- 결과 [rubular.com](http://rubular.com/r/em8RaHlnq9)

### i로 시작하고 n으로 끝나는 모든 문자 게으른 방식
- 예문
	`internationalization`
- 정규 표현식
	`i\w+?n`
- 결과 [rubular.com](http://rubular.com/r/fr6Ejzal0N)

## 그룹 () 
- 괄호 사이에 존재하는 표현식을 통해 찾은 결과를 묶음으로 처리할 수 있다.
- \1과 같이 \ 문자와 그룹의 번호로 구성된다.
- 일반적으로 전체 결과가 \0이며 , 앞에서 부터 나타나는 그룹의 순서에 따라 숫자가 하나씩 증가하는 방식이다.

- 예문 : h 태그 찾기
```
<h1>이것은 첫 번째 제목</h1>
<h2>이것은 두 번째 제목</h2>
<h3>이것은 세 번째 제목</h3>
<h4>It's also right heading</h4>
<h5>이것은 올바르지 않은 제목</h6>
```
- 정규 표현식
`<(h[1-6])>[가-힣\w\s']+<\/\1>`
	- (h[1-6]) : h1부터 h6까지 
	- [가-힣\w\s']+ : 한글 및 영문자, 공백, '문자 한개 이상 존재하는 문자
	- <\/\1> : \것만 빼고 그룹 1과 동일하다.

- 결과 [rubular.com](http://rubular.com/r/ZF58XxDYVw)