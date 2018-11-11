# FDS11 중간 프로젝트

쇼핑몰 구현하기

---

## 기능

- 최소 요구사항
  - 사용자는 **로그인**을 할 수 있습니다.
  - 사용자는 **카테고리**별 **상품 목록 페이지**를 이용할 수 있습니다.
  - 사용자는 **상품 페이지**를 통해 상품에 대한 자세한 정보를 확인할 수 있습니다.
  - 사용자는 **장바구니에 상품을 담거나 장바구니에서 상품을 제거**할 수 있습니다.
  - 사용자는 장바구니에 담긴 항목 **전체를 주문**할 수 있습니다.
  - 사용자는 **주문 내역을 확인**할 수 있습니다.
- 추가 요구사항
  - 사용자는 **회원 가입**을 할 수 있습니다.
  - 사용자는 장바구니 항목의 **구매 수량을 수정**할 수 있습니다.
  - 사용자는 장바구니에 담긴 항목 중 주문하고 싶은 것만 **선택해서 주문**할 수 있습니다.
  - 사용자는 상품 목록에서 **페이지**를 넘기며 상품을 탐색할 수 있습니다.
  - 관리자는 별도의 **관리자 페이지**에서 상품을 추가/수정/삭제할 수 있습니다. (id가 1번인 사용자를 관리자로 간주합시다.)

---

## 초기 기획

### 주제

장난감 쇼핑몰

### 페이지 기획 단계

1. 기능을 페이지 사용 흐름에 따라 그려본다.

- 로그인 버튼
  - 로그인 페이지 이동
    - 로그인 성공 시 메인 페이지로 이동

(로그인 중)
- 카테고리 클릭
  - 해당 카테고리 상품 목록 페이지 이동
    - 상품 선택
      - 해당 상품 상세페이지 이동
        - 장바구니
          - 장바구니 페이지로 이동
            - 상품 제거 기능
            - 전체 주문
              - 주문 내역 페이지로 이동
        - 즉시 주문
          - 주문 내역으로 바로 이동

