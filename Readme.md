채팅서버 구현
---
조명 : 고구마라떼조
---
이름 : 김대용, 박재희,최원오 


학습목표
---
    소켓 프로그래밍 및 멀티 쓰레드 프로그래밍을 하는 방법에 대해 공부하고, 구현을 했습니다.
    기본적인 쓰레드 동작원리와 채팅서버가 어떻게 작동하는지에 대해서 고민하고, 구조적인 문제점이 있을경우
    개선점에 대해서 학습하였습니다.

배운것들
---
    Thread
    Socket 통신
    공유객체

구조
---
    채팅서버

    ChatHouse : 채팅서버의 자료구조, 채팅방과 채팅유저를 포함함.
    ChatServer : 서버 핸들러를 통해서 통신
    ChatServerHandler : 서버에서 작동하는 기능에 대해서 정의
    ChatServerMain : 메인 실행 클래스

    채팅클라이언트

    ChatClient : 채팅 핸들러를 통해서 통신
    ChatClientHandler : 클라이언트에서 작동하는 기능에 대해서 정의
    ChatClientMain : 메인 실행 클래스

구조적인 문제점
---
    채팅인원이 추가될때마다 쓰레드가 생성되어서, 인원이 많아질 경우 채팅이 정상적으로 작동하지 않을수있습니다.
    대용량 채팅이 불가능합니다.

개선가능점
---
    Nio, Netty를 통해서 대용량 서버를 만든다.
    자바 네트워크 소녀 네티책 참고
