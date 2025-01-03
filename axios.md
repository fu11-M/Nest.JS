## Axios
Axios는 JavaScript에서 HTTP 요청을 처리하는 데 사용되는 라이브러리이다. 브라우저와 Node.js 환경 모두에서 동작하며, 주로 비동기 요청을 보내고, 서버로부터 데이터를 받아오는 데 사용됩니다. Axios는 Promise 기반으로 작동하여, 비동기 코드를 작성하는 데 유용하고, JSON 응답을 쉽게 처리할 수 있다.

Axios는 JavaScript에서 HTTP 요청을 간편하게 처리할 수 있는 라이브러리로, 비동기 요청을 Promise 기반으로 처리한다. 이를 통해 then()과 catch() 메서드를 사용하여 요청의 결과를 쉽게 처리할 수 있다. 

또한, Axios는 브라우저 환경뿐만 아니라 Node.js 환경에서도 사용할 수 있어, 서버와 클라이언트 모두에서 유용하게 활용된다. 사용자는 GET, POST, PUT, DELETE와 같은 다양한 HTTP 메서드를 간단하게 호출할 수 있어, API 통신을 효율적으로 관리할 수 있다.

Axios는 서버로부터 JSON 형식의 응답을 받을 경우, 이를 자동으로 파싱하여 JavaScript 객체로 변환해 주기 때문에 별도의 파싱 작업을 할 필요가 없다. 

또한, 요청을 보내기 전에는 request interceptor를 사용하여 요청을 수정할 수 있고, 응답을 받은 후에는 response interceptor를 통해 응답을 처리할 수 있는 기능을 제공한다. 이 인터셉터 기능은 코드의 유연성과 관리 편의성을 높이는 데 유용하다.

URL, 헤더, 타임아웃 등의 설정을 전역적으로 정의할 수 있는 기능을 제공하여, 코드의 재사용성을 높이고 설정을 일관되게 관리할 수 있게 해준다.

### HTTP 요청 예시

Axios는 웹에서 데이터를 주고받는 역할을 하는 HTTP 요청 라이브러리입니다. 예를 들어, 프론트엔드에서 React를 사용해 사용자 정보를 표시하는 웹 애플리케이션을 만들고, 백엔드에서 NestJS를 사용해 사용자 데이터를 제공하는 서버를 구축한다고 가정해봅시다.

React에서는 사용자가 페이지에 접속했을 때 사용자 목록을 불러오기 위해 Axios를 사용해 NestJS 서버의 /users 엔드포인트로 GET 요청을 보냅니다. 이 요청은 React의 컴포넌트가 렌더링되기 전에 실행되거나 특정 버튼 클릭과 같은 사용자 액션에 의해 트리거될 수 있습니다. 

예를 들어, React의 useEffect 훅 안에서 Axios를 사용하여 서버에 요청을 보내고, 서버로부터 받은 사용자 데이터를 컴포넌트의 상태(state)에 저장합니다. 

그런 다음, 상태에 저장된 데이터를 React가 화면에 렌더링해 사용자에게 표시합니다. 이처럼 Axios는 프론트엔드에서 데이터를 요청하고 결과를 받아 UI를 업데이트하는 중요한 역할을 합니다.

반대로, 백엔드에서는 NestJS가 React로부터 온 Axios의 HTTP 요청을 처리합니다. 

NestJS는 사용자 목록을 반환하기 위해 컨트롤러와 서비스 계층을 활용합니다. 예를 들어, React에서 /users 엔드포인트로 GET 요청이 오면, NestJS의 컨트롤러는 이 요청을 받아 서비스 계층으로 전달합니다. 

서비스 계층은 데이터베이스에서 사용자 정보를 조회한 뒤, 조회된 데이터를 JSON 형식으로 컨트롤러에 반환합니다. 컨트롤러는 최종적으로 이 데이터를 React로 응답합니다.

 NestJS는 요청을 처리하고 데이터를 제공하는 역할을 수행하며, React는 Axios를 사용해 이 데이터를 받아 화면에 표시합니다.

이처럼 프론트엔드와 백엔드 각각의 역할이 분명하게 나뉘어 있고, Axios는 이 둘을 연결해 데이터 흐름을 원활하게 만들어주는 중요한 도구로 사용됩니다. 프론트엔드에서는 사용자의 요청을 백엔드에 전달하고 데이터를 받아 UI를 업데이트하며, 백엔드에서는 클라이언트의 요청을 처리하고 필요한 데이터를 제공하는 구조를 가집니다. 

이를 통해 React와 NestJS가 협력해 사용자에게 완전한 기능을 제공할 수 있습니다.