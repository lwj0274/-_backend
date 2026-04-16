## 현재 상태
Docker 실행 가능
PostgreSQL 연결 완료
백엔드 docs 확인 가능: http://localhost:8000/docs
AI 더미 서버 확인 가능: http://localhost/ai/health
정적 파일 예시: http://localhost/static/result.glb

## 실행 전 준비
- Docker Desktop 실행
- backend 폴더에서 명령어 실행
- `.env` 파일 필요

## 실행
backend 폴더에서 powershell / cmd
docker compose down -v
docker compose up --build

## 프론트 연결용 api
POST /api/v1/jobs
GET /api/v1/jobs/{job_id}
GET /api/v1/jobs/{job_id}/result
