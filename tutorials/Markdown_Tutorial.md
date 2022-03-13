Smarcle markdown 작성법
======================
# 1. 마크다운에 관하여
## 1.1 마크다운이란?
[Markdown](https://whatismarkdown.com/)은 텍스트 기반의 마크업언어로 2004년 존그루버에 의해 만들어졌으며 쉽게 쓰고 읽을 수 있으며 HTML로 변환이 가능하다. 특수기호와 문자를 이용한 매우 간단한 구조의 문법을 사용하여 웹에서도 보다 빠르게 컨텐츠를 작성하고 보다 직관적으로 인식할 수 있다. 마크다운이 최근 각광받기 시작한 이유는 깃헙(https://github.com) 덕분이다. 깃헙의 저장소Repository에 관한 정보를 기록하는 README.md는 깃헙을 사용하는 사람이라면 누구나 가장 먼저 접하게 되는 마크다운 문서였다. 마크다운을 통해서 설치방법, 소스코드 설명, 이슈 등을 간단하게 기록하고 가독성을 높일 수 있다는 강점이 부각되면서 점점 여러 곳으로 퍼져가게 된다.    

## 1.2 마크다운의 장 - 단점
장점
-----------------------------
```
1. 간결하다.
2. 별도의 도구없이 작성가능하다.
3. 다양한 형태로 변환이 가능하다.
4. 텍스트(Text)로 저장되기 때문에 용량이 적어 보관이 용이하다.
5. 텍스트파일이기 때문에 버전관리시스템을 이용하여 변경이력을 관리할 수 있다.
6. 지원하는 프로그램과 플랫폼이 다양하다.
```

단점
-----------------------------------
```
1. 표준이 없다.
2. 표준이 없기 때문에 도구에 따라서 변환방식이나 생성물이 다르다.
3. 모든 HTML 마크업을 대신하지 못한다.
```

# 2. 마크다운 사용법(문법)
## 2.1. 헤더Headers
* 큰제목: 문서 제목
```
This is an H1
=============
```
This is an H1
=============

* 작은제목: 문서 부제목
```
This is an H2
-------------
```
This is an H2
-------------

* 글머리: 1~6까지만 지원
```
# This is a H1
## This is a H2
### This is a H3
#### This is a H4
##### This is a H5
###### This is a H6
```
# This is a H1
## This is a H2
### This is a H3
#### This is a H4
##### This is a H5
###### This is a H6
####### This is a H7(지원하지 않음)        

## 2.2. BlockQuote
이메일에서 사용하는 ```>``` 블럭인용문자를 이용한다.
```
> This is a first blockqute.
>	> This is a second blockqute.
>	>	> This is a third blockqute.
```
> This is a first blockqute.
>	> This is a second blockqute.
>	>	> This is a third blockqute.            

이 안에서는 다른 마크다운 요소를 포함할 수 있다.      

> ### 중국집 메뉴판
>	> * 메뉴판
>	>	> ```짜장면, 짬뽕, 탕수육......```           

## 2.3. 목록
* 순서있는 목록(번호)
```
1. 첫번째
2. 두번째
3. 세번째
```
1. 첫번째
2. 두번째
3. 세번째

### 현재까지는 어떤 번호를 입력해도 순서는 내림차순으로 정의된다.
```
1. 첫번째
3. 세번째
2. 두번째
```
1. 첫번째
2. 세번째
3. 두번째

### * 순서없는 목록(글머리 기호: ```*```, ```+```, ```-``` 지원)
```
* 빨강
  * 녹색
    * 파랑

+ 빨강
  + 녹색
    + 파랑

- 빨강
  - 녹색
    - 파랑
```
* 빨강
  * 녹색
    * 파랑

+ 빨강
  + 녹색
    + 파랑

- 빨강
  - 녹색
    - 파랑

혼합해서 사용하는 것도 가능하다(내가 선호하는 방식)

```
* 1단계
  - 2단계
    + 3단계
      + 4단계
```

* 1단계
  - 2단계
    + 3단계
      + 4단계   

## 2.4 코드
`(키보드에서 숫자키 옆에 ~키를 시프트 누르지 않고 나타내는 억음 부호를 통해 인라인에서 코드를 표현할 수 있다)를 사용하여 코드블럭코드를 만들 수 있는데 이를 이용해 코드를 출력할 수 있다.    
깃헙에서는 코드블럭코드("```") 시작점에 사용하는 언어를 선언하여 [문법강조(Syntax highlighting)](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/creating-and-highlighting-code-blocks#syntax-highlighting)이 가능하다.                 
![캡처123](https://user-images.githubusercontent.com/81175672/158050318-6ab3a8a3-23e8-4fad-aaee-75ba014b49eb.JPG)
[표 출처](https://computer-science-student.tistory.com/366)                

* C언어         
```C
#include <stdio.h>

int main()
{
printf("Hello! We are Smarcle!\n");
return 0;
}
```
* 파이썬           
```python
print("Hello! We are Smarcle!\n")
```
                   
## 2.5. 수평선 ```<hr/>```
아래 줄은 모두 수평선을 만든다. 마크다운 문서를 미리보기로 출력할 때 *페이지 나누기* 용도로 많이 사용한다.

```
* * *

***

*****

- - -

---------------------------------------
```

* 적용예
* * *

***

*****

- - -

---------------------------------------

## 2.6. 링크
* 외부 링크
```
사용문법: [Title](link)
적용예: [Google](https://google.com, "google link")
```          
Link: [Google](https://google.com, "google link")

* 자동연결
```
일반적인 URL 혹은 이메일주소인 경우 적절한 형식으로 링크를 형성한다.

* 외부링크: <http://example.com/>
* 이메일링크: <address@example.com>
```

* 외부링크:  http://example.com/
* 이메일링크:  address@example.com

## 2.7. 강조
```
*single asterisks*
_single underscores_
**double asterisks**
__double underscores__
~~cancelline~~
```
*single asterisks*
_single underscores_
**double asterisks**
__double underscores__
~~cancelline~~

## 2.8. 이미지
```
![Alt text](/path/to/img.jpg)
![Alt text](/path/to/img.jpg "Optional title")
```
### 위 경로로 변경시키는 법
![캡처45](https://user-images.githubusercontent.com/81175672/158050745-bedf1178-0c59-4626-b53b-ef4e2fe134a9.JPG)      
#### 1. Issues 창에 들어가기     
![캡처46](https://user-images.githubusercontent.com/81175672/158050787-521ae066-3b0f-435a-b272-d2c8d2814890.JPG)          
#### 2. New issue 클릭          
![캡처47](https://user-images.githubusercontent.com/81175672/158050813-c0c1ef99-5f9a-4b82-82a6-5f3323027052.JPG)      
#### 3. Leave a comment에 사진 파일 드래그
![캡처48](https://user-images.githubusercontent.com/81175672/158050835-f0ae93b9-265a-4dbe-a962-9a3e79dcd7f8.JPG)    
#### 4. 반환된 경로를 github 파일에 붙여넣기

### 사진 크기 조절하는 법
```
<img src="(사진 경로)"  width="(너비)" height="(높이)"/> 
```           
