## 정규표현식 테스트 사이트
https://regexr.com
https://regex101.com 등

## 정규식 생성방법
```js
// 생성자 함수방식
const regexp1 = new RegExp(^abc)
new RegExp(표현, 옵션)

// 리터럴 방식
const regexp2 = /^abc/
/표현/옵션
```

## 예제 문자열
```js
const str = `
010-1234-5678
thesecon@gmail.com
http://www.omdbapi.com/?apikey=7035c60c&s=frozen
The quick brown fox jumps over the lazy dog.
abbcccdddd
`
```

## 메소드
메소드 | 문법 | 설명
--|--|--
test | `정규식.test(문자열)` | 일치여부(boolean) 반환
match | `문자열.match(정규식)` | 일치하는 문자의 배열(Array) 반환
replace | `문자열.replace(정규식, 대체문자)` | 일치하는 문자를 대체

## 플래그 (옵션)
플래그 | 설명
--|--
g | 일치하는 모든 문자(global)
i | 영어 대소문자 구분하지 않음(ignore case)
m | 여러 줄로 구분하여 일치여부 확인(multi line)

## 패턴 (표현)
패턴 | 설명
--|--
^ab | 줄(Line) 시작에 있는 ab와 일치
ab$ | 줄(Line) 끝에 있는 ab와 일치
. | 임의의 한 문자와 일치
a&verbar;b | a 또는 b와 일치
ab? | b가 없거나 b와 일치
{3} | 3개 연속 일치
{3,} | 3개 이상 연속 일치
{3, 5} | 3개 이상 5개 미만 연속 일치
[abc] | a 또는 b 또는 c
[a-z] | a부터 z 사이의 문자 구간에 일치(영어소문자)
[A-Z] | A부터 Z 사이의 문자 구간에 일치(영어대문자)
[0-9] | 0부터 9 사이의 문자 구간에 일치 (숫자)
[가-힣] | 가부터 힣 사이의 문자 구간에 일치(한글)
\w | 63개 문자에 일치(대소영문 52 + 숫자 10 + 밑줄(_))
\b | 63개 문자에 일치하지 않는 문자 경계
\d | 숫자(digit)에 일치
\s | 공백(space, tab 등)에 일치
(?=) | 앞쪽 일치(Look ahead)
(?<=) | 뒤쪽 일치(Look behind)