 ## HTTP Protocol
 
 HTTP? TEXT기반의 PROTOCOL
 
 TCP Connection으로 연결되어 응답/요청을 받는다.
 
 Telnet과 generic tcp connection을 받음.  
 
 RequestLine <------------------------------
                    
                    RequestHeader(CRLF)
                    
                    (CRLF)emptyLine
                    
                    RequestBody
                    
                    
Message의 요소하나하나가 바로 Token이다.

첫번째로 나오는 것이 바로 Http Method(GET,POST,PUT,DELETE) +SPACE(공백도 문자이다.) + URI(RESOURCE) + SPACE(공백) + HTTP VERSION(HTTP/ 1.1)

공백 문자를 정의하는 곳은? 

일단 공백문자의 코드는?

먼저 ASCII 코드부터 알고 넘어가야 한다.

ASCII(American Standard Code For Information Interchange)

코드의 개수는? 128개라고 한다.

공백은 32번에 뜻한다. 

LF(Line Feed) 10번(0A) 라인( 줄 바꿈 했을 시 같은 위치의 다음 라인으로 넘어감)

CR(Cawiuage Return) 13(0B)번 엔터( 줄 바꿈 시 다음 라인의 첫번째 위치로 넘어감.)

즉 Http 마지막은 crlf로 넘어간다.

윈도우는 lf만 실행된다.

윈도우 맥 git을 사용했을때 항상 crlf 설정을 해줘야 한다.

아스키코드 하나는 몇비트일까? 128. 2의 7승 즉 7비트이다.

RequestHearder 뒤에 CRLF로 줄바꿈을 해주고

EMPTYLINE이 또 CRLF로 적용된다.

덤프뜨면 13/10 (0A/0)B으로 나온다.

hexadeclimal(16진법)
