# golang-starter-docs
Go언어를 새롭게 배우시는 분들께 도움이 될 수 있는 다양한 자료들과 이론을 기록해요!

## 목차
- [Go언어란 무엇인가?](#Go언어란-무엇인가?)
  - [Go언어의 장점들](#Go언어의-장점들)
  - [Go언어의 단점들](#Go언어의-단점들)
- [Go언어 입문자를 위한](#Go언어-입문자를-위한)
  - [서적](#서적)
  - [영상](#)
- [코드와 관련된](#코드와-관련된)
  - [Code Style](#Code-Style)
  - [CSP](#CSP)
- [Back-End(서버 프로그래밍)](#Back-End)

## Go언어란 무엇인가?
Go언어는 2009년 구글에서 개발한 프로그래밍 언어로 구문이 C언어와 유사하며 가비지 컬렉션과 메모리 보안, [CSP(Communicating Sequential Processes)](https://ko.wikipedia.org/wiki/%EC%BB%A4%EB%AE%A4%EB%8B%88%EC%BC%80%EC%9D%B4%ED%8C%85_%EC%8B%9C%ED%80%9C%EC%85%9C_%ED%94%84%EB%A1%9C%EC%84%B8%EC%8A%A4) 스타일의 동시성을 지원합니다.   
특히 Go루틴을 통한 간편한 동시성 지원은 엔터프라이즈 서비스에서도 Go언어를 적극적으로 도입하게 되는 계기가 됐습니다. 이와 함께 단일 파일로 컴파일 되는 실행 파일은 외부 라이브러리에 대한 의존성이 없어 운영 환경에서 라이브러리 버전 충돌로 인한 시스템 구성 문제를 간단히 해결합니다.   
이와 같이 배포에 최적화 되면서 컨테이너기반의 시스템에서도 널리 쓰이게 됐습니다. - ["왜 Go언어를 사용하나요?"에서 발췌함.](https://www.namutech.co.kr/%EC%99%9C-go%EC%96%B8%EC%96%B4%EB%A5%BC-%EC%82%AC%EC%9A%A9%ED%95%98%EB%82%98%EC%9A%94/)

### Go언어의 장점들
**간결한 문법과 빠른 컴파일**  
Go언어는 시스템 프로그래밍에 적합하도록 설계되었으며, C언어와 구문이 비슷합니다.   
이는 대부분의 컴퓨터공학 전공자들이 C언어를 배울뿐더러 기존 시스템 프로그래밍 영역에서 C언어와 C++언어가 많이 사용되었기 때문에 개발자들이 새로운 언어에서 빠르게 생산성을 발휘할 수 있도록 하기 위함입니다.   
Go언어는 C언어와 비슷하지만 키워드가 25개로 C(37개), C++ 11(84개)에 비해 간결합니다. C언어와 C++언어에서의 복잡한 요소를 최대한 줄이고 간결하게 만들어져 C언어에 경험이 있는 개발자라면 쉽게 배울 수 있습니다.

Go언어는 C언어와 구문은 비슷하지만, 복잡도를 낮추고 컴파일 속도 향상을 위해 기존에 사용하던 헤더(Header) 파일을 정의하는 방식 대신 소스 자체를 패키지화하는 방식을 채택했습니다.  
소스코드 자체를 패키지화하여 변경된 부분만 컴파일함으로써 컴파일 속도를 향상시켰습니다.  

또한 Go 언어는 소스 내에 사용하지 않는 변수나 패키지가 있을 경우 컴파일 시 오류를 발생합니다. 불필요한 패키지 가져오기에 따른 지연시간을 줄이고 사용하지 않는 변수 및 패키지 선언으로 인해 향후에 발생할 수 있는 버그를 줄이고자 함입니다. - ["Google이 만든 프로그래밍 언어, Go"에서 발췌함.](https://www.samsungsds.com/kr/insights/golang.html)

**풍부한 기능과 유틸리티 제공**   
Go 언어는 개발자의 생산성 향상에 초점을 두고 설계되어 기존 개발자들이 사용하던 IDE(Integrated Development Environment)에서 쉽게 환경을 구성할 수 있습니다.  
[공식 홈페이지](www.golang.org)에서 Go 언어로 작성된 파일을 컴파일·실행·관리할 수 있는 go 바이너리를 다운로드하고 소수의 환경변수 $GOROOT, $GOPATH($GOPATH를 $PATH에 추가)를 설정하는 것만으로 개발 환경을 구성할 수 있습니다.   
다운로드한 유틸리티 go 파일은 Go 언어로 작성한 소스파일을 컴파일(build)하여 실행 가능한 바이너리를 생성하는 것은 물론, 컴파일 후 바로 실행(run)하는 기능을 제공합니다. - ["Google이 만든 프로그래밍 언어, Go"에서 발췌함.](https://www.samsungsds.com/kr/insights/golang.html)

## Go언어 입문자를 위한
### 서적
- [Tucker의 Go 언어 프로그래밍](http://www.yes24.com/Product/Goods/99108736)
- [가장 빨리 만나는 Go 언어](http://www.yes24.com/Product/Goods/18077092)
- 

### 영상
- [Tucker의 Go 언어 프로그래밍](https://youtu.be/KBdz5c-0t1w)
- [Learn Go Programming - Golang Tutorial for Beginners](https://youtu.be/YS4e4q9oBaU)

## 코드와 관련된
### 기초 문법
- [The Go programming language - Documentation](https://go.dev/doc/)

### Code Style
- [Effective Go](https://go.dev/doc/effective_go)
- [Uber Go Style Guide](https://github.com/uber-go/guide/blob/master/style.md)
- [TangoEnSkai/uber-go-style-guide-kr](https://github.com/TangoEnSkai/uber-go-style-guide-kr) - Uber Go Style Guide의 한국어 번역판
- [fransoaardi wiki - Uber go style guide(1)](https://fransoaardi.github.io/posts/uber_go_style_guide_1/)
- [fransoaardi wiki - Uber go style guide(2)](https://fransoaardi.github.io/posts/uber_go_style_guide_2/)
- [golang/go - Go Code Review Comments](https://github.com/golang/go/wiki/CodeReviewComments)

### CSP
- [CSP모델을 통한 Go 언어의 특성](https://velog.io/@myong/CSP%EB%AA%A8%EB%8D%B8%EC%9D%84-%ED%86%B5%ED%95%9C-Go-%EC%96%B8%EC%96%B4%EC%9D%98-%ED%8A%B9%EC%84%B1)
- [고 언어에서의 동시성 모델](https://hamait.tistory.com/934)
- [Communicating sequential processes(CSP) for Go developer in a nutshell.](https://levelup.gitconnected.com/communicating-sequential-processes-csp-for-go-developer-in-a-nutshell-866795eb879d) 

### Data Sturce(자료 구조)
- [[Golang] 자료 구조](https://dev-yakuza.posstree.com/ko/golang/data-structure/)
- [[이더리움으로 배우는 GO언어] 자료구조 & 컬렉션](https://hamait.tistory.com/1002)
- [Go(Golang) - 자료구조 Stack(스택) 작성 예제 및 소스파일 ](https://niceman.tistory.com/162)

## Back-End
### 추천하는 프레임워크
Go언어에서 사용할 수 있는 백엔드 프레임워크는 다양합니다. 기본적인 `net/http`부터 다양한 패키지를 지원하고 있습니다.  
[Top Go Web Frameworks](https://github.com/mingrammer/go-web-framework-stars)에서 Go언어에서 사용되는 백엔드 프레임워크에 대해서 순위를 알아보실 수 있습니다.

- [**`net/http`**](https://pkg.go.dev/net/http) - Package http provides HTTP client and server implementations.
- [**`gin-gonic/gin`**](https://github.com/gin-gonic/gin) - Gin is a HTTP web framework written in Go (Golang).
- [**`gofiber/fiber`**](https://github.com/gofiber/fiber) - Express inspired web framework written in Go
