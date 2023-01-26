# bootpay

[Flutter Bootpay 개발 문서](https://docs.bootpay.co.kr/?front=flutter&backend=curl#step-production) 사이트를 참조하였습니다.
```
Bootpay API를 사용하여 인앱 결제를 구현해보았습니다.

먼저 Frontend 클라이언트 단 결제 연동을 개발한 후에 
Backend 서버 단의 결제 결과 수신 및 취소 연동을 개발하고
테스트 개발 연동까지를 목표로 하고 개발을 하였습니다.
```

## 필요한 패키지 추가
```
bootpay 모듈과 생체 인증 결제 사용시 필요한 bootpay_bio 모듈을 설치하였습니다.
서버에서 데이터를 받아오기 위한 get 모듈을 추가 설치하였습니다.
```
![image](https://user-images.githubusercontent.com/58906858/214777425-d2dc7120-669e-4e63-9c88-29b48f6dc5b7.png)

## PG일반 카드 결제 테스트 ( 결제 요청1 )
```
PG사의 결제창을 통해 결제를 요청합니다. 
별도의 서버 개발 없이도 결제창을 띄워 실제 결제 진행까지 이 섹션을 통해 가능합니다.
```
![image](https://user-images.githubusercontent.com/58906858/214784045-c8f93fa6-d1f0-4198-9460-d9565e9c26c5.png)

```
기본 화면에 다양한 결제 방식의 버튼을 추가하면서 테스트해보았습니다.

제일 먼저 PG 일반 카드 결제 테스트의 예제코드를 사용해보았습니다.
```
![image](https://user-images.githubusercontent.com/58906858/214783943-f65cd243-7d55-4d6f-9519-c53c9514c222.png)

```
PG 일반 결제 버튼을 누르면 payload로 선택 상품의 이름과 가격 등의 정보를 각각의 payload 키의 값으로 전달해주었습니다.
결제 요청같은 경우 bootpay 안에 payload 모듈안에 결제 방식, 상품, 가격 등의 정보가 들어가 있는 것 같았습니다.

```
![image](https://user-images.githubusercontent.com/58906858/214784355-6094d04e-350b-438b-b2d1-dd3f6298128c.png)

![image](https://user-images.githubusercontent.com/58906858/214784188-6daad539-2924-4955-b117-de8733305064.png)
