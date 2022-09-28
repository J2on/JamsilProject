# JamsilProject

잠실대교는 왜 막히는 거야 - 기획서
=======================

## 목차
> >1. 게임개요
> > >1) 제목
> > >2) 플랫폼
> > >3) 배경-스토리
> > >4) 배경-지리적
> > >5) 클리어 조건
> > >6) 주요 오브젝트
> > >
> >2. 게임플레이
> > >1) 시점
> > >2) 골드 획득
> > >3) 게임 조작법
> > > >1) 유닛 이동방법
> > > >2) 유닛 생성방법
> > > >3) 전투방식
> > >4) 적 AI

> >3. 게임유닛
> > >0) 저격수
> > >1) 지상유닛
> > >2) 수중유닛
> > >3) 공중유닛

> >4. 개발
> > >1) 에셋 명명법
> > >2) 변수 명명법

## 1. 게임개요
> >### 제목
> > >잠실대교는 왜 막히는거야
> >### 플랫폼
> > > Desktop
> >### 배경-스토리
> > > 잠실대교의 이름에 불만을 가진 '건대주민연합'이 잠실대교의 이름을 '건국대교'로 변경하기 위해 '잠실주민연합'과 마찰을 빚음. 이것이 전쟁으로 발전.
> >### 배경-지리적
> > > 잠실대교 인근. 한강을 기준으로 북쪽으로는 건국대학교 일감호, 남쪽으로는 석촌호수를 포함함.
> >### 클리어 조건
> > > 플레이어는 잠실 진영으로 전투에 참가하며 상대 건대 진영의 요새(육군기지)의 HP를 0으로 만드는 경우 승리, 상대 진영의 유닛에 의해 아군 진영의 요새의 HP가 0이 되는 경우 패배한다.
> >### 주요 오브젝트
> > > 잠실대교
> > > >잠실대교는 지상유닛이 상대 진영으로 넘어갈 수 있는 유일한 통로로, 두 진영의 지상유닛 간의 주된 전투지역으로 활용됨.

> > > #### 기지
> > > > 공통- 육군기지, 해군기지, 공군기지는 각각 HP를 보유.    각각 지상유닛, 수상유닛, 공중유닛을 생산할 수 있으며 유닛 생산방식은 각각의 기지를 클릭하여 생성되는 UI에서 생성하고자하는 유닛과 숫자를 선택해 특정위치에 스폰되는것으로 함.   
> > > > ##### 육군기지(요새)
> > > >  건대진영은 광양고등학교, 잠실진영은 롯데월드에 위치하며 최종 요새로써 HP가 0이 되면 게임이 종료됨. 
> > > > > 업그레이드 : 지상유닛 공격력 ↑, 요새 HP ↑, 요새에 저격수 배치 + 업그레이드는 한번으로 제한함. 
> > > > > 
> > > > > +일정 골드 지불 시 요새의 HP 증가 및 육군 지상유닛의 공격력이 증가되며 육군기지에 저격수가 배치됨   
> > > > > +저격수는 별개의 유닛이 아닌 육군기지에 종속되는 육군기지의 공격옵션으로 여겨짐. 다만, 저격수는 별개의 HP를 보유하며 요새가 공격받는 경우에 HP를 소모함.   
> > > > > 
> > > > ##### 해군기지
> > > >  건대진영은 일감호, 잠실진영은 석촌호수에 위치하며 HP가 0이 되면 폭파 효과와 함께 더이상 수상유닛을 생성할 수 없음
> > > >   
> > > > ##### 공군기지 
> > > >  건대진영은 스타필드, 잠실진영은 롯데타워에 위치하며 HP가 0이 되면 폭파 효과와 함께 더이상 공중유닛을 생산할 수 없음.

