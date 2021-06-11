
> 아마존 사의 클라우드 컴퓨팅. 가상머신, 스토리지, 네트워크 인프라 등 다양한 서비스 제공. 클라우드 스토리지 플랫폼(EBS, S3)

### 1. AWS service

1. EC2(Elastic Compute Cloud) : 몇 분동안 구동 가능한 가상 서버 -> api 서버 배포(e.g. django)

2. VPC(Virtual Private Cloud) : AWS 네트워크 망 안의 사용자 전용의 사설 네트워크 -> 거대한 구름 중에 구름 조각을 떼서 주는 격

3. S3(Simple Storage Servive) : 파일 업로드 및 공유

4. RDS(Relational Database Service) : 클라우드에서 데이터베이스 관리

5. ELB(Elastic 'Load Balancing') : 서버로 들어오는 트래픽을 골고루 여러개의 머신으로 전달 -> 서버 부하 방지(한 서버에서 모두 감당하지 않아도 될 것)

### 2. CI / CD? : '자동화'
[참고 링크](https://itholic.github.io/qa-cicd/)

#### CI(Continuous Integration) : 지속적 통합
- 개발을 하면서 코드에 대한 '통합'을 '지속적'으로 진행함으로써 품질 유지

> 빌드 및 테스트 자동화

```
1. 모든 개발자는 퇴근하기 전에 자신의 코드를 중앙 코드와 통합한다.
2. 다음날 출근시 메일로 발송된 결과 리포트를 확인하고 버그가 있으면 수정한다.
```

#### CD(Continuous Deployment, Delivery) : 지속적 배포
> 배포 자동화

- CI의 연장선. 통과한 코드에 대해 테스트 서버와 운영 서버에 곧바로 그 내용을 배포하여 반영하는 것. 이것도 또한 '지속적'으로 이뤄진다.
