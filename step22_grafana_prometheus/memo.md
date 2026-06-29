# 1. 프로메테우스 커뮤니티 헬름 레포지토리 등록
helm repo add prometheus-community https://prometheus-community.github.io/helm-charts

# 2. 메뉴판 최신화 (아까  명령어!)
helm repo update


# 1. 모니터링 전용 방(Namespace) 생성
kubectl create namespace monitoring

# 2. 커스텀 변수(my-values.yaml)를 적용해서 설치!
helm install my-kube-prometheus prometheus-community/kube-prometheus-stack \
  -n monitoring \
  -f my-values.yaml