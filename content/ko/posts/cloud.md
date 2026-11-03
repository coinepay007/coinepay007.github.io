---
title: "Cloudflare 초보자 가이드: 꼭 알아야 할 10가지 핵심 기능"
slug: cloud
date: 2026-11-03
draft: false
---
# Cloudflare 초보자 가이드: 꼭 알아야 할 10가지 핵심 기능

웹사이트의 로딩 속도를 높이고 보안을 강화하며 안정적인 접속 환경을 구축하고 싶다면 Cloudflare는 매우 유용한 서비스입니다.

Cloudflare는 DNS 관리, CDN, SSL/TLS, DDoS 방어, 웹 방화벽 등 웹사이트 운영에 필요한 다양한 기능을 제공합니다. 초보자도 기본적인 설정만으로 웹사이트의 성능과 보안을 개선할 수 있습니다.

이 글에서는 Cloudflare의 기본 개념부터 초보자가 알아야 할 10가지 핵심 기능, 설정 방법, 자주 발생하는 오류와 해결 방법까지 차근차근 설명합니다.

## 1. Cloudflare란 무엇인가요?

Cloudflare는 웹사이트 속도 향상, 보안 강화, 네트워크 관리 등의 서비스를 제공하는 플랫폼입니다.

웹사이트를 Cloudflare에 연결하면 방문자와 원본 서버 사이에 Cloudflare 네트워크가 배치됩니다.

이를 통해 다음과 같은 장점을 얻을 수 있습니다.

- CDN을 통한 웹사이트 로딩 속도 개선
- DDoS 공격 방어
- SSL/TLS를 통한 통신 암호화
- 간편한 DNS 관리
- 악성 트래픽 및 비정상적인 접근 차단
- 캐싱을 통한 원본 서버 부하 감소

Cloudflare는 무료 요금제도 제공하므로 개인 블로그나 소규모 웹사이트에서도 부담 없이 시작할 수 있습니다.

## 2. Cloudflare 계정 생성 및 웹사이트 추가

Cloudflare를 사용하려면 먼저 계정을 만들고 관리할 도메인을 추가해야 합니다.

### 2.1 계정 만들기

Cloudflare 공식 웹사이트에 접속합니다.

