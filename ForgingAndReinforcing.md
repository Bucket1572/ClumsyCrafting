단조와 강화
===

개요
---
본 플러그인에서는 모루와 대장장이 작업대로 단조 작업과 강화 작업을 할 수 있습니다.

단조 작업
---
본래 강철을 두드려 용도에 맞게 가공하는 것을 [단조법](https://www.tlv.com/global/KR/steam-theory/casting-and-forging.html) 이라 합니다.
본 플러그인에서는 두드려서 가공한다는 컨셉만을 차용하였습니다.
모루 위에서 강철을 버리면, 단조 작업을 시작할 수 있습니다.
단조 작업 중인 모루는 파괴할 수 없으며, 사용할 수도 없습니다. _단, 추가 단조 작업을 할 수는 있습니다._
단조 작업을 시작한 사람에게는 단조 작업 중이라는 알림이 규칙적으로 발송되며, 단조 작업을 마쳤을 때, 끝났음을 알려줍니다.
단조 작업이 끝나면, 모루에서 폭죽이 터지고, 강철은 0.3 만큼 [자체 품질](Quality.md) 이 증가합니다.
품질이 최대 품질을 넘어가면, 품질은 최대 품질로 고정됩니다.

강화 작업
---
철을 제외한 다른 아이템도 품질을 올릴 방법이 있어야 하기에 강화 작업을 추가하였습니다.
강화 작업은 대장장이 작업대 위에서 아이템을 버리는 방식으로 시작할 수 있습니다.
다만, 철괴와 다이아몬드 도구는 강화 작업 처리 할 수 없습니다.
강화 작업 중인 작업대 역시 파괴할 수 없으며, 사용할 수도 없습니다. _단, 추가 강화 작업을 할 수는 있습니다._
강화 작업을 시작한 사람에게는 강화 작업 중이라는 알림이 규칙적으로 발송되며, 강화 작업을 마쳤을 때, 끝났음을 알려줍니다.
강화 작업이 끝나면, 작업대에서 폭죽이 터지고, 아이템은 0.5 만큼 [자체 품질](Quality.md) 이 증가합니다.
품질이 최대 품질을 넘어가면, 품질은 최대 품질로 고정됩니다.

프로페셔널한 강화 작업
---
기본적으로 대장장이 작업대 위에서는 항상 강화 작업이 가능합니다.
하지만, 책장을 추가함으로써 강화 작업의 안전성을 키울 수 있습니다.
대장장이 작업대 한 칸 아래를 기준으로 3 * 3 구역 내, 정중앙을 제외한 구역에 놓여있는 책장의 개수만큼 강화 작업의 안정성이 커집니다.

강화 가챠
---
강화 작업에는 운이 필요합니다.
기본적으로 안정성을 키우지 않은 강화 작업은, 파괴 확률이 22%, 실패 확률이 40%, 성공 확률이 38%입니다.
책장의 품질의 총합과 작업대의 품질의 2배를 합한 값을 α라 하였을 때, 파괴 확률은 (22 - 2×α)%, 실패 확률은 (40 - 3×α)%, 성공 확률은 (38 + 5×α)%입니다.
<details>
<summary>확률 계산 예시</summary>

* 품질이 0.2, 0.5, 0.7인 책장을 사용하고, 대장장이 작업대의 품질이 0.8이라 하자.
* 계수 α = 0.2 + 0.5 + 0.7 + 0.8 × 2 = 3.0
* 따라서, 파괴 확률은 22 - 2 × 3.0 = 16, 16%이다.
* 실패 확률은 40 - 3 × 3.0 = 31, 31%이다.
* 성공 확률은 38 + 5 × 3.0 = 100 - (16 + 31) = 53, 53%이다.

</details>

책장의 개수가 최대가 되면, 파괴 확률이 2%, 실패 확률이 10%, 성공 확률이 88%인 상태로 강화 작업을 시행할 수 있습니다.

세공 작업
---
모든 아이템의 품질을 올릴 수 있지만, 그만큼 더 힘들고 더 가-챠 성격이 강한 작업입니다.
세공 작업은 인챈트 테이블 위에서 아이템을 버리는 방식으로 시작할 수 있습니다.
세공 작업은 강화 작업과 거의 같습니다. 하지만, 품질의 증가폭이 1.5입니다.

프로페셔널한 세공 작업
---
대장장이 작업대에서 더 안정적으로 강화 작업하는 것과 같은 맥락입니다.
그러나, 이 경우, 실제 인챈트를 하듯이 책장을 5*5의 테두리에 두르면, 그 책장이 도움을 줍니다.

세공 가챠
---
책장의 품질의 총합과 인챈트 테이블의 품질의 4배를 합한 값을 α라 하였을 때, 파괴 확률은 (22 - 1×α)%, 실패 확률은 (40 - 1.5×α)%, 성공 확률은 (38 + 2.5×α)%입니다.

재가공 작업
---
품질이 좋은 칼, 갑옷, 도끼, 낚싯대의 능력치를 더 좋게 만들 수 있습니다.
재가공 작업은 조합대 위에서 칼, 갑옷, 도끼, 낚싯대를 버리면 시작할 수 있습니다.
재가공 작업은 단조 작업과 거의 똑같습니다.
재가공 작업이 완료되면, 칼, 도끼의 경우 공격력이, 갑옷의 경우 방어도가, 낚싯대의 경우 행운이 증가합니다.

칼, 도끼의 공격력 계산법은 다음과 같습니다.
* 0.75 * (원래 공격력) + 1.25 * (품질) * (원래 공격력)

따라서, 최대 품질일 때 원래 공격력의 2배가 됩니다.

갑옷의 방어도 계산법은 다음과 같습니다.
* 0.75 * (원래 방어도) + 1.25 * (품질) * (원래 방어도)

따라서, 최대 품질일 때 원래 방어도의 2배가 됩니다.

낚싯대의 행운 계산법은 다음과 같습니다.
* -2 + 5 * (품질)

따라서, 최대 품질일 때 행운이 3 증가합니다.
재가공 작업을 1번 진행하면, 재가공 태그가 붙습니다. 
재가공 태그가 붙은 물건은 재가공 작업할 수 없습니다.

작업대 강화
---
이미 설치한 훈연기, 화로, 용광로, 작업대, 대장장이 작업대, 모루, 인챈트 테이블 역시 강화할 수 있습니다.
아래에서는 이 모두를 아우르는 대명사로 작업대를 사용했습니다.

* 훈연기, 화로, 용광로의 경우 : 석탄 / 목탄 / 석탄 블록을 들고 좌클릭하면, 해당 재료의 자체 품질만큼 작업대의 자체 품질이 증가합니다.
* 상자, 작업대의 경우 : 목재를 들고 좌클릭하면, 해당 재료의 자체 품질만큼 작업대의 자체 품질이 증가합니다.
* 대장장이 작업대의 경우 : 매끄러운 돌을 들고 좌클릭하면, 해당 재료의 자체 품질만큼 작업대의 자체 품질이 증가합니다.
* 모루의 경우 : 철괴를 들고 좌클릭하면, 해당 재료의 자체 품질만큼 작업대의 자체 품질이 증가합니다.
* 인챈트 테이블의 경우 : 다이아몬드를 들고 좌클릭하면, 해당 재료의 자체 품질만큼 작업대의 자체 품질이 증가합니다.
* 책장의 경우 : 책을 들고 좌클릭하면, 해당 재료의 자체 품질만큼 책장의 자체 품질이 증가합니다.

작업대 강화에는 시간이나 갓-챠가 필요 없습니다.