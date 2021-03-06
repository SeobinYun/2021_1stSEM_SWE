# ***2021_1stSEM_SWE***

---

## ***GFM extension     |    GFM 확장기능***

---

### 4.10. Tables 표
- 표를 추가하고 싶을 때 사용
- **사용법** : 하이픈(-)과 파이프(|)문자를 사용한다.
    - 단어들을 작성할 때, **파이프(|) 문자 하나를 이용해 열을 구분**하고, **3개의 연속된 하이픈(-)문자을 이용해 행의 헤더를 구분**시켜준다.

    - *ex 198*
        > 
          | 이름 | 나이 |
          | --- | --- |
          | 윤서빈 | 20 |

    
     
        | 이름 | 나이 |   
        | --- | --- |
        | 윤서빈 | 20 |
        
        
    - *ex 205* // 추가된 행이 없을 경우 
        >
          | abc | def |
          | --- | --- |

        | abc | def |
        | --- | --- |


- **특징**
    1. 행의 헤더를 구분하는 하이픈(---)열에 **콜론(:)문자를 추가**하여 각각의 열마다 정렬위치를 지정할 수 있다.   
        >             
            | 이름 | 지역 | 나이 |
            | :--- | :---: | ---: |
            | 윤서빈 | 서울특별시 | 20 |
            | 김도토리 | 제주도 | 9 |


        | 이름 | 지역 | 나이 |
        | :--- | :---: | ---: |
        | 윤서빈 | 서울특별시 | 20 |
        | 김도토리 | 제주도 | 9 |

     2. 표 안에 파이프 문자를 사용하고 싶을 경우, **파이프 문자 앞에 백슬래쉬(\\)를 넣어주면 된다.**
     3. 표 안에 링크, 코드, 강조와 같은 다른 Markdown 구문을 적용할 수 있다.  
       - *ex 200*
         >
                   | Name \| age  | 
                   | ------ |
                   | Seobin `\|` 20 |  // '|' 코드화
                   | Dotori **\|** 9 | // '|' Bold


           | Name \| age  |
           | ------ |
           | Seobin `\|` 20 |
           | Dotori **\|** 9 |



    4. 열의 수가 헤더의 열의 수보다 적을 경우, 나머지 셀은 빈칸으로 채워진다.       
        하지만 열의 수가 헤더의 열의 수보다 많을 경우, 초과된 부분은 무시된다.  
      - *ex 204*
          >
                | Name | age |
                | --- | --- |
                | Seobin |           // 열의 수가 적을 경우
                | Dotori | 9 | Jeju |   // 열의 수가 많을 경우


        | Name | age |
        | --- | --- |
        | Seobin |
        | Dotori | 9 | Jeju |

        
---

### 5.3. Task list items
- 할 일 목록을 작성할 때 사용, 사용시 체크박스가 나타난다.
- **사용법** : 할 일 맨앞에 하이픈(-)기호 하나를 적고 대괄호([])를 이어서 적어준다.  
                이때 체크박스를 체크 상태로 나타내고 싶다면 대괄호 사이에 **'x'를 추가**해주면 된다.
    >   
        - [ ] 할일

    >
        - [x] 밥먹기  
        - [x] 숨쉬기
        - [ ] 소웨공 과제하기
        - [ ] 깃헙 1일 1커밋하기


     > - [x] 밥먹기  
     > - [x] 숨쉬기
     > - [ ] 소웨공 과제하기
     > - [ ] 깃헙 1일 1커밋하기

- **특징** : 들여쓰기를 통해 Task list 안에 또 Task list를 적용할 수 있다.
    >
        - [x] 나가기
            - [ ] 마스크 사기
            - [ ] 햄버거 먹기 
                - [ ] 상하이스파이시버거
        - [ ] 물마시기
            - [ ] 20잔

     > - [x] 나가기
     >   - [ ] 마스크 사기
     >   - [ ] 햄버거 먹기 
     >       - [ ] 상하이스파이시버거
     > - [ ] 물마시기
     >   - [ ] 20잔

---

### 6.5 Strikethrough
- 단어에 취소선을 적용하고 싶을 때 사용
- **사용법** : 취소선을 긋고자하는 단어나 문장 앞뒤에 **물결표시(~) 두개를 연속으로 추가**해준다.
    > 
        Hi. My name is ~~Lia~~ Seobin. Nice to meet you.
        
    >

        Hi.
        My name is ~~Lia
        from Seoul.~~.
        Seobin. Nice to meet you.
    
    > Hi. My name is ~~Lia~~ Seobin. Nice to meet you.
     
    > Hi.  
    > My name is ~~Lia  
    > from Seoul.~~  
    > Seobin. Nice to meet you.  


- **주의점** : 물결표시를 적용하고자하는 단어와 띄어쓰면 안된다. 무조건 붙여써야 한다.
    > 
        Hi. My name is ~~ Lia ~~ Seobin. Nice to meet you. (X)
        
    > Hi. My name is ~~ Lia ~~ Seobin. Nice to meet you.


---

### 6.9 Autolinks
- 앞서 언급한 링크 방법과 달리 자동 링크 연결을 지원한다.
- 확장된 www autolink는 'www.' 를 인식해 자동으로 링크로 연결될 수 있게 도와준다.
- **사용법** : 그냥 URL을 쓰면 된다.
    > 
        www.google.com
    
    > www.google.com
 
- **특징** : 이메일 주소에도 적용된다.
    >
        o0oseobin@naver.com
        
    > o0oseobin@naver.com
   
- **자동URL연결 차단** : URL 앞뒤에 backstick(`)기호를 적용한다.
    > 
        `www.google.com`
        
    > `www.gooogle.com`
   
---

### 6.11 Disallowed Raw HTML
- GFM은 HTML 출력을 할때, 몇몇 아래와 같은 HTML 태그를 필터링하는 태그 필터 확장 기능을 가능하게 한다.
- 목록에 없는 HTML 태그들은 수정되지 않는다.
- **목록**
    >
        - <title>
        - <textarea>
        - <style>
        - <xmp>
        - <iframe>
        - <noembed>
        - <noframes>
        - <script>
        - <plaintext>
    
- '<'기호를 '\&lt;'로 대체하면서 적용된다.
- **사용예시**
    >
        <strong> <title> <style> <em>  

        <blockquote>
            <xmp> is disallowed.  <XMP> is also disallowed.
        </blockquote>
      
    > <strong> <title> <style> <em>
    >
    > <blockquote>
    >  <xmp> is disallowed.  <XMP> is also disallowed.
    > </blockquote>

---

### Fenced code blocks
- 코드블록을 설정하고 싶을 때 사용
- **사용법** : 적용하고자 하는 코드의 맨 위아래 라인에 backticks(`) 기호 3개를 추가해준다.
    > 
        ```
        void myfunction(void){
            printf("Hi\n");
        }
        ```
   
   ```
   void myfunction(void){
   printf("Hi\n");
   }
   ```
       
---