2. 1번을 토대로 페이지를 나누고, 각 페이지에 필요한(원하는) 요소를 생각한다.
  - 메인 페이지
    - new arrival
    - 이미지만

  - 로그인 페이지
    - 로그인 폼

  - 상품 목록 페이지
    - 해당 카테고리 아이템들 모두 정렬
    - 이미지, 이름, 가격 표시

  - 상품 상세페이지
    - 이미지와 상품 이름, 상세 정보
    - 상세 정보
      - 디테일한 상품 이름
      - 주문 수량 선택 기능
      - 주문 수량에 맞춰 금액 표시
      - 장바구니 담기 버튼
      - 주문하기 버튼

  - 장바구니 페이지
    - 이미지, 상품 이름, 선택한 수량, 수량에 따른 금액 표시
    - 해당 상품 제거 버튼
    - 수량 변경 기능

  - 주문 내역 페이지
    - 장바구니 페이지에서 주문한 뭉탱이 그대로 표시(수량변경, 제거버튼 제외)
    - 주문 건 별로 정렬


  ### 일정

  1. 1일차(11/7) - 상품 상세 페이지 기능까지 완료. 가능하면 카트페이지 건드려보기
  2. 2일차(11/8) - 카트 페이지, 주문 내역 페이지 기능까지 완료 - 최소 기능 구현 완료
  3. 3일차(11/9) - css 완료, 가능하면 추가 기능 구현 시도.

  ### 목표

  - 최소 기능 구현
  - css 보다 기능 구현을 먼저하자.

  ---

  ## 회고(11/11)

  ### 마감(11/9 18시) 완성도

  85%

  - 최소 기능 구현 완료.
  - 추가 기능 중 장바구니 항목에서 수량 변경 기능 구현.
  - 장바구니 페이지, 주문 내역 페이지 css 미완성.
  - 나머지 페이지 css 마무리까지 완료.

  ### 현재(11/11) 완성도
  - 못한 css 마무리 완료.
  - 디버깅.
  - 회원가입 기능 추가.

  ### 소감

  1. 기획 단계에서는 머릿속에서만 그려보는거라 내가 구현을 할 수 있든 말든 신나게 했는데 막상 기획을 다 해가니까 내가 과연 할 수 있을까 싶었다.

  2. 그래도 어쨌든 시작은 해야하니 시작해봤다.

  3. 기획 단계를 거치다보니까 머릿속에 완성본이 떠다녀서 처음부터 완성된 모습을 목표로 기능을 구현하려니 걱정만 되고 지금 당장 일순위가 아닌 기능들이 자꾸 생각의 꼬리를 물고 이것때문에 집중력이 산으로 가는 것 같아서 한 페이지, 한 페이지씩 단계 별로 완성해보려고 노력했고, 해당 페이지 기능 구현할 땐 해당 페이지에 없는 기능은 아예 생각하지 않았다.

  4. 좋은 방법이었던 것 같다. 다음 단계를 할 수 있을지 없을지 걱정하기 전에 일단 지금 단계를 완성시켜놓으니까 어떻게든 다음 단계를 시작하게됐고, 일단 시작하니까 걱정과는 달리 내가 뭐라도 생각해내더라. 그래서 다음 단계는 나중의 나에게 맡기고 지금 단계에 집중하는 방식으로 프로젝트 전반을 임했다.

  5. 카트페이지가 가장 까다롭고 주문 내역은 그냥 카트페이지를 통째로 가져가면 될 거라 생각했는데, 주문 내역 페이지가 최종 보스였다. 다행히 강사님과의 중간 트러블슈팅 시간 전에 주문 내역 페이지 구현을 시작했고, 어느정도 삽질해보다가 트러블슈팅을 진행하게 되어서 많은 도움이 됐고 덕분에 시간 낭비를 덜 했다.

  6. 비록 css는 완벽히 마무리하진 못해서 아쉬웠지만 생각보다 기능 구현을 빨리 끝내서 뿌듯했다.

  7. 하지만 완성하고보니 코드가 너무 더럽다ㅜㅜ 어떻게든 구현만하려고 그냥 막 짜다보니... 어디서부터 정리해야할지 감도 안잡힌다. 이게 마감에 쫒겨 스토리가 안드로메다로 가던 작가들의 심정인가ㅜㅜ...

  8. 그리고 html 클래스 네이밍이 진짜진짜 지옥이었다. 쳐다보기도 무섭다. 클래스 작명소가 필요하다.

  9. 디자인은 예쁜 사이트를 찾아서 벤치마킹했다.

  10. 처음부터 끝까지 내가 기획하고 만들어볼 수 있어서 좋은 기회였다고 생각한다. 덕분에 지금까지 배운 템플릿과 데이터 요청을 주구장창 써보면서 조금이나마 친해졌고, 데이터 구조에서 미아가 됐었다가 지금은 지도보고 목적지 찾기 정도는 할 수 있게 됐다. 많이 얻어가는 것 같다.

  ### 추가로 해보고 싶은 것

- 추가 요구사항 중 구현하지 못한 사항들.
  - 사용자는 장바구니에 담긴 항목 중 주문하고 싶은 것만 **선택해서 주문**할 수 있습니다.
  - 사용자는 상품 목록에서 **페이지**를 넘기며 상품을 탐색할 수 있습니다.
  - 관리자는 별도의 **관리자 페이지**에서 상품을 추가/수정/삭제할 수 있습니다. (id가 1번인 사용자를 관리자로 간주합시다.)

- 주문 내역 최신 순으로 정렬

- 장바구니에 동일한 상품이 존재하면 장바구니에 새로 아이템 추가 하지 않고 기존 장바구니 아이템에서 수량만 추가.

- 로그인 된 상태일 시 로그인/회원가입 버튼 대신 마이페이지/로그아웃 버튼으로 교체하기

- 모바일 반응형 디자인

- 가격 (,) 구분

- 옵션 추가

- 코드 정리(?)

