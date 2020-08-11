## 2강 hello django

1)가상환경이란?
  ->자신이 원하는 Python 환경 구축을 위해 필요한 모튤만 담아 놓는 바구니 느낌???
  
2)pip 란??
  ->Python으로 작성된 패키지 소프트 웨어를 관리하는 패키지 관리 시스템
  
3)vs code 단축키들
 
  + 터미널 생성: ctrl + shift + `
  + 이전 명령어 불러오기: 화살표 ↑
  + 현재 커서 위치의 코드 복사: Ctrl + D (여러 줄 복사도 가능)
  + 현재 커서 위치의 코드 이동: Alt + 화살표 ↑ or ↓
  
4)가상환경 명령어 모음

  + [가상환경 생성] 
    -> python -m venv <가상환경 이름>
  + [가상환경 활성화]
    -> source <가상환경 이름>/bin/activate
  + [가상환경 끄기
    -> deactivate
    
5)장고 명령어
   + [패키지 설치] 
    -> pip install django
   + [프로젝트 생성]
    -> django-admin startproject<프로젝트 명> . (마지막에 .을 붙이면 새로운 폴더 생성 안됨)
   + [App 생성] 
    -> python manage.py startapp <App 이름>
   + [로컬 서버 시작]
    ->Python manage.py runserver
    
6)깃 허브 생성 방법

7)repository 업로드 방법

8)생성되는 파일 명+능력

 + project
  -> setting.py: 전체 프로젝트를 관리하는 설정 파일(자주볼것이여)
  -> urls.py: 프로젝트의 URL 관리 파일(자주 볼것이여)
  -> wsgi.py & asgi.py: 프로젝트를 서비스하기 위한 파일(배포할 때 하니면 볼일 없는 파일)
  -> __init__.py: 해당 디렉토리가 Python Pakage의 일부임을 Python에게 알려주는 파일
  
 + App
  -> views.py: 웹 요청을 받고, 전달받은 데이터를 처리해서 가공하는 파일(자주봏것이여)
  -> models.py: Database와 관련된 다양한 역할 수행(자주봏것이여)
  -> admin.py: 관리자 관련 파일
  -> apps.py: Project에서 App의 존재를 알려줄 때 활용되는 파일

9)Home 페이지에 풀력하기

  + settings.py -> Project에게 App의 존재 알리기
  + Templates -> User에게 보여줄 HTML 파일 만들기
  + views.py -> 요청이 들어오면 HTML 파일을 열어주는 함수 정의
  + urls.py-> url 요청을 views와 연결하기
