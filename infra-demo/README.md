# Infra-Demo

Infra-Demo 는 World 서비스, 애플리케이션을 위한 Helm Chart 작성 시 참고를 위한 데모 프로젝트입니다.

## Prerequisites

Kubernetes 1.24+

## Chart 테스팅 및 설치

k8s 클러스터 배포 전 dry-run은 아래 명령어 통해 테스트 :

```bash
$ helm install -f values.yaml \
    --dry-run --debug my-demo-release dev/infra-demo
```

`my-demo-release` 라는 release 이름으로 설치 :

```bash
$ helm install -f values.yaml \
    my-demo-release dev/infra-demo
```

**Tip**: 배포된 파드 확인을 위해 `kubectl get pods`

## Chart 삭제

`my-demo-release` 배포 삭제를 위하여 아래 명령어 실행 :

```bash
$ helm uninstall my-demo-release
```
해당 명령어는 Chart에 연관된 모든 Kubernetes 컴포넌트를 제거하고 helm release를 삭제합니다.

### Image and tag 규칙

### Secret
