## API 연동하기
    - 웹 애플리케이션을 만들때 데이터를 브라우저 뿐 아니라 보존, 다른사람들도 조회할수 있도록
    - 서버를만들고 서버의 API를 사용하여 데이터를 읽고 써야 한다.

### REST API란?
    - 클라이언트와 서버가 소통하는 방식
    - Representational State Transfer API
    - 구성 : 자원(RESOUCE - URI), 행위(Verb - HTTP METHOD), 표현(Representations)
    - 특징 
        1. 유니폼인터페이스 :조작을 통일되고 한정적인 인터페이스로 수행하는 아키텍처 스타일
        2. 무상태성 : 작업을 위한 상태정보를 따로 저장하고 관리하지 않는다. (세션, 쿠키 X)
        3. 캐시가능 : HTTP라는 기존 웹표준을 그대로 사용,  Last-Modified태그나 E-Tag를 이용하면 캐싱 구현이 가능
        4. 자체표현구조 : REST API 메시지만 보고도 이를 쉽게 이해 할 수 있는 자체 표현 구조로 되어 있다
        5. 클라이언트-서버 구조 : REST 서버는 API 제공/클라이언트는 사용자 인증이나 컨텍스트 등을 직접 관리하는 구조로 역할구분이 확실하기 때문에 의존성이 줄어듦
        6. 계층형구조 : REST 서버는 다중 계층으로 구성될 수 있으며 보안, 로드 밸런싱, 암호화 계층을 추가해 구조상의 유연성을 둘 수 있고 PROXY, 게이트웨이 같은 네트워크 기반의 중간매체를 사용할 수 있게 한다.
    - REST API 디자인가이드
        1. URI의 정보자원 표현
        2.  자원에대한 행위는 HTTP Method(GET, POST, PUT, DELETE)로 표현
        3.  잘못된 REST 예)  GET /members/delete/1 Delete와 같은 행위에 대한 표현 X
        4.  리소스명은 동사보다 명사 사용
    - 예) GET/users
    - 예) POST/articles

    - axios : REST API 쉽게 요청 가능 요청 -> 프로미스 반환  
    - API 연동실습용 : https://jsonplaceholder.typicode.com/users
    
### useState 와 useEffect 로 데이터 로딩하기
    - 요청상태관리 : useState
    - 컴포넌터 렌더링시점에 요청 : useEffect
    - 요청에대한 상태관리 3가지 
        1. 요청의결과
        2. 로딩상태
        3. 에러

### useReducer로 요청상태 관리
    -  useState 대신 useReducer사용해보기 
    -  LOADING, SUCCESS, ERROR 액션3가지에 따라 다른 처리
    -  로직을 분리하여 쉽게 재사용 가능 
 










*** git url 변경
    git remote -v : URL 주소 찾기
    git remote set-url origin http://나머지 주소 