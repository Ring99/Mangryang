## [UNITY 3D] 망량: Detectors
## 1. 소개

<p align="center">
  <img src="https://github.com/user-attachments/assets/c73ddc0c-e62d-484f-a23e-191c03ea9a27" width="30%" />
  <img src="https://github.com/user-attachments/assets/4670fe3d-6ad9-4d43-98c1-c2c546f4b578" width="30%" />
  <img src="https://github.com/user-attachments/assets/20d9ea3a-a6d2-4a59-ba4f-26df5a5a379b" width="30%" />
</p>

- Unity URP로 제작된 2.5D 덱빌딩 로그라이트 모바일 게임입니다.
- 플레이어블 캐릭터를 성장시키고 부적을 해금하는 슬레이더 스파이어 방식의 전투스타일입니다.
- 동양 세계관 기반의 캐릭터 4명의 고유 부적들과 유물, 필살부를 조합하여 다채로운 방식으로 전투를 진행하는 게임입니다.
- 배틀씬 매커닉을 담당하였으며 전투, 맵, 부적등 전투에 필요한 요소들을 개발했습니다.저장

## 2. 개발환경
- UNITY 2020.3.25f1 / URP / C#
- Visual Studio 2019
- Windows 10
- 2025.01 ~ 2026.04 (16개월)
- 개발 2명, 기획 1명, 디자인 2명

## 3. 사용기술
- 디자인 패턴 : Single Tone 패턴으로 매니저 관리
- Object Pooling : 부적, 유물, 아이콘, 파티클 등 생성되는 객체를 풀링
- Save : 데이터를 json으로 변환화여 저장
- Spine Animation : 스파인 4.1 버전 사용, 모든 캐릭터의 모션을 스파인 적용
- Dotween : 카드, 캐릭터 등 인게임 연출적 요소 전반에 활용
- Cinemachine : 전투씬에서 동적 카메라 연출을 위해 사용
- PostProcessing : 모바일 성능에 영향을 주지 않는 선에서 후처리 사용

## 4. 기능구현
- 카드를 드래그 앤 드롭으로 사용  
    Physics.Racast 와 UI GrapicRaycaster를 병행 사용하여 터치 좌표를 변환하였으며 카드 와 몬스터 UI가 유기적으로 선택되게 구현하였습니다.  
- 덱/핸드 관리  
    덱, 핸드, 묘지 분리 관리 상황에 따라 특정 위치에있는 카드를 재투입하는 셔플백 시스템 구현  
    핸드의 카드를 Lerp로 좌우 기준점 사이를 보간하며 곡률 및 기울기를 계산하여 자연스럽게 배치하였습니다.  
- 데미지 계산 시스템  
    카드의 자체 데미지를 기준으로 실드, 캐릭터의 능력치 및 관통 파쇄효과 버프 디버프등 상황에 따라 변경된 수식들을 적용하여  
    카드를 사용할때 종합 처리하여 수치를 결정합니다.  
- 몬스터  
    가중치가 부여된 랜덤 선택으로 행동을 결정하며 공격, 방어, 대기, 스킬사용의 스테이트가 있습니다.  
    몬스터의 월드 좌표를 스크린 좌표로 변환화여 몬스터 전용 UI(HP바, 이름 등 텍스트)를 추적하여 표시하게 하였습니다.  
- 스파인  
    전달받은 스파인 4.1 버전 데이터를 유니티에서 SkeletonAnimation으로 처리했습니다.  
    전투 상황에 맞는 애니메이션이 재생되도록 구현하였습니다.  
- 데이터매니저  
    DataManager에서 TSV를 로드 후 파싱합니다.  
    캐릭터 와 몬스터의 스탯 데이터, 카드, 유물, 맵등 플레이어 정보를 제외한 모든 데이터를 가져옵니다.  
- 어드레서블  
    방대한 이미지 데이터는 아틀라스화 하여 서버에서 추가 다운로드할 수 있도록 구현  

## 5. 플레이영상
- 공식영상: https://youtube.com/shorts/n3z2TIVdpZ8?si=5MMxm6XP9ThLidSV

## 6. 링크
- [https://store.steampowered.com/app/3920940/_/](https://play.google.com/store/apps/details?id=com.ableane.Detecters&hl=ko)
