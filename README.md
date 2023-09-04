# 키친포스

## 퀵 스타트

```sh
cd docker
docker compose -p kitchenpos up -d
```

## 요구 사항

### 상품

- 상품을 등록할 수 있다.
- 상품의 가격이 올바르지 않으면 등록할 수 없다.
    - 상품의 가격은 0원 이상이어야 한다.
- 상품의 이름이 올바르지 않으면 등록할 수 없다.
    - 상품의 이름에는 비속어가 포함될 수 없다.
- 상품의 가격을 변경할 수 있다.
- 상품의 가격이 올바르지 않으면 변경할 수 없다.
    - 상품의 가격은 0원 이상이어야 한다.
- 상품의 가격이 변경될 때 메뉴의 가격이 메뉴에 속한 상품 금액의 합보다 크면 메뉴가 숨겨진다.
- 상품의 목록을 조회할 수 있다.

### 메뉴 그룹

- 메뉴 그룹을 등록할 수 있다.
- 메뉴 그룹의 이름이 올바르지 않으면 등록할 수 없다.
    - 메뉴 그룹의 이름은 비워 둘 수 없다.
- 메뉴 그룹의 목록을 조회할 수 있다.

### 메뉴

- 1 개 이상의 등록된 상품으로 메뉴를 등록할 수 있다.
- 상품이 없으면 등록할 수 없다.
- 메뉴에 속한 상품의 수량은 0 이상이어야 한다.
- 메뉴의 가격이 올바르지 않으면 등록할 수 없다.
    - 메뉴의 가격은 0원 이상이어야 한다.
- 메뉴에 속한 상품 금액의 합은 메뉴의 가격보다 크거나 같아야 한다.
- 메뉴는 특정 메뉴 그룹에 속해야 한다.
- 메뉴의 이름이 올바르지 않으면 등록할 수 없다.
    - 메뉴의 이름에는 비속어가 포함될 수 없다.
- 메뉴의 가격을 변경할 수 있다.
- 메뉴의 가격이 올바르지 않으면 변경할 수 없다.
    - 메뉴의 가격은 0원 이상이어야 한다.
- 메뉴에 속한 상품 금액의 합은 메뉴의 가격보다 크거나 같아야 한다.
- 메뉴를 노출할 수 있다.
- 메뉴의 가격이 메뉴에 속한 상품 금액의 합보다 높을 경우 메뉴를 노출할 수 없다.
- 메뉴를 숨길 수 있다.
- 메뉴의 목록을 조회할 수 있다.

### 주문 테이블

- 주문 테이블을 등록할 수 있다.
- 주문 테이블의 이름이 올바르지 않으면 등록할 수 없다.
    - 주문 테이블의 이름은 비워 둘 수 없다.
- 빈 테이블을 해지할 수 있다.
- 빈 테이블로 설정할 수 있다.
- 완료되지 않은 주문이 있는 주문 테이블은 빈 테이블로 설정할 수 없다.
- 방문한 손님 수를 변경할 수 있다.
- 방문한 손님 수가 올바르지 않으면 변경할 수 없다.
    - 방문한 손님 수는 0 이상이어야 한다.
- 빈 테이블은 방문한 손님 수를 변경할 수 없다.
- 주문 테이블의 목록을 조회할 수 있다.

### 주문

- 1개 이상의 등록된 메뉴로 배달 주문을 등록할 수 있다.
- 1개 이상의 등록된 메뉴로 포장 주문을 등록할 수 있다.
- 1개 이상의 등록된 메뉴로 매장 주문을 등록할 수 있다.
- 주문 유형이 올바르지 않으면 등록할 수 없다.
- 메뉴가 없으면 등록할 수 없다.
- 매장 주문은 주문 항목의 수량이 0 미만일 수 있다.
- 매장 주문을 제외한 주문의 경우 주문 항목의 수량은 0 이상이어야 한다.
- 배달 주소가 올바르지 않으면 배달 주문을 등록할 수 없다.
    - 배달 주소는 비워 둘 수 없다.
- 빈 테이블에는 매장 주문을 등록할 수 없다.
- 숨겨진 메뉴는 주문할 수 없다.
- 주문한 메뉴의 가격은 실제 메뉴 가격과 일치해야 한다.
- 주문을 접수한다.
- 접수 대기 중인 주문만 접수할 수 있다.
- 배달 주문을 접수되면 배달 대행사를 호출한다.
- 주문을 서빙한다.
- 접수된 주문만 서빙할 수 있다.
- 주문을 배달한다.
- 배달 주문만 배달할 수 있다.
- 서빙된 주문만 배달할 수 있다.
- 주문을 배달 완료한다.
- 배달 중인 주문만 배달 완료할 수 있다.
- 주문을 완료한다.
- 배달 주문의 경우 배달 완료된 주문만 완료할 수 있다.
- 포장 및 매장 주문의 경우 서빙된 주문만 완료할 수 있다.
- 주문 테이블의 모든 매장 주문이 완료되면 빈 테이블로 설정한다.
- 완료되지 않은 매장 주문이 있는 주문 테이블은 빈 테이블로 설정하지 않는다.
- 주문 목록을 조회할 수 있다.

