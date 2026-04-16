## 현재 상태
Docker 실행 가능\n
PostgreSQL 연결 완료\n
백엔드 docs 확인 가능: http://localhost:8000/docs \n
AI 더미 서버 확인 가능: http://localhost/ai/health \n
정적 파일 예시: http://localhost/static/result.glb \n

## 실행 전 준비
- Docker Desktop 실행 \n
- backend 폴더에서 명령어 실행 \n
- `.env` 파일 필요 \n

## 실행
backend 폴더에서 powershell / cmd \n
docker compose down -v \n
docker compose up --build \n

## 프론트 연결용 api
POST /api/v1/jobs \n
GET /api/v1/jobs/{job_id} \n
GET /api/v1/jobs/{job_id}/result \n
