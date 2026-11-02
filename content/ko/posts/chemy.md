---
title: "Alchemy 가입 가이드: 계정 생성 및 API Key 발급 방법"
slug: chemy
date: 2026-11-02
draft: false
---


# Alchemy 가입 가이드: 계정 생성 및 API Key 발급 방법

Alchemy는 Web3 개발자를 위한 블록체인 인프라 플랫폼으로, RPC 서비스, 온체인 데이터 조회 및 탈중앙화 애플리케이션(DApp) 개발을 지원합니다. 이 가이드에서는 Alchemy 계정을 생성하고 API Key를 발급받는 방법을 단계별로 설명합니다.

Web3 서비스를 이용할 때 온라인 결제 수단이 필요한 경우 CoinePay 가상 카드 서비스를 별도로 알아볼 수 있습니다. 또한 TRON 네트워크에서 거래 수수료를 관리하려는 사용자는 TRXAPI의 TRON 에너지 임대 서비스도 참고할 수 있습니다. 두 서비스는 Alchemy와 별개의 독립적인 서비스이며, Alchemy와 공식적인 제휴 또는 통합 관계가 아닙니다.

## 💳 CoinePay – 가상 카드 서비스

CoinePay는 온라인 결제에 활용할 수 있는 가상 카드 서비스를 제공합니다. 다양한 온라인 서비스의 결제 수단을 알아보고 있다면 아래 링크에서 확인할 수 있습니다.

