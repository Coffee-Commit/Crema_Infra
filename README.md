# [CREMA] Infrastructure

이 문서는 [CREMA]의 인프라 구성과 운영 방법을 안내합니다.

## 📜 개요 (Overview)

본 인프라는 [CREMA]을 [GCP] 환경에 배포하고 안정적으로 운영하는 것을 목표로 합니다.

- **Cloud Provider**: `GCP`
- **Orchestration**: `Kubernetes`
- **CI/CD**: `Jenkins` / `ArgoCD`

### 아키텍처 다이어그램
![Architecture Diagram](https://via.placeholder.com/800x400.png?text=Architecture+Diagram+Here)

---

## 🚀 시작하기 (Getting Started)

로컬 환경에서 인프라를 관리하기 위해 필요한 도구와 설정입니다.

### 필수 도구 (Prerequisites)
- **kubectl**: `v1.28.x`
- **kustomize**: `v5.x.x`
- **aws-cli**: `2.x` (또는 사용하는 클라우드 CLI)

### 클러스터 접근 설정 (Cluster Access)
아래 명령어를 실행하여 로컬 `kubeconfig`에 클러스터 정보를 추가합니다.
```bash
# 예시 (AWS EKS)
aws eks update-kubeconfig --region [리전] --name [클러스터 이름]