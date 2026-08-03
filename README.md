# Bamboo Board Frontend

대나무숲 콘셉트의 익명 게시판 프론트엔드입니다. 회원 인증, 게시글·댓글·좋아요·신고, 프로필과 비밀번호 변경 기능을 제공합니다.

## 기술 구성

- React 19
- React Router 7
- Vite 8
- Oxlint
- Nginx
- Docker
- GitHub Actions 기반 Blue/Green 배포

## 로컬 실행

```bash
npm ci
npm run dev
```

API 주소는 `VITE_API_BASE_URL`로 지정합니다. 값을 지정하지 않으면 `http://localhost:8080`을 사용합니다.

## 검증

```bash
npm run lint
npm run build
```

## 배포

CI에서 lint와 build를 통과하면 컨테이너 이미지를 생성합니다. 배포가 활성화된 환경에서는 GitHub Actions와 AWS SSM을 통해 Blue/Green 방식으로 배포합니다.