## 2. 게임플레이
> > ### 시점
> > > 기본적으로 탑뷰 시점을 활용하며, 마우스의 움직임에 따라 맵 내에서는 자유롭게 이동이 가능    ex) 리그오브레전드, 로스트아크 참조
> > ### 골드 획득
> > > 지상유닛이 골드를 획득하는 장소에 위치하거나 해당장소에서 상호작용을 할 때에 해당 지상유닛의 숫자에 비례하여 골드를 획득
> > ### 게임 조작법
> > > #### 유닛 이동방법
> > > ##### 공통
> > > - 유닛은 개별이동 및 드래그를 이용한 다수 선택으로 군집 이동이 가능.   
> > > - 선택된 유닛(혹은 군집)은 마우스 클릭지점으로 이동.
> > > #### 유닛 생성방법
> > > - 유닛은 각각의 기지에 지정된 스폰장소에 스폰됨.   
> > > - 유닛을 생성하는 ui창은 각각에 해당되는 기지를 더블클릭하여 화면에 표출하며 ui창에서는 어떠한 유닛을 얼마나 생성할지 선택할 수 있어야 함.   
> > > #### 전투방식
> > > ##### - 공통
> > > > 컨트롤 하고 있는 유닛(혹은 군집)이 있을때 상대 유닛(군집)을 마우스로 클릭하면 전투명령으로 인지 
> > > > 모든 유닛은 적 건물이 사정거리 내에 있을때 타격이 가능
> > > ##### - 지상유닛
> > > > 지상유닛은 근거리와 원거리로 구분되지만, 원거리 유닛이 공중유닛이나 수상유닛을 타격하는 것은 불가능함.    
> > > > 지상 >> 지상 타격가능
> > > ##### - 수상유닛
> > > > 수상 >> 수상 타격 가능   
> > > > 수상유닛이 적 진영에 상륙하여 지상유닛으로 전환되는 경우 지상유닛을 타격할 수 있음
> > > ##### - 공중유닛
> > > > 공중 >> 공중, 공중 >> 수상, 공중 >> 지상 타격 가능  
> > > > 공중유닛은 원거리 유닛으로써 상대 모든 유닛에 타격이 가능함
> > ### 적 AI
> > > - 적 AI는 기본적으로 AI컨트롤러에 골드를 지불하여 유닛을 생성하는 비헤이비어 트리를 추가하여 구현한다.  
> > > 다만, AI컨트롤러의 복합적인 구현이 어려운 경우에 일정 시간에 맞춰 상대 유닛이 생성되는 것으로 한다.   
> > > 적 AI의 유닛들은 각각의 AI컨트롤러를 통해 이동하며 아군 유닛들을 공격한다.
>
## 3. 게임유닛
> > ### 0) 저격수
> > > 저격수는 유닛이지만 메쉬를 가지지 않으며 육군기지(요새)에 종속된다.  
> > > 저격수는 요새와 별도의 HP를 가지며 요새가 공격받는 경우에 HP가 감소하며, HP가 모두 감소하면 저격수는 소멸한다.   
> > > 공격범위 내에 진입한 공중유닛을 우선으로 공격하며, 수 초에 한 번씩 상대에게 가해지는 공격 데미지는 지상유닛보다 높게 형성된다.  
> > ### 1) 지상유닛
> > > 지상유닛은 근거리 유닛과 원거리 유닛으로 나뉜다.   오직 잠실대교를 통해서만 상대 진영으로 이동이 가능함.  
> > > > - 근거리 유닛
> > > > 체력↑/ 공격력↓  
> > > > - 원거리 유닛
> > > > 체력↓/ 공격력↑  
> > ### 2) 수상유닛
> > > 수상유닛은 수상전투 및 상대 진영으로의 상륙을 통한 지상유닛으로의 변환을 목표로 함.   필요시 추가 가능   
> > > 상륙은 상대 진영의 지정된 장소에서만 가능함.
> > > > - 오리배(가정) 유닛 
> > > > 오리배 유닛 한 개는 지상유닛 10개로 변환이 가능함(추후 수정 가능). 수중에서는 근거리 전투만이 가능.   
> > > >  이동속도↓ / 가격 ↑
> > ### 3) 공중유닛
> > > 공중유닛은 기본적으로 원거리 공격을 사용하며 적 모든 유닛 및 오브젝트를 타격이 가능함   
> > > 적 공중유닛과 저격수만이 공중유닛의 타격이 가능함.
> > > > - 열기구(가정) 유닛
> > > > 이동속도↑ 공격력↑ / 가격 ↑↑ 체력 ↓

## 4. 개발
> > 프로젝트 개발은 블루프린트로 제작을 베이스로 하며 필요시 C++를 사용함.
> > ### 1)에셋 명명법
> > 에셋스토어에서 필요한 에셋들을 가져올때 지켜야할 점.
> > > 0) 기본적으로 콘텐츠종류_이름_순번 의 구성을 사용 함.   (최초 파일은 00, 다음 파일은 01, 다음 파일은 02 ...)   
> > >  ex) 3개의 풀 스태틱메시를 가져왔을때 두번째 풀 메시의 이름은 SM_grass02_00으로 명명.
> > > 1) 레벨 - LV_레벨이름_00   
> > > 2) 머터리얼 - M_머터리얼이름_00 
> > > 3) 블루프린트클래스 - BP_블루프린트이름_00 
> > > 4) 스켈레탈 메시 - SKM_메시이름_00
> > > 5) 텍스처 - T_텍스처이름_00   
> > > 로 작성을 하며 이 외의 케이스는 [링크](https://github.com/VLAST-GIT/UE5-StyleGuide#9-%EB%A0%88%EB%B2%A8%EB%94%94%EC%9E%90%EC%9D%B8)의 1.2 부분을 참고   
> > > 2) 블루프린트 명명법
> > > 블루프린트 파일의 경우 앞서 언급한 BP_이름_00으로 작성하며 블루프린트 내에 작성하는 변수 및 함수의 경우에는 파스칼 케이스를 사용함.   
> > > 파스칼케이스는 각 단어를 띄어쓰기 없이 붙여 사용하며 각 단어의 첫 글자를 대문자로 작성하는 방법   
> > > ex) PascalCase, EatBread, KickABall, IsTrue
