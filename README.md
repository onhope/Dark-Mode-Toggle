# Dark-Mode-Toggle
<img src="./image.gif" width="500px">

## 효과  
버튼을 토글하면 배경이 흑백으로 전환   

## 학습     
### 1. CSS : @keyframes   
- 애니메이션 코드를 지정   
  ```
  @keyframes animationname {keyframes-selector {css-styles;}}
  ```

- 스타일 변경이 발생하는 시기 지정하는 방법 
  1. 백분율로 지정
  
  2. "from" 및 "to" 키워드를 사용하여 지정 => 이는 0% 및 100%와 동일합니다. 0%는 애니메이션의 시작이고, 100%는 애니메이션이 완료된 시점입니다. 

      예) 하나의 애니메이션에 여러 키프레임 선택기를 추가
      ```
      @keyframes mymove {
        0%   {top: 0px;}
        25%  {top: 200px;}
        50%  {top: 100px;}
        75%  {top: 200px;}
        100% {top: 0px;}
      }
      ```
  
- 애니메이션 중에 CSS 스타일 세트를 여러 번 변경할 수 있습니다.     
  
  예) 하나의 애니메이션에서 여러 CSS 스타일을 변경    
    ```
    @keyframes mymove {
        0%   {top: 0px; background: red; width: 100px;}
        100% {top: 200px; background: yellow; width: 300px;}
    }
    ```

  예) 다양한 CSS 스타일을 갖춘 다양한 키프레임 선택기

    ```
    @keyframes mymove {
        0%   {top: 0px; left: 0px; background: red;}
        25%  {top: 0px; left: 100px; background: blue;}
        50%  {top: 100px; left: 100px; background: yellow;}
        75%  {top: 100px; left: 0px; background: green;}
        100% {top: 0px; left: 0px; background: red;}
      }
    ```

- !important 규칙은 키프레임에서 무시    
    ```
    @keyframes myexample {
      from {top: 0px;}
      50%  {top: 100px !important;} /* ignored */
      to   {top: 200px;}
    }
    ```  

### 2. HTML : `<input>` 속성 checked
- 페이지가 로드될 때 미리 선택될 `<input>` 요소를 명시   
- checked 속성은 페이지가 로드된 후에도 자바스크립트를 사용하여 설정 가능   
- 불리언(boolean) 속성   
- 해당 속성을 명시하지 않으면 속성값이 자동으로 false 값을 가지게 되며, 명시하면 자동으로 true 값을 가지게 됩니다.     
- 이 속성은 `<input>` 요소의 type 속성값이 “checkbox” 또는 “radio”인 경우에만 사용할 수 있습니다.   

```
<input type="checkbox|radio" checked>
```

## 학습 출처 
- 유튜브   
https://www.youtube.com/@JavaScriptKing     

- CSS   
https://www.w3schools.com/cssref/css3_pr_animation-keyframes.php    

- HTML   
https://www.tcpschool.com/html-tag-attrs/input-checked