## 용어 사전
### 메뉴
![menu](https://user-images.githubusercontent.com/22831002/265471870-58cf648c-7cc0-40a7-a76c-27feba74905b.png)


| 한글명 | 영문명 | 설명 |
| -- | -- | -- |
| 메뉴 그룹 | menu group | 메뉴들을 그룹화하는 카테고리를 의미한다. 예르 들어 '디저트', '메인 요리' '사이드' 등과 같이 여러 메뉴들을 분류할 때 사용된다. | 
| 메뉴 그룹명 | menu group name | 메뉴 그룹의 이름, ( 세트메뉴그룹, 디저트메뉴그룹, 단품메뉴그룹, 추가서비스료메뉴그룹 ) |
| 메뉴 | menu | 메뉴 그룹에 속하는 것으로 판매 가능한 서비스의 항목을 의미한다. 메뉴는 이름, 가격, 관련상품정보, 전시여부와 같은 정보를 지닌다. ( 세트메뉴1번, 단일메뉴, 룸서비스, 콜라 ) |
| 메뉴명 | menu name | 메뉴의 이름 |
| 메뉴 가격 | menu price | 메뉴를 판매하는 가격 |
| 메뉴 상품 | menu product | 메뉴를 구성하는 상품 ( [치킨,콜라,치킨무], [콜라], [배달료] ) |
| 주문가능 | display | 메뉴가 판매중인 상태 |
| 주문불가 | hide | 메뉴가 판매중단된 상태 |
| 비속어 | profanity | 사전적으로 비속한[불경스런] 말 |  
| 상품 | product | 가격과 이름이 있는 서비스 또는 물건의 정보 ( 예시: 콜라, 사이다, 양념치킨, 배달료, 룸대실료, 무료서비스 ) |  
|상품 이름 | product name | 상품의 이름 |  
| 상품 가격 | product price | 상품의 가격 |


### 주문
![order](https://user-images.githubusercontent.com/22831002/265472916-2c4c8b09-f836-42d2-ac30-5cdf1b01f569.png)

| 한글명          | 영문명 | 설명                                          |
|--------------| --- |---------------------------------------------|
| 주문           | order |                                             |
| 주문 유형        | order type | 주문의 유형 ex) 배달, 포장, 매장식사                     |
| 배달           | delivery | 주문 유형에서 배달 주문                               |
| 포장           | take out | 주문 유형에서 포장 주문 |                               
| 매장식사         | eat in | 주문 유형에서 매장에서 식사하는 경우 |                        
| 주문 상태        | order status | 주문의 진행중인 상태 |
| 주문접수요청       | created | 손님이 주문을 접수한 경우 |                           
| 주문 접수 대기     | waiting | 주문을 요청했으나, 아직 가게에는 접수되지 않은 상태 |              
| 주문 접수 승인     | accepted | 요청한 주문이 가게에 접수된 경우               |           
| 상품 제공됨       | served | - 상품 준비가 완료되어, 손님 또는 배달에 전달 된 경우 |          
| 배달중          | delivering | 주문 상태에서 배달중인 상태 |          
| 배달 완료        | delivered | 주문 상태에서 배달이 완료된것, 주문이 종료된 것은 아니다. |           
| 주문 종료        | completed | 성공여부와 관계없이, 주문이 더 이상 처리될 수 없는 종료된 상태 |        
| 배달대행사        | kitchen riders | 배달을 진행해주는 주체 |     
| 주문내역리스트      | order line | 주문한 메뉴 리스트 |                                 
| 주문내역         | order line item | - 주문안에 있는 한 줄을 의미한다, 주문내역 |                   
| 주문 내역 메뉴     | order line menu | 주문한 메뉴 |             
| 매장 테이블       | order table | 매장 내에 식사할 때의 테이블 |                            
| 점유중인 테이블     | occupied table | 인원수와 무관하게 테이블에 앉는 주문이 정해져있는 테이블 |             
| 점유중이지 않은 테이블 | unoccupied table | 사용중이지 않은 테이블 |        
| 테이블을 비우다     | clear | 테이블의 점유를 해제하는 것, 테이블을 치워서 다른 손님을 받을 수 있는 상태 | 
| 매장 테이블명      | order table name | 매장 테이블 이름 | 
| 테이블 인원 수     | number of guests | 테이블에 앉아 있는 인원 |                               
| 사용중          | occupied | 사용중인 상태 |

## 모델링
