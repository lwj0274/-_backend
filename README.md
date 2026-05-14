# RealFit Backend

가상 피팅 프로젝트용 백엔드 서버입니다.  
FastAPI + PostgreSQL + Docker + Nginx + dummy AI server 구조로 구성되어 있습니다.

## 현재 구현된 기능

### 1. 기본 Job API
- `POST /api/v1/jobs`
- `GET /api/v1/jobs`
- `GET /api/v1/jobs/{job_id}`
- `GET /api/v1/jobs/{job_id}/result`

### 2. 마네킹 생성 API
- `POST /api/v1/jobs/mannequin`

기능:
- 사용자 이미지 업로드
- AI 서버 전처리 호출
- `mannequin_obj_url`, `mannequin_mesh_url`, `front_image_url` 저장
- DB 저장 및 반환

### 3. 옷 합성 API
- `POST /api/v1/jobs/fitting`

기능:
- 기존 마네킹 데이터 조회
- 의류 이미지 업로드
- AI 서버 합성 호출
- `glb` 결과 URL 저장 및 반환

### 4. 마이페이지용 조회 기능
- 생성된 작업 목록 조회
- 생성된 마네킹 상세 조회
- `thumbnail_url`, `mannequin_url`, `created_at` 반환

---

## 현재 동작 상태

- Docker 실행 가능
- PostgreSQL 연결 완료
- FastAPI docs 확인 가능
- dummy AI server 동작 가능
- 마네킹 생성 API 동작
- 옷 합성 API 동작
- 결과 URL DB 저장 가능
- 더미 결과 파일 URL 접근 가능

---

## 실행 전 준비

- Docker Desktop 실행
- 저장소 루트에서 명령어 실행
- `.env` 파일 필요

---

## 실행 방법

```bash
docker compose down -v
docker compose up --build
