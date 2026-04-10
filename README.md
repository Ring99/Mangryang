## [UNITY 3D] 망량: Detectors
## 1. 소개

![1](https://github.com/user-attachments/assets/c73ddc0c-e62d-484f-a23e-191c03ea9a27)

- Unity URP로 제작된 2.5D 덱빌딩 로그라이트 모바일 게임입니다.
- 플레이어블 캐릭터를 성장시키고 부적을 해금하는 슬레이더 스파이어 방식의 전투스타일입니다.
- 캐릭터 4명의 고유 부적들과 유물, 필살부를 조합하여 다채로운 방식으로 전투를 진행하는 게임입니다.
- 배틀씬 매커닉을 담당하였으며 전투, 맵, 부적등 전투에 필요한 요소들을 개발했습니다.

## 2. 개발환경
- UNITY 2020.3.25f1 / URP / C#
- Visual Studio 2019
- Windows 10
- 2025.01 ~ 2026.04 (16개월)

## 3. 사용기술
- 디자인 패턴 : Single Tone 패턴으로 매니저 관리
- Object Pooling : 부적, 유물, 아이콘 등 생성되는 객체를 풀링
- Save : 데이터를 json으로 변환화여 저장
- Spine Animation : 스파인 4.1 버전 사용, 모든 캐릭터의 모션을 스파인 적용
- PostProcessing : 모바일 성능에 영향을 주지 않는 선에서 후처리 사용

## 4. 기능구현
- 카드를 드래그 앤 드롭으로 사용
    연소재로 설정된 오브젝트에 불이 붙고 옮겨붙는 매커니즘과 비주얼 이펙트를 사용하였습니다.
- 연소 완료된 오브젝트 파괴 : RayFire for Unity - Obsolete 에셋사용
    연소가 종료된 오브젝트가 조각나 파괴되며 텍스쳐를 변경합니다.
- 인게임 이벤트
    세션별 환경에 맞는 고유 이벤트를 맵별 7종씩 구현하였습니다.
- 번역
    자체 스크립트로 한국어와 영어 세팅에 따라 텍스트가 번역되도록 제작하였습니다.

## 5. 플레이영상
- 공식영상: https://youtube.com/shorts/n3z2TIVdpZ8?si=5MMxm6XP9ThLidSV

## 6. 링크
- [https://store.steampowered.com/app/3920940/_/](https://play.google.com/store/apps/details?id=com.ableane.Detecters&hl=ko)
