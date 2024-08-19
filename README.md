# 프로젝트 이름
**Elixir-of-Flamel**

## 📖 목차
1. [프로젝트 소개](#프로젝트-소개)
2. [개발기간](#개발기간)
3. [와이어프레임](#와이어프레임)
4. [프로젝트 수행절차](#프로젝트-수행절차)
5. [기술적 의사결정](#기술적-의사결정)
6. [주요기능](#주요기능)
7. [Trouble Shooting](#trouble-shooting)

## 👨‍🏫 프로젝트 소개
1. 다양한 장르가 혼합된 게임을 만들어보며 이를 실현해보고자 함
2. 각 장르의 대표적인 기능들을 적어도 하나 이상씩 구현해보며 최대한 많은 기능을 경험해보고자 함

## ⏲️ 개발기간
- 2024.06.27(목) ~ 2024.08.20(화)

## 와이어프레임
- 초기 구상 로직</br>
[기초 화면 및 로직 구상]
![게임루프](https://github.com/user-attachments/assets/cfd088a9-76a9-456b-973e-e1dd2bcb3cf4) </br>
![필수기능목록](https://github.com/user-attachments/assets/bf8d7731-e08a-4817-aa03-91707c070b04) </br>
![UML](https://github.com/user-attachments/assets/a76e98c4-ddb1-470b-b8bd-25de4d3383e3) </br>


## 프로젝트 수행절차
|구분|기간|활동|
|:---|:---|:---|
사전기획|6/27~7/5|프로젝트 기획 및 UML설계
기본구현|7/5~7/12|필수 유틸 제작, 스테이지별 기본 기능 구현 및 씬 병합
추가 기능구현(1차)|7/13 ~ 7/24|스테이지별 특화 기능 구현 및 디버그
추가 기능구현(2차)|7/25 ~ 8/13|세부 컨텐츠 작업 및 디버그, 빌드
QA|8/14 ~ 8/20|유저 테스트 및 디버그

## 기술적 의사결정
|기술스택|사용이유|결과|
|:---|:---|:---|
제네릭싱글톤|싱글톤을 만들기 위해서 동일한 코드를 반복 작업하기 보다는 제네릭을 활용하여 상속을 통한 싱글톤화가 보다 작업효율을 높이리라고 판단하였습니다.|반복적인 코드가 줄어 불필요한 코드의 양을 줄일 수 있었으며, 반복 작업을 피해 작업효율이 보다 상승하였습니다.
오브젝트 풀|오브젝트 중 생성과 파괴가 빈번하게 일어나는 경우 리소스를 낭비하지 않기 위해서 선택하였습니다.|오브젝트의 생성 및 파괴시 발생하는 성능 하락을 방지할 수 있었습니다.
JSON|게임의 진행 상태를 저장하고 불러오기 위해서 JSON 방식을 선택하였습니다.|JSON 파일을 관리하는 방식을 익혔으며, 데이터 관리의 중요성에 대해서 알게 되었습니다.
Cinemachine|스테이지에서 카메라를 관리 및 통제하고자 Cinemachine의 Confiner 기술을 채택하였습니다.|스테이지에서 불필요한 영역이 가려져 플레이어의 몰입도가 게임 진행 중에 깨지기 않게 되었습니다.
Perlin Noise|채집 스테이지를 랜덤하게 생성하고자 동적생성 방식 중 하나의 필드를 랜덤 생성할 수 있는 Perlin Noise를 선택하였습니다.|난이도와 컨셉에 맞는 다양한 맵을 실시간으로 무작위하게 생성할 수 있게 되어, 플레이어에게 매번 색다른 경험을 제공해 줄 수 있게 되었습니다.
Grid & NavMeshPlus|디펜스 스테이지에서 건축물을 설치하고, 매번 달라지는 경로를 찾아 목표지점으로 이동할 수 있는 적을 구현하고자 해당 기술들을 사용하였습니다.|보다 깔끔하고 정리된 형태로 스테이지를 구성할 수 있게 되었으며, NavMeshPlus의 사용법에 대해 익힐 수 있었습니다.

## 🕹주요기능

1.편의성
  - 설정
    ![설정](https://github.com/user-attachments/assets/919cebe6-8dae-4f46-b084-6161b01ce1c5) </br>
    
  - 튜토리얼</br>  
    ![튜토리얼 기능](https://github.com/user-attachments/assets/1525ff48-418b-4f6b-b381-c930c2790ca7) </br>
    
  - 데이터저장</br>  
    ![저장](https://github.com/user-attachments/assets/51c54d06-e2de-4093-a84a-e72a04faf5e9) </br>
    
  - UI 및 기능
    ![인게임UI](https://github.com/user-attachments/assets/30d1792e-c26c-4d9b-813d-0e7f6cd1d04b) </br>    
 
2.레시피와 조합 시스템
  - 조합</br>  
    ![조합](https://github.com/user-attachments/assets/f416f265-5fea-4e4d-b44e-fa73de2460fc) </br>

  - 레시피</br>  
    ![레시피](https://github.com/user-attachments/assets/6ad7657f-e97d-4af9-83d1-8520e1e7d948) </br>  

3.마을 내 컨텐츠
  - 재배
    ![재배](https://github.com/user-attachments/assets/85ee3c6a-c653-4cf7-ad23-db633ae7c75b) </br>

  - 제작
    ![제작](https://github.com/user-attachments/assets/d190ef3f-cb9a-47e4-8005-85a2f8e291fc) </br>

  - 구호소

    ![구호소](https://github.com/user-attachments/assets/68123852-8212-41a1-9241-5b1b0552c476) </br>    

4.채집 및 전투

  - 스테이지 난이도
    ![채집 스테이지](https://github.com/user-attachments/assets/8477bead-21c5-46e2-acb8-ca36c8341eab) </br>

  - 채집 & 전투
    ![채집과 전투](https://github.com/user-attachments/assets/b8a139ce-ee0c-4312-b3bc-079b262fb86d) </br>

5.Grid & NavMesh

  - Grid</br>
    ![디펜스 설치 및 업그레이드](https://github.com/user-attachments/assets/57268f19-e22e-400b-b5c6-cbf72c5415a6) </br>

  - NavMesh</br>
    ![디펜스 진행](https://github.com/user-attachments/assets/f1f0fa82-7081-47e3-809d-478c544b2105) </br>

5.이벤트와 퀘스트

  - 이벤트
    ![이벤트](https://github.com/user-attachments/assets/7e5e5457-f588-48d2-a9fe-be6b178e0b6e) </br>

  - 퀘스트</br>
    ![퀘스트 내용](https://github.com/user-attachments/assets/8c77df8b-c41b-42bf-87d2-4aeebb0566c6) </br>
    ![퀘스트 수락](https://github.com/user-attachments/assets/0cac06fa-b19c-43f3-9aa8-9c7fdb022022) </br>

## 🛠Trouble Shooting
1. 오디오 실행 및 관리시 마주한 문제
 </br>🐛문제발생
  </br>-효과음이 동시에 실행될 때, 오디오 소스가 1개 이므로 여러 효과음이 동시에 실행되어야 할 때 최적화 문제가 발생
 </br>💡해결
  </br>-오디오 소스의 양을 최대 10개로 제한하고, 동적인 생성 대신 미리 생성시켜둠으로써 최적화 문제를 해결함

![트러블슈팅 오디오](https://github.com/user-attachments/assets/e7130780-6e95-4c57-b68d-569fb28a10ea)</br>
  
 2. 씬 전환시 데이터 관리 문제
  </br>🐛문제발생
   </br>-상호작용 가능한 오브젝트가 Raycast를 통해 감지되도록 설계했으나, 씬 전환시 Missing 오류가 발생
  </br>💡해결
   </br>-감지된 오브젝트가 씬 전환 후에도 변수에 담긴 채로 이동되어 오류가 발생한 것으로, Bool값을 걸어두어 상호작용 중일 때는 Raycast의 사용을 막음으로써 해결함

![트러블슈팅 씬전환 데이터1](https://github.com/user-attachments/assets/7da902b0-592d-4d81-8bd1-1ea920a5c539) </br>
![트러블슈팅 씬전환 데이터2](https://github.com/user-attachments/assets/f1e7dd56-e086-4294-b5c8-60475ca040ab) </br>

 3. 채집스테이지 랜덤 생성시 오브젝트 겹침 문제
  </br>🐛문제발생
   </br>-매번 랜덤하게 생성되는 맵과 오브젝트 중에서 콜라이더 설정된 맵타일과 오브젝트끼리 겹쳐서 생성되는 바람에 원활한 플레이가 불가한 문제
  </br>💡해결
   </br>-오브젝트 생성 시 좌표값을 리스트로 정리해두고, 콜라이더 적용된 맵타일이 생성될 시 해당 리스트의 값을 피해서 설치가 되도록 수정 추가로 안정성을 확보하고자 확장 메서드를 추가함

![트러블슈팅 랜덤맵생성](https://github.com/user-attachments/assets/3e86b2aa-4f3f-44bc-ace2-442046a8cfc3) </br>

 4. 디펜스 스테이지 NavMeshPlus 적용시 발생한 문제
  </br>🐛문제발생
   </br>-스테이지 시작시 적이 생성이 제각각이거나, 사망처리가 된 적이 파괴되지 않고 유지되는 등 수많은 문제가 발생
  </br>💡해결
   </br>-몬스터의 생성 위치가 NavMesh 경로 외부에 존재하였으며, 적의 시작위치 또한 다른 오브젝트의 좌표값을 참조 하고 있었음. 해당 참조를 정상적으로 재설정하고 생성 위치를 NavMesh 경로 안쪽으로 재배치하여 대다수의 문제를 해결
   
![트러블슈팅 디펜스 NavMesh](https://github.com/user-attachments/assets/55fd35ff-caa7-433b-9a0e-d8fd1ecc1f80)

