# container-infra-hands-on
Hands on building container based infrastructure using vagrant - kubenetes (+docker) - jenkins - grafana (+prometheus)

# Iaac (Infrastructure as a Service)
- Vagrant
- VirtualBox

# Container Management
- docker
- kubernetes

# CI/CD
- Jenkins

# Monitoring
- prometheus
- grafana


etc
- 인프라를 구축하면서 여러 에러에 부딪혔다.
- VM 실행이 되지 않아 트러블슈팅해보니,
  -  CPU SVM 이 disabled 되어 있는 것을 booting 모드로 들어가 enabled 로 수정
  -  fasoo drm 가 백그라운드에서 이미지 실행할 때에 충돌되서 제거
  -  master node 1, worker node 3개를 띄우니 메모리 점유율이 100%에 근접하며 꼬였는데, antimalware service executable 서비스가 큰 점유율을 차지하고 있었다. window defender 기본 백신에서 제공하는 멜웨어 방지 기능으로 해당 프로세스가 검사하는 파일에 vm 을 제외 리스트로 추가하였다.