[https://www.cloudflare.com/](https://www.cloudflare.com/)

이메일 주소와 비밀번호를 입력해 계정을 생성한 다음, 필요한 경우 이메일 인증을 완료합니다.

### 2.2 웹사이트 추가하기

로그인한 후 대시보드에서 'Add a site'를 선택합니다.

관리하려는 도메인 이름을 입력하고 요금제를 선택합니다. 처음 사용하는 경우 무료 요금제부터 시작해도 좋습니다.

### 2.3 DNS 레코드 확인하기

Cloudflare가 기존 DNS 레코드를 자동으로 검색하면 각 항목이 올바른지 확인합니다.

특히 다음 레코드를 확인해야 합니다.

- A 레코드
- AAAA 레코드
- CNAME 레코드
- MX 레코드

이메일 서비스를 사용하고 있다면 MX 레코드와 관련 TXT 레코드도 정확하게 설정되어 있는지 확인해야 합니다.

### 2.4 네임서버 변경하기

Cloudflare에서 제공하는 네임서버 주소를 도메인을 구매한 등록기관의 관리 페이지에 입력합니다.

변경 사항이 적용되기까지 일정 시간이 걸릴 수 있습니다.

연결이 완료되면 Cloudflare 대시보드에서 다양한 기능을 관리할 수 있습니다.

## 3. 초보자가 알아야 할 Cloudflare 핵심 기능 10가지

## 3.1 DNS 관리(DNS Management)

DNS는 도메인 이름과 서버의 IP 주소를 연결하는 시스템입니다.

Cloudflare에서는 DNS 레코드를 한곳에서 관리할 수 있습니다.

대표적인 DNS 레코드는 다음과 같습니다.

- A: 도메인을 IPv4 주소에 연결
- AAAA: 도메인을 IPv6 주소에 연결
- CNAME: 다른 도메인 이름을 참조
- MX: 이메일 서버 지정
- TXT: 도메인 인증 및 이메일 인증 등에 사용

### Proxied와 DNS Only의 차이

Cloudflare DNS 관리 화면에는 주황색 구름과 회색 구름 아이콘이 표시됩니다.

**Proxied(주황색 구름)**

트래픽이 Cloudflare 프록시를 통과합니다. CDN 및 일부 보안 기능을 사용할 수 있습니다.

**DNS Only(회색 구름)**

DNS 조회만 Cloudflare에서 처리하며, 실제 트래픽은 원본 서버로 직접 연결됩니다.

일반적인 웹사이트의 HTTP/HTTPS 트래픽은 해당 레코드를 Proxied로 설정하면 Cloudflare의 프록시 및 보호 기능을 이용할 수 있습니다.

다만 이메일 서버처럼 프록시를 지원하지 않는 서비스의 DNS 레코드는 DNS Only로 설정해야 합니다.

## 3.2 CDN 및 웹사이트 속도 향상(CDN)

CDN은 전 세계 여러 지역에 분산된 서버를 통해 방문자와 가까운 위치에서 웹사이트 콘텐츠를 전달하는 기술입니다.

Cloudflare CDN을 사용하면 이미지, CSS, JavaScript 등의 정적 파일을 캐싱하여 원본 서버에 전달되는 요청을 줄일 수 있습니다.

주요 장점은 다음과 같습니다.

- 웹페이지 로딩 속도 개선
- 원본 서버의 부하 감소
- 해외 방문자에게도 빠른 콘텐츠 제공
- 웹사이트 접속 안정성 향상

CDN의 실제 효과는 웹사이트 구성, 캐시 설정, 방문자의 위치 등에 따라 달라질 수 있습니다.

## 3.3 SSL/TLS 설정(SSL/TLS)

SSL/TLS는 방문자와 웹사이트 사이의 통신을 암호화하는 기술입니다.

Cloudflare에서는 SSL/TLS 암호화 모드를 설정할 수 있습니다.

주요 모드는 다음과 같이 네 가지입니다.

**Off**

암호화를 사용하지 않습니다.

**Flexible**

방문자와 Cloudflare 사이의 통신만 암호화하며, Cloudflare와 원본 서버 사이의 통신은 암호화하지 않습니다.

**Full**

방문자부터 Cloudflare, Cloudflare부터 원본 서버까지 전체 통신을 암호화합니다. 다만 원본 서버의 인증서가 신뢰할 수 있는 인증기관에서 발급되었는지 검증하지는 않습니다.

**Full (strict)**

전체 통신을 암호화하며 원본 서버의 SSL 인증서도 검증합니다.

원본 서버에 유효한 SSL 인증서가 설치되어 있다면 일반적으로 'Full (strict)' 모드를 권장합니다.

### 자주 발생하는 SSL 오류

- 525: Cloudflare와 원본 서버 사이의 SSL 핸드셰이크에 실패한 경우 발생합니다.
- 526: Full (strict) 모드에서 원본 서버의 인증서를 검증할 수 없는 경우 발생합니다.

이러한 오류가 발생하면 원본 서버의 SSL 인증서, 서버 설정, 방화벽 등을 확인해야 합니다.

## 3.4 캐시 관리(Caching)

캐싱은 웹사이트 콘텐츠를 임시로 저장했다가 다음 방문 시 재사용하는 기능입니다.

Cloudflare 캐시를 사용하면 원본 서버에 전달되는 요청을 줄이고 페이지 로딩 속도를 개선할 수 있습니다.

### 주요 캐시 기능

- 정적 파일 캐싱
- Cache Rules를 통한 캐시 조건 설정
- Purge Cache를 통한 캐시 삭제
- 캐시 동작 방식 조정

### Purge Cache 사용 방법

웹사이트의 이미지나 CSS 파일을 변경했는데도 이전 내용이 계속 표시되는 경우가 있습니다.

이럴 때는 Cloudflare 대시보드에서 'Caching'으로 이동한 다음 'Purge Cache'를 선택해 캐시를 삭제하면 됩니다.

다만 로그인 페이지, 장바구니, 개인정보 페이지, 결제 페이지처럼 사용자마다 내용이 달라지는 페이지는 무분별하게 캐싱하지 않도록 주의해야 합니다.

## 3.5 DDoS 방어(DDoS Protection)

DDoS 공격은 특정 서버나 웹사이트에 대량의 트래픽을 전송해 정상적인 서비스를 이용할 수 없게 만드는 공격입니다.

Cloudflare는 네트워크에서 비정상적인 트래픽을 탐지하고 DDoS 공격에 대응할 수 있도록 지원합니다.

주요 장점은 다음과 같습니다.

- 대량의 악성 트래픽에 대한 방어
- 서버 부하 감소
- 웹사이트 서비스 가용성 향상
- 비정상적인 요청 필터링

웹사이트 운영자는 Cloudflare 보안 설정과 이벤트 로그를 정기적으로 확인하여 의심스러운 접근이 발생하는지 살펴보는 것이 좋습니다.

## 3.6 웹 애플리케이션 방화벽(WAF)

WAF는 웹 애플리케이션을 대상으로 하는 악성 요청을 탐지하고 제어하는 보안 기능입니다.

Cloudflare WAF를 사용하면 SQL 인젝션과 크로스 사이트 스크립팅(XSS) 등 일반적인 웹 공격에 대한 방어를 강화할 수 있습니다.

주요 기능은 다음과 같습니다.

- Managed Rules: 미리 제공되는 보안 규칙 사용
- Custom Rules: 직접 조건을 설정해 트래픽 허용 또는 차단
- 의심스러운 요청 탐지
- 특정 IP 주소나 국가 등을 기준으로 접근 제어

### 초보자를 위한 설정 팁

처음에는 사용 가능한 Managed Rules를 확인하고 필요한 보안 규칙을 활성화하는 것이 좋습니다.

다만 설정에 따라 정상적인 방문자의 요청까지 차단될 수 있습니다.

웹사이트 이용에 문제가 발생하면 보안 이벤트를 확인하고 정상적인 요청이 잘못 차단되고 있는지 살펴보세요.

## 3.7 리디렉션 설정(Redirect Rules)

Redirect Rules를 사용하면 방문자가 특정 URL에 접속했을 때 다른 URL로 자동 이동하도록 설정할 수 있습니다.

예를 들어 기존 페이지를 새로운 페이지로 변경했을 때 유용합니다.

대표적인 리디렉션 유형은 다음과 같습니다.

**301 리디렉션**

영구적인 주소 변경에 사용합니다. 기존 URL을 새로운 URL로 완전히 변경한 경우에 적합합니다.

**302 리디렉션**

임시적인 주소 변경에 사용합니다. 기간 한정 이벤트 페이지 등에서 활용할 수 있습니다.

리디렉션을 설정할 때는 원본 URL과 대상 URL을 정확하게 입력해야 합니다.

## 3.8 트래픽 분석(Analytics)

Cloudflare Analytics에서는 웹사이트의 트래픽과 보안 관련 정보를 확인할 수 있습니다.

주요 분석 항목은 다음과 같습니다.

- 요청 수
- 대역폭 사용량
- 캐시 사용 현황
- 보안 이벤트
- 트래픽 변화 추이

이러한 데이터를 통해 웹사이트의 접속 상태와 네트워크 문제를 파악하는 데 도움을 받을 수 있습니다.

다만 Cloudflare Analytics는 네트워크 및 요청 분석에 중점을 둡니다. 방문자의 행동이나 페이지 조회 정보를 분석하는 Google Analytics와는 목적이 다릅니다.

## 3.9 Cloudflare Workers

Cloudflare Workers는 Cloudflare 네트워크에서 JavaScript 등의 코드를 실행할 수 있는 서버리스 실행 환경입니다.

별도의 서버를 직접 관리하지 않고도 요청 처리나 API 구축 등의 작업을 수행할 수 있습니다.

주요 활용 사례는 다음과 같습니다.

- API 구축
- 요청 처리
- URL 재작성
- 인증 및 접근 제어
- 동적 콘텐츠 생성

Workers에서 사용할 수 있는 기능과 사용량 제한은 요금제 및 서비스 정책에 따라 달라질 수 있습니다.

## 3.10 Cloudflare Pages

Cloudflare Pages는 정적 웹사이트와 프런트엔드 프로젝트를 배포할 수 있는 호스팅 서비스입니다.

GitHub 등의 저장소와 연결하면 코드가 업데이트될 때 자동으로 웹사이트를 배포할 수 있습니다.

### 기본적인 웹사이트 배포 방법

1. Cloudflare 대시보드에 로그인합니다.
2. Workers & Pages 메뉴를 엽니다.
3. Pages 프로젝트 생성을 선택합니다.
4. GitHub 계정을 연결합니다.
5. 배포할 저장소를 선택합니다.
6. 빌드 명령어와 출력 디렉터리를 설정합니다.
7. 배포를 실행합니다.
8. 필요한 경우 사용자 지정 도메인을 연결합니다.

정적 웹사이트를 처음 공개하는 사용자도 비교적 쉽게 이용할 수 있습니다.

## 4. 초보자에게 추천하는 Cloudflare 기본 설정

Cloudflare를 처음 사용하는 경우 모든 기능을 한꺼번에 변경할 필요는 없습니다.

먼저 다음 기본 설정부터 확인하는 것이 좋습니다.

### 4.1 DNS 레코드 확인

A, AAAA, CNAME, MX 등의 레코드가 올바르게 설정되어 있는지 확인합니다.

### 4.2 SSL/TLS 설정

원본 서버에 유효한 SSL 인증서가 설치되어 있다면 'Full (strict)' 모드를 고려하세요.

### 4.3 CDN 및 캐시 활성화

정적 파일 캐싱을 활용하고 필요한 경우 Cache Rules를 설정합니다.

### 4.4 보안 기능 확인

DDoS 방어와 WAF 등 사용할 수 있는 보안 기능을 확인합니다.

### 4.5 로그 정기적으로 확인

Analytics와 보안 이벤트를 살펴보고 비정상적인 접근이나 설정 문제가 없는지 확인합니다.

## 5. Cloudflare 사용 중 자주 발생하는 문제와 해결 방법

Cloudflare를 설정한 후 웹사이트에 접속할 수 없거나 오류 메시지가 표시되는 경우가 있습니다.

여기서는 초보자가 자주 겪는 문제와 해결 방법을 소개합니다.

### 5.1 Cloudflare 연결 후 웹사이트가 열리지 않는 경우

가능한 원인:

- DNS 레코드가 잘못 설정됨
- 네임서버 변경 사항이 아직 적용되지 않음
- 원본 서버가 중단됨
- SSL/TLS 설정이 올바르지 않음

해결 방법:

1. DNS 레코드가 정확한지 확인합니다.
2. 도메인의 네임서버 설정을 확인합니다.
3. 원본 서버가 정상적으로 작동하는지 확인합니다.
4. SSL/TLS 암호화 모드를 확인합니다.

### 5.2 오류 522: Connection Timed Out

이 오류는 Cloudflare가 원본 서버와 연결을 설정하지 못하고 시간 초과가 발생했을 때 나타납니다.

가능한 원인:

- 원본 서버가 중단됨
- 서버 응답이 너무 느림
- 방화벽이 Cloudflare의 요청을 차단함
- 서버에 과부하가 발생함

해결 방법:

- 원본 서버가 정상적으로 작동하는지 확인합니다.
- 서버 방화벽 설정을 확인합니다.
- Cloudflare IP 주소에서 들어오는 요청을 허용합니다.
- 서버 부하와 네트워크 상태를 점검합니다.

### 5.3 오류 525: SSL Handshake Failed

이 오류는 Cloudflare와 원본 서버 사이의 SSL 핸드셰이크가 실패했을 때 발생합니다.

해결 방법:

- 원본 서버의 SSL 인증서를 확인합니다.
- 서버의 SSL/TLS 설정을 점검합니다.
- 사용 중인 암호화 방식과 포트를 확인합니다.
- 서버 측 SSL 관련 로그를 확인합니다.

### 5.4 이미지나 파일이 업데이트되지 않는 경우

웹사이트의 이미지나 CSS를 변경했는데 이전 내용이 계속 표시될 수 있습니다.

Cloudflare 또는 브라우저에 이전 캐시가 남아 있기 때문일 수 있습니다.

해결 방법:

1. Cloudflare 대시보드를 엽니다.
2. Caching 메뉴로 이동합니다.
3. Purge Cache를 선택합니다.
4. 필요한 캐시를 삭제합니다.
5. 브라우저를 새로고침하여 확인합니다.

### 5.5 무료 요금제로도 충분할까요?

개인 블로그, 소규모 웹사이트, 일반적인 콘텐츠 사이트라면 무료 요금제만으로도 기본 기능을 이용할 수 있는 경우가 많습니다.

다만 고급 WAF 기능, 추가 분석 기능, 세부적인 트래픽 제어 등이 필요하다면 유료 요금제를 검토할 수 있습니다.

제공 기능과 사용량 제한은 변경될 수 있으므로 최신 요금제 정보는 Cloudflare 공식 웹사이트에서 확인하는 것이 좋습니다.

## 6. Cloudflare 공식 자료

Cloudflare를 더 자세히 배우고 싶다면 다음 공식 자료를 참고할 수 있습니다.

- 공식 웹사이트: [https://www.cloudflare.com/](https://www.cloudflare.com/)
- 공식 개발자 문서: [https://developers.cloudflare.com/](https://developers.cloudflare.com/)
- Cloudflare 대시보드: [https://dash.cloudflare.com/](https://dash.cloudflare.com/)
- Cloudflare 학습 센터: [https://www.cloudflare.com/learning/](https://www.cloudflare.com/learning/)

기능별 설정 방법과 자세한 기술 정보는 공식 문서를 참고하세요.

## 7. 마무리

Cloudflare는 웹사이트 속도 향상, 보안 강화, DNS 관리 등을 통합적으로 지원하는 유용한 서비스입니다.

초보자는 먼저 DNS, CDN, SSL/TLS, 캐시, DDoS 방어와 같은 기본 기능부터 이해하는 것이 좋습니다.

이후 필요에 따라 WAF, Redirect Rules, Analytics, Workers, Pages 등을 활용하면 웹사이트 관리와 운영을 더욱 효율적으로 할 수 있습니다.

처음부터 모든 설정을 변경하기보다는 각 기능을 하나씩 이해하고 적용하는 것이 중요합니다.

## 8. 온라인 결제 및 TRON 에너지 관련 서비스

💳 **CoinePay – 가상 카드 서비스**

온라인 결제 옵션과 가상 카드 관련 서비스를 확인해 보세요.

👉 [https://www.coinepay.net/register?referrer=RFGSSDZ9](https://www.coinepay.net/register?referrer=RFGSSDZ9)

⚡ **TRXAPI – TRON 에너지 임대**

호환되는 블록체인 거래에 필요한 TRON 에너지 임대 서비스를 확인해 보세요.

👉 [https://login.trxapi.io/energy](https://login.trxapi.io/energy)

※ CoinePay와 TRXAPI는 Cloudflare와 관련이 없는 독립적인 제3자 서비스입니다. Cloudflare의 공식 제품이나 공식 파트너가 아닙니다.

## 9. 참고 자료

- Cloudflare 공식 웹사이트: [https://www.cloudflare.com/](https://www.cloudflare.com/)
- Cloudflare 개발자 문서: [https://developers.cloudflare.com/](https://developers.cloudflare.com/)
- Cloudflare DNS 문서: [https://developers.cloudflare.com/dns/](https://developers.cloudflare.com/dns/)
- Cloudflare SSL/TLS 문서: [https://developers.cloudflare.com/ssl/](https://developers.cloudflare.com/ssl/)
- Cloudflare 캐시 문서: [https://developers.cloudflare.com/cache/](https://developers.cloudflare.com/cache/)
- Cloudflare Workers 문서: [https://developers.cloudflare.com/workers/](https://developers.cloudflare.com/workers/)
- Cloudflare Pages 문서: [https://developers.cloudflare.com/pages/](https://developers.cloudflare.com/pages/)

