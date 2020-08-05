## javascript 기초문법
  
  1)javascript
  
    -이 친구는 주로 동적일때 이용하는 친구이다
    
    사용법1.html파일 않아서 <script> 태그내에 사용
    
    사용법2..js 파일로 만들고 <script src="파일경로">를 사용해서 불러오기
    
  2)변수
    사용가능한 데이터 타입:Boolean(사실, 거짓),Null(없음),Undefined(없음), Number(수), String,Symbol,Object.
    
    변수 선언 방식
      
      -var(잘 안씀)
      
      -let(block scope 변수)
      
      -const(변하지 않는 데이터를 저장 할때 이용)
      
    ex)
      let booleanVAl =true;
      typeof(booleanVAl)=>boolean
     
##기본적 javascript 문법

  1)for문
    
      for(let i=0;i<10;i++){consol.log(i)}
        1
        2
        3
        .
        .
        .
        10
   2)for in 문
   
      const numinfo = [one:first, two:second ,,,,,];
      
      for(const i in numinfo){console.log('기수:$(i), 서수:$(numinfo(i))};
      
   3)for of문(리스트 같은것을 반복즉으로 읽을 수 있을 때 하나씩 꺼내어 읽을 수 있게 한다)
      
      const oddNums = [1, 3, 5, 7, 9, 11];
      
      for(const i of oddNums){console.log(i);
   
   
   3)while 문
   
    let i = 0;
    
     while (i < 10> {console.log(i);i++;})
   
   
   4)조건문
   
    let score = prompt("점수를 입력하세요. 1", 0);
     
     if(score >= 90) {
     
         console.log("A+");
      } else if (score >= 80){
      
        colsole.log("B+");
        
      } else {
      
         console.log("C+");
         
      }
   
   ##dom 다루기
   
    1)document object model
     
     ->웹페이지에 접근할 수 있게 해주는 일본의 인터페이스
     
     ->js와는 별개임, js에 DOMㅇ르 조작할 수 있는 API가 존재
     
    2)DOM 활용과정
    
     (1)node 선택하기
     
      -ID로 DOM 객체 선택
     
        let idObj = document.getElementById("name");
      
      -Class로 DOM 객체 선택
    
       let classIbj = document.getElementsByClassName("");
      
      -CSS 선택자로 DOM 객체 선택
    
        let selectorObj = document.querySelector("#main");
        
     (2)속성 변경하기,추가하기
        -변경하기
         사용할 수 있는 속성들(style, innerText, innerHtml)
     
           + selectorObj.style = "color:yellow";
           + selectorObj.innerText = "헬로";
           + selectorObj.innerHTML = '<a href="https://www.naver.com>네이버로 가기</a>';
           
         a Tag의 herf 속성같은 각종 태그들의 속성들
        
          + aTag.href = "https://www.naver.com";
    
   ## 함수
   
   1) 기본
    funtion ver1_appendNewNode(target, tag="p", text="기본값") {
        let newTag = document.createElement(tag);
        newTag.innerText = ext;

        target.appendChild(newTag);
                }

            appendNewNode(target);
            appendNewNode(target, "a");
            appendNewNode(target, "a", "A태그!");
            
            
      2)화살표 함수
      let ver3_appendNewNode = (target, tag="p", text="기본값") => {
      let newTag = document.creteElement(tag);
            newTag.innerText = text;

            target.appendChild(newTag);
        }
   
    3)익명 함수
      let ver2_appendNewNode = function(target, tag="p", text="기본값") {
     let newTag = document.createElement(tag);
      neTag.innerText = text;

      target.appendChild(newTag);
      }
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
    
