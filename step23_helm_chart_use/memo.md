### helm chart 저장소에 있는 chart 활용하기

```bash

# 저장소 등록
helm repo add <저장소이름> <저장소위치>
helm repo add my-repo https://hacksungboo.github.io/my-helm-chart/
helm update
helm search repo my-repo

# 바로 install 하지 않고 local 로 다운로드 해서 커스터마이징도 가능하다 (tar 파일 다운로드)
helm pull my-repo/market-app

```