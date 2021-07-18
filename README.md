# Servlet
## 서블릿  - 개발자가 HTTP Request, Response를 편리하게 사용할 수 있도록 해주는 것 - 서블릿 객체 생성 요청은 스레드가 한다.  ## 서블릿 컨테이너  - 서블릿 객체들을 생성, 호출, 관리(WAS가 종료되면 서블릿 컨테이너도 종료시킴) - 톰캣처럼 서블릿을 지원하는 WAS를 서블릿 컨테이너라고 함 - 서블릿 객체는 싱글톤으로 관리(스프링 컨테이너에 객체를 하나만 생성하고 공용으로 사용하는 것)     - 고객의 요청이 올 때마다 계속 객체를 생성하는 것은 비효율     - 최초 로딩 시점에 서블릿 객체를 미리 만들어두고 재활용     - 모든 고객 요청은 동일한 서블릿 객체 인스턴스에 접근     - **공유 변수 사용 주의**     - 서블릿 컨테이너 종료시 함께 종료 - JSP도 서블릿으로 변환되어서 사용 - 서블릿을 지원하는 WAS는 동시 요청을 위한 멀티 스레드 처리 지원  ## 서블릿을 이용한 HTTP 요청 처리 Flow  1. HTTP Request가 들어오면 서블릿은 Repuest 객체를 새로 생성해서 HTTP 요청 정보를 담는다 (Response 객체도 생성한다).  2. 개발자는 서블릿 Request 객체에서 요청 정보를 편하게 읽고 그에 맞게 Response를 준비한다. 3. Response가 준비되면 서블릿 Response 객체에 Response를 담아 응답을 보낸다.
