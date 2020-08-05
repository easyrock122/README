##FETCH API

 ### 1)비동기 처리
  
  -들어온 정보를 순차적(동기적)으로 처리하지 않고 동시적으로 요청을 처리한다
  
  -이런 방식을 통해 조금더 빨리 요청을 반환할 수 있다.
  
  -비동기 처리는 promise 객체를 사용한다
      ->대기
      ->이행
      ->거부
      
   ### 2)비동기 호출
      
      (1)async, await 키워드를 활용
      
          async function astncFunnction(){ await [promise객체] }
          
      (2)Promise객체
      
          .then(콜백함수)--->성공에 관함
          .catch(콜백함수)--->실패에 관함
          
   ### 3)FETCH API
     
      (1)FETCH API
      
         -네트워크 통신을 위해서 제공되는 API
         
         -Promise 객체를 반환
         
         -Request, Response라는 두 개의 객체 사용
        
       (2)실습
        
        function promiseTest1(timer) {
    // Promise 객체를 new 키워드를 통해 만들어줍니다.
    let promiseObj = new Promise((resolve, reject) => {
        setTimeout() => {
            // resolve 함수를 통해 메시지를 반환해줍니다.
            resolve(`Timer : ${timer}`)
        }, tumer);
    });

    // 반환된 메시지는 then 함수를 통해 익명함수의 매개변수
    // 여기서는 value로 들어가게 되고,
    // console.log(value)로 출력됩니다.
    promiseObj.then((value) => console.log(value));

}

funtion promiseTest2(timer) {
    // status를 랜덤으로 만듭니다.
    // Math.floor() : 바닥함수 -> 소수점이하를 버립니다.
    // Math.random() : 0~1 사이의 랜덤한 숫자를 반환합니다.
    const status = Math.floor(Math.random() * 10) % 2;
    let promiseObj = new Promise((resolve, reject) => {
        // 랜덤으로 뽑은 status가 1이면 resolve
        // status가 0이면 reject로 메시지를 반환합니다.
        setTimeout(() => {
            if (status === 1) resolve('성공!');
            else reject('실패!');
        }, timer)
    })

    promiseObj
        .then((value) => console.log(value))
        .catch((error) => console.log(error));
}
