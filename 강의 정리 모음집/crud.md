## 7,8강 CRUD #1,2

->CREATE, READ, UPDATE, DELETE

  + GET/POST
    ->GET data를 url에 포함시켜 전송
          전송하는 길이에 제약O
          Caching 가능
  
          ---------------->read 에 활용
          
    ->POST  DATA를 body에 넣어 전송(url에 노출x)
            전송하는 길이에 제약x
            caching 불가능
           
           ------------------>create/update 에서 활용
  
 + [CREATE] 새로운 객체를 생성해 Date를 저장

  {객체 생성} if request.method == 'POST':
	        post = Designer()

  {입력 Data 저장}  post.name = request.POST['name']
                  post.address = request.POST['address']…
  
  {입력 Data(POST 객체) 저장} post.save()
  
 
 + [UPDATE] 정보 수정이 필요한 객체를 찾아 Data를 새롭게 저장

  {객체 탐색} post=get_object_or_404(Designer, pk = designer_id)
            if requset.mothod == 'POST':
  {입력 Data 저장}  post.name = request.POST['name']
                  post.address = request.POST['address']…
  {입력 Data(POST 객체) 저장}  post.save()

  + [DELETE] 제거가 필요한 객체를 찾아 삭제

  {객체 탐색} post = get_object_or_404(Designer, pk = designer_id)
  
  {객체 삭제} post.delete()
  
  {Home으로 이동} reyurn redirect('home')
  
  
