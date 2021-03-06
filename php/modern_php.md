# Modern PHP

모던 PHP의 가장 중요한 특징들은 아래와 같다. 

- 네임스페이스
- 인터페이스
- 트레이트
- 제너레이터
- 클로저
- 젠드 오피캐시
- 내장 HTTP 서버




## 네임스페이스

PHP코드를 운영체제의 파일시스템 디렉토리 구조처럼 가상 계층 구조로 구성하는 도구. (PHP 5.3.0에서 도입)

실제 운영체제에 있는 물리적인 파일시스템과는 달리 가상의 개념이지만, 관례적으로 파일시스템 디렉토리에 맞추어 구성함.

네임스페이스가 생기기 전에는 유니크한 클래스명을 사용하기 위해 _를 사용하여 매우 긴 클래스명을 작성했다. 

하지만 네임스페이스가 등장한 이후로는 앞에 네임스페이스를 선언해주는 것으로 클래스명을 짧게 지을 수 있게 되었다. 



### 벤더네임스페이스 

최상위 네임스페이스로, 고유한 이름을 통해 하위경로에 저장되는 파일들을 외부와 분리해주는 역할을 한다. 

예제로, 아래 링크의 12번째 라인을 보면, 네임스페이스는 <?php 시작 태그 바로 다음 줄에 선언한다. 

https://github.com/symfony/http-foundation/blob/master/Response.php

```php
namespace Symfony\Component\HttpFoundation
```

위의 코드에서 Symfony가 벤더네임스페이스(최상위 네임스페이스)이며, 뒤이어 나오는 Component와 HttpFoundation은 서브네임스페이스다.



### import와 alias

#### import

```php
<?php
use Symfony\Component\HttpFoundation\Response;

$response = new Response('앗',400);
$response->send();
```

**use 명령어**를 사용해서 네임스페이스, 함수, 클래스, 인터페이스를 import 할 수 있다. 

이러면 Symfony\Component\HttpFoundation 라는 풀 클래스명을 사용하지 않고 맨 마지막의 Response만으로 인스턴스를 생성할 수 있다. 



#### alias

```php
<?php
use Symfony\Component\HttpFoundation\Response as Res;

$response = new Res('앗',400);
$response->send();
```

**as** 를 쓰면 줄여서 표기가 가능하다. 



## 인터페이스