## NestJS 탄생 배경
NodeJS로 인해 javascript를 이용한 클라이언트 + 서버 (풀스택) 개발이 활발해져
javascript라는 한가지 언어로 개발을 할 수 있어 생산성을 향상 시키고 빠른개발이 가능해졌다.

하지만 NodeJS의 높은 자유도로 인해 Architecture 구성이 어렵고 효과적이지 못하였다.
하여 이를 해결하기 위해 Angular의 아키텍처 사상을 기반으로 NestJS가 만들어졌다.

### Angular 아키텍처 사상
- 의존성 주입(DI): 객체 간 결합도를 낮추고 테스트 용이성을 높이는 설계.
- 모듈화(Modular Architecture): 기능별로 분리된 모듈 구조로 개발.
- 컴포넌트 기반 설계: UI를 재사용 가능한 작은 단위로 분리.
- 데코레이터 활용: 선언적 프로그래밍으로 코드 가독성과 생산성 향상.
- MV 패턴*: 관심사의 분리를 통한 코드 관리 용이성.

## NestJS 특징
- nodeJS 서버 애플리케이션을 구축하기 위한 프레임워크
- Express 기반으로 만들어짐
- TypeScript을 기본으로 사용함
- 외부 모듈을 자유롭게 이용할 수 있음
- unit test와 e2e 테스트를 할 수 있는 툴을 제공

### NestJS를 사용하면 좋은점
- Nest는 Java의 Spring과 같이 규칙을 제공하여 아케텍처 구성을 위한 고민을 해소해준다.
- Java, Spring 사용자라면 아키텍처 구조가 비슷해 접근성이 좋다.
- Angular 아키텍처 구조 사상을 따르기 때문에 Angular 사용자도 접근성이 좋다.
- 기본적으로 제공하는 라우팅, 보안등의 기능이 많아 편리하다.
- 외부모듈을 통한 확장이 얼마든지 가능하다.

## NestJS 설치 및 실행
VSCode를 다운받고 NestJS를 실행할 폴더를 생성한 다음 VSCode를 열어 NestJS 
CLI(Command Line Interface)를 설치해야 한다.




