# Setup-WordPress

# 목표
* Amazon EC2와 RDS를 활용하여 WordPress 사이트를 설정하고 실행.
* 다중 가용 영역(AZ) 구성을 통해 고가용성과 데이터베이스 장애 조치(failover)를 지원.

# Step

* RDS 설정
  - MySQL 데이터베이스 엔진을 선택하고 프리티어 옵션을 사용.
  - 데이터베이스 초기 설정(식별자, 유저네임, 비밀번호 모두 `wordpress`로 설정).

* EC2 인스턴스 설정
  - Apache2, PHP, 및 PHP MySQL을 설치.
  - WordPress 디렉토리를 `/var/www`로 이동하고 설정.
  - `wp-config.php` 파일을 수정하여 RDS 엔드포인트를 연결.

* 보안 그룹 및 네트워크 설정
  - VPC 및 보안 그룹을 구성.
  - EC2와 RDS 간 통신을 위한 보안 규칙을 설정.

* Auto Scaling 및 Application Load Balancer (ALB)
  - Auto Scaling 그룹을 생성하여 웹 서버의 확장성을 확보.
  - ALB를 설정하여 다중 가용 영역에서 로드 밸런싱 지원.

* WordPress 설치 및 배포
  - WordPress 관리자 계정을 생성하고 설치 완료.
  - Public IP 또는 ALB DNS를 통해 웹사이트에 접근 가능.


※ 21년 기준 자료라 참고만 부탁드립니다
