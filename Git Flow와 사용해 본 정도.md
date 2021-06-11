[참고 링크](https://uxgjs.tistory.com/183)

# Git Flow

![](https://images.velog.io/images/sinichy7/post/0ccaf6f4-7a5b-4dca-adfb-86ac18d37172/image.png)

- git을 어떻게 운용할지에 대한 방법론. 어떤 공식이나 그런 건 아니고 개발 환경에 따라 수정하고 변형할 수 있다.

### 1. 대표 브랜치
- master : 기준, 제품 배포
- dev : 개발 브랜치, 작업물 머지
- feature : 단위 기능 별 브랜치, 데브에 합침
- release : QA용 -> 통과되면 master
- hotfix : master에서 급히 문제가 발생했을 때 수정하는 브랜치

### 2. FLOW
마스터에서 시작 -> 동일하게 데브 생성 -> 데브에서 피쳐 브랜치로 단위 별 개발 -> 이후 데브에 머지 -> 데브를 릴리즈로 만들고 QA 진행 -> 완료되면 master에 추가하여 배포 -> 이후 문제 발생하면 Hotfix 긴급 수정 후 '태그 생성'하여 수정 배포

### 3. 실제 프로젝트에서 진행한 수준
마스터에서 시작 -> 피쳐 브랜치 생성 -> 개발 후 Pull Request 진행 -> 이후 merge -> 이를 pull 하여 다시 마스터 최신화 시키고 피쳐 다시 기능단위로 파서 진행