👉 [https://www.coinepay.net/register?referrer=RFGSSDZ9](https://www.coinepay.net/register?referrer=RFGSSDZ9)

## ⚡ TRXAPI – TRON 에너지 임대 서비스

TRXAPI는 TRON 네트워크에서 필요한 에너지를 임대할 수 있는 서비스입니다. TRON 네트워크의 거래 비용을 관리하는 데 관심이 있다면 아래 링크를 참고하세요.

👉 [https://login.trxapi.io/energy](https://login.trxapi.io/energy)

## 1. Alchemy란 무엇인가요?

Alchemy는 블록체인 애플리케이션 개발을 위한 인프라 서비스를 제공하는 플랫폼입니다. 개발자는 Alchemy를 통해 블록체인 네트워크에 연결하고, 데이터를 조회하며, 스마트 컨트랙트와 상호작용할 수 있습니다.

Alchemy에서 제공하는 주요 기능은 다음과 같습니다.

- **RPC 서비스:** 애플리케이션과 블록체인 네트워크 간의 통신을 지원합니다.
- **온체인 데이터 조회:** 블록체인의 트랜잭션, 블록 및 기타 데이터를 조회할 수 있습니다.
- **개발자 도구:** Web3 애플리케이션 개발과 디버깅을 지원합니다.
- **API 서비스:** 다양한 블록체인 네트워크와 연결할 수 있는 API를 제공합니다.

Alchemy를 사용하려면 먼저 계정을 만들고 프로젝트에 사용할 API Key를 발급받아야 합니다.

## 2. Alchemy 가입 전에 준비할 사항

가입을 시작하기 전에 다음 사항을 준비하세요.

### 2.1 유효한 이메일 주소

Alchemy 계정 등록과 이메일 인증에 사용할 수 있는 이메일 주소가 필요합니다.

### 2.2 안정적인 인터넷 연결

가입 과정에서 이메일 인증과 Dashboard 접속이 필요하므로 안정적인 인터넷 환경을 사용하는 것이 좋습니다.

### 2.3 사용할 블록체인 네트워크 확인

API Key를 생성하기 전에 어떤 블록체인 네트워크를 사용할지 결정하는 것이 좋습니다.

예를 들면 다음과 같습니다.

- Ethereum Mainnet
- Ethereum Sepolia
- Base

사용할 네트워크에 따라 앱 생성 과정에서 적절한 체인을 선택해야 합니다.

## 3. Alchemy 공식 웹사이트에서 계정 만들기

### 3.1 공식 웹사이트 접속

Alchemy 공식 웹사이트를 방문합니다.

[https://www.alchemy.com/](https://www.alchemy.com/)

홈페이지에서 **Sign Up**, **Sign In** 또는 **Get Started** 버튼을 클릭합니다.

### 3.2 회원가입 진행

화면의 안내에 따라 이메일 주소를 입력하거나 지원되는 타사 계정 로그인 방식을 선택합니다.

이메일로 가입하는 경우 다음 단계를 진행합니다.

1. 이메일 주소를 입력합니다.
2. 비밀번호 설정 등 화면에 표시되는 절차를 완료합니다.
3. 이메일 인증 메시지를 확인합니다.
4. 인증 절차를 완료하고 계정에 로그인합니다.

### 3.3 Dashboard 접속

로그인이 완료되면 Alchemy Dashboard로 이동합니다.

[https://dashboard.alchemy.com/](https://dashboard.alchemy.com/)

Dashboard는 Alchemy에서 앱과 API Key를 관리하는 주요 화면입니다.

일부 계정에는 가입 직후 기본 앱이나 API Key가 이미 표시될 수 있습니다. 표시되는 항목을 먼저 확인하고, 필요한 경우 새 앱을 생성하면 됩니다.

## 4. Alchemy에서 새 앱 만들기

API Key를 체계적으로 관리하려면 프로젝트별로 앱을 생성하는 것이 좋습니다.

### 4.1 Apps 메뉴 찾기

Alchemy Dashboard에 로그인한 후 다음 메뉴를 찾습니다.

**Team Overview > Apps**

계정 화면의 버전에 따라 메뉴 위치나 이름이 다르게 표시될 수 있습니다.

### 4.2 Create new app 클릭

Apps 페이지에서 **Create new app** 버튼을 클릭합니다.

앱 생성 화면이 열리면 프로젝트 정보를 입력합니다.

### 4.3 앱 정보 입력

일반적으로 다음 항목을 설정할 수 있습니다.

- **App Name:** 앱 또는 프로젝트 이름
- **Description:** 프로젝트 설명
- **Chains:** 사용할 블록체인 네트워크
- **Services:** 필요한 서비스 또는 기능

예를 들어 Ethereum 네트워크를 사용하는 프로젝트라면 Chains에서 Ethereum을 선택할 수 있습니다.

### 4.4 앱 생성 완료

필요한 정보를 입력한 다음 **Create App** 버튼을 클릭합니다.

생성이 완료되면 Apps 목록에 새 앱이 표시됩니다.

## 5. Alchemy API Key 발급받기

앱을 생성했다면 이제 API Key를 확인할 수 있습니다.

### 5.1 앱 상세 페이지 열기

Alchemy Dashboard의 Apps 목록에서 방금 생성한 앱을 선택합니다.

앱 상세 페이지에서 해당 앱의 API 관련 정보를 확인할 수 있습니다.

### 5.2 API Key 복사하기

앱 상세 화면에서 **API Key** 항목을 찾습니다.

복사 버튼을 클릭해 API Key를 복사합니다.

API Key는 애플리케이션이 Alchemy 서비스에 요청을 보낼 때 사용하는 인증 정보입니다. 다른 사람에게 노출되지 않도록 주의하세요.

### 5.3 Endpoints 확인하기

앱 상세 페이지의 **Endpoints** 탭에서도 네트워크별 API Endpoint를 확인할 수 있습니다.

Ethereum Mainnet RPC Endpoint의 형식은 다음과 같습니다.

```
https://eth-mainnet.g.alchemy.com/v2/YOUR_API_KEY
```

여기서 `YOUR_API_KEY` 부분을 실제 발급받은 API Key로 바꾸면 됩니다.

예를 들어 TRXAPI는 TRON 에너지 임대와 관련된 별도의 서비스이며, Alchemy의 Ethereum RPC Endpoint와는 다른 서비스입니다.

## 6. API Key 정상 작동 여부 테스트하기

API Key를 복사한 후 실제 요청을 보내 정상적으로 작동하는지 확인할 수 있습니다.

### 6.1 테스트 명령어

터미널이나 명령줄 도구를 열고 다음 명령어를 실행합니다.

`YOUR_API_KEY`를 본인의 실제 API Key로 변경하세요.

```
curl https://eth-mainnet.g.alchemy.com/v2/YOUR_API_KEY \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"eth_blockNumber","params":[],"id":1}'
```

### 6.2 응답 결과 확인

요청이 정상적으로 처리되면 다음과 비슷한 JSON 응답을 받을 수 있습니다.

```
{
  "jsonrpc": "2.0",
  "id": 1,
  "result": "0x..."
}
```

`result` 항목에 블록 번호가 반환되면 API 요청이 정상적으로 처리된 것입니다.

반대로 오류가 발생한다면 API Key, Endpoint, 네트워크 설정 및 요청 형식을 확인해야 합니다.

## 7. Alchemy API Key 사용 시 주의사항

API Key를 발급받은 후에는 안전하게 관리해야 합니다.

### 7.1 API Key를 공개하지 마세요

API Key를 공개된 GitHub 저장소, 공개 문서 또는 클라이언트 코드에 그대로 입력하지 않는 것이 좋습니다.

가능하면 환경 변수나 서버 측 설정을 사용해 관리하세요.

### 7.2 API Key와 Access Key의 차이점 이해하기

Alchemy는 API Key 외에도 Access Key와 관련된 관리 기능을 제공합니다.

두 항목은 사용 목적과 관리 방식이 다를 수 있으므로, 프로젝트에서 어떤 인증 방식이 필요한지 공식 문서를 확인한 후 사용하세요.

### 7.3 올바른 네트워크 Endpoint 사용하기

Ethereum Mainnet과 Ethereum Sepolia 등 네트워크마다 Endpoint가 다릅니다.

테스트넷과 메인넷을 혼동하지 않도록 주의하세요.

### 7.4 API 사용량 및 요금 확인하기

Alchemy 계정의 사용량과 요금 관련 정보를 정기적으로 확인하는 것이 좋습니다.

프로젝트 규모에 따라 사용량이 달라질 수 있으므로, 본인의 계정에 적용되는 요금 정책을 확인하세요.

## 8. Alchemy 가입 및 API Key 관련 FAQ

### Q1: Alchemy 가입은 무료인가요?

Alchemy는 무료로 시작할 수 있는 요금제를 제공하지만, 기능과 사용량에는 제한이 있을 수 있습니다. 최신 요금과 사용 한도는 공식 웹사이트에서 확인하세요.

### Q2: API Key를 찾을 수 없으면 어떻게 해야 하나요?

Alchemy Dashboard에 로그인한 다음 Apps 메뉴에서 해당 앱을 선택하세요. 앱 상세 페이지에서 API Key와 Endpoints 정보를 확인할 수 있습니다.

### Q3: 여러 개의 API Key를 만들 수 있나요?

프로젝트와 앱 관리 방식에 따라 여러 앱과 관련 API 인증 정보를 관리할 수 있습니다. 구체적인 생성 및 관리 기능은 Dashboard와 공식 문서를 확인하세요.

### Q4: API Key를 다른 사람과 공유해도 되나요?

공개적으로 공유하는 것은 권장하지 않습니다. API Key가 노출되면 다른 사람이 해당 키를 사용해 요청을 보낼 수 있으므로 보안에 주의해야 합니다.

### Q5: API Key를 입력했는데 작동하지 않는 이유는 무엇인가요?

다음 사항을 확인해 보세요.

- API Key를 정확하게 복사했는지 확인합니다.
- Endpoint 주소가 올바른지 확인합니다.
- 선택한 블록체인 네트워크가 맞는지 확인합니다.
- API 요청 형식이 올바른지 확인합니다.
- 계정의 사용량 제한이나 서비스 상태를 확인합니다.

## 9. 마무리

Alchemy는 Web3 개발자에게 블록체인 연결과 데이터 조회 기능을 제공하는 인프라 플랫폼입니다.

Alchemy 계정을 만들고 API Key를 발급받는 전체 과정은 다음과 같습니다.

1. Alchemy 공식 웹사이트에 접속합니다.
2. 이메일 또는 지원되는 로그인 방식으로 가입합니다.
3. Dashboard에 로그인합니다.
4. Apps 메뉴에서 새 앱을 생성합니다.
5. 사용할 블록체인 네트워크를 선택합니다.
6. 앱 상세 페이지에서 API Key를 복사합니다.
7. Endpoint를 이용해 API 요청을 테스트합니다.

이 단계를 완료하면 Alchemy API를 Web3 프로젝트에 연결해 사용할 수 있습니다.

온라인 결제에 사용할 가상 카드 서비스가 필요하다면 CoinePay를 별도로 확인할 수 있습니다.

👉 [https://www.coinepay.net/register?referrer=RFGSSDZ9](https://www.coinepay.net/register?referrer=RFGSSDZ9)

TRON 네트워크의 에너지 임대 서비스에 관심이 있다면 TRXAPI도 참고할 수 있습니다. 이 서비스는 Alchemy와 별개로 운영됩니다.

👉 [https://login.trxapi.io/energy](https://login.trxapi.io/energy)

## 10. Alchemy 공식 참고 자료

가입 및 API Key 발급 과정에 대한 자세한 내용은 Alchemy 공식 문서를 참고하세요.

- 공식 웹사이트: [https://www.alchemy.com/](https://www.alchemy.com/)
- Dashboard: [https://dashboard.alchemy.com/](https://dashboard.alchemy.com/)
- API Key 생성 가이드: [https://www.alchemy.com/docs/create-an-api-key](https://www.alchemy.com/docs/create-an-api-key)
- Quickstart 가이드: [https://www.alchemy.com/docs/alchemy-quickstart-guide](https://www.alchemy.com/docs/alchemy-quickstart-guide)
- Access Key 생성 가이드: [https://www.alchemy.com/docs/how-to-create-access-keys](https://www.alchemy.com/docs/how-to-create-access-keys)

## Google Sites 게시 권장 사항

- 메인 제목은 H1으로 설정합니다.
- 주요 섹션 제목은 H2로 설정합니다.
- 세부 항목은 H3으로 설정합니다.
- 코드 명령어와 JSON 예시는 코드 블록으로 유지합니다.
- 표보다는 짧은 문단과 명확한 소제목을 사용하는 것이 좋습니다.
- CoinePay와 TRXAPI는 Alchemy와 공식 제휴 또는 통합된 서비스가 아니라는 점을 명확히 표시합니다.

