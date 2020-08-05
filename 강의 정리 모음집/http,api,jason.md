### http

 1)http
   
   -Hyper Text Transfer Protocol
   
    ->인터넷을 통해 참조를 통해 한 문서에서 관련된 문서들로 
       넘나들 수 있게 해주는 주고 받을때 지켜야 할 규칙
 
 2)http 요청 메소드
   (1)get=url에 표시된 리소스 가져오기
   (2)post=body에 정보를 담아 서버에 입력
   (3)put=url에 표시된 리소르와 바꿔치기
   (4)patch=put과 다르게 일부만 수정
   (5)delete=url에 표시된 특정 리소스 삭제
  
###json
  
  1)json
  
    -java script object notation
    
    (내가 이해하기로는 정보를 가지고 올때, 작성할 때, 삭제할 때 이용하기 위한 방식)
    
   2)json의 특징
   
      +전송-> 직렬화 과정을 거친다
      +수신-> 역직렬화 과정을 거친다
      +기존 XML보다 가볍다 (프로세싱의 시간이 작다)
      +많은 프로그래밍 언어가 지원한다 
      
###api
  
  1)api
    
    -apprication programming interface
     
     (이용자가 쓸 수 있는 제어장치(ex 리모콘))
     
  2)api종류
  
    -soap(simple object access prtocol)
    
    -rest(represntational state transfer)----->주로 이놈 많이 이용
    
    -graphql(graph query language)
    
  3)rest 의 구성요서
  
    -자원(정보들)
    
    -행위(json(get, patch))
    
    -표현
