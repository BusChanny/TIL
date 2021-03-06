1. Web Server와 Web Application Server의 차이점을 설명해주세요
   - 가장 큰 차이점은 동적인 컨텐츠를 다룰 수 있는지 여부입니다. WAS는 웹서버에 웹 컨테이너를 합쳐 동적 컨텐츠를 사용하게 만들어진 형태입니다.

2. WAS를 통해 클라이언트가 서버로부터 데이터를 받는 방식에 대해 설명해주세요

   1. 클라이언트가 웹 서버에 데이터를 요청합니다.
   2. 웹 서버에서는 동적 컨텐츠인지를 확인합니다.
      1. 동적 컨텐츠라면 웹 컨테이너로 전송합니다.
      2. 정적 컨텐츠라면 클라이언트에게 데이터를 전송합니다.
   3. 동적 컨텐츠를 전송받은 웹 컨테이너는 Servlet 구동환경을 제공합니다.
   4. 제공받은 환경에서 동적 컨텐츠를 생성하고 이를 웹서버에 넘겨줍니다.
   5. 넘겨받은 동적 컨텐츠를 클라이언트에게 전송해줍니다.

3. WAS가 웹 서버의 기능 모두 수행하지 않는 이유는 무엇인가요?
   
   1. 기능 분리로 서버 부하 방지
      - 정적 데이터 처리로 인해 부하가 커지게 되고, 동적 컨텐츠의 처리가 지연됨에 따라 수행 속도가 느려진다.
   2. 물리적 분리로 보안 강화
      - SSL에 대한 암복호화 처리에 웹 서버사용 
   3. 여러 대의 WAS 연결 가능
      - Load Balancing을 위해 웹 서버 사용
   4. 여러 웹 애플리케이션 서비스 가능
      - PHP Application과 Java Application을 함께 사용하는 경우  