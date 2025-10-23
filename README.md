# 고선 — GitHub Pages 간단 랜딩페이지

이 저장소는 Google Play Console 조직(회사) 검증을 빠르게 통과하기 위한 **간단한 랜딩페이지 템플릿**입니다.
회사명: **고선**  
이메일: **ysj07722@naver.com**  
전화: **0507-1303-9530**

---

## 제공 파일
- `index.html` : 홈페이지 (루트)
- `google1234567890.html` : Google이 HTML 파일 업로드 검증을 요구할 때 사용할 샘플 파일
- `verify_dns.txt` : DNS TXT 예시 값
- `README.md` : 이 파일

---

## 1) 로컬에서 확인
1. 이 폴더를 로컬로 복사합니다.
2. 브라우저에서 `index.html`을 열어 디자인을 확인하세요.

---

## 2) GitHub 저장소 생성 및 업로드 (가장 쉬운 방법)
1. GitHub에서 새 저장소를 만드세요 (예: `goseon-site`).
2. 로컬에서 아래 명령으로 초기화 후 커밋/푸시:
```bash
git init
git add .
git commit -m "Initial commit - 고선 landing page"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```
3. GitHub 저장소로 가서 **Settings > Pages** 로 이동합니다.
   - **Source**를 `main` branch / root로 설정하고 저장합니다.
   - 몇 분 후 `https://<your-username>.github.io/<repo-name>/` 주소로 사이트가 뜹니다.

---

## 3) Google Play Console 도메인/웹사이트 검증 방법 (옵션)
Google Play가 요구하는 검증 방식은 보통 다음 중 하나입니다.

### A) HTML 파일 업로드 방식 (권장, GitHub Pages로 가능)
1. Play Console이 제공하는 특정 파일 이름(예: `googleXXXXXXXX.html`)을 요청할 때, 해당 파일을 리포지토리 루트에 업로드하세요.
   - 이미 제공된 `google1234567890.html` 파일을 이름에 맞게 바꿔 업로드하면 됩니다.
2. GitHub Pages가 활성화된 후 `https://<your-username>.github.io/<repo-name>/googleXXXXXXXX.html` 로 접속하여 파일이 보이면 Play Console에서 검증을 클릭하세요.

### B) DNS TXT 방식
1. 도메인을 가지고 있고 DNS 설정을 편집할 수 있다면, Google이 준 TXT 값을 도메인 DNS에 추가하세요.
2. 예시: `google-site-verification=ABC123...`  
(실제 값은 Play Console에서 받을 값으로 대체하세요.)

---

## 4) 추가 팁
- GitHub Pages에 업로드 후 Google Play 검증이 실패한다면, HTML 파일의 이름과 내용(특히 파일 이름)이 정확한지 확인하세요.
- 회사 이메일(예: admin@yourdomain.com)을 만들 수 있다면 도메인 기반 이메일로도 추가 검증이 가능합니다 (Google Workspace 사용 시 유리).

---

문제가 있으면 제가 `index.html`을 회사 CI/CD나 사용할 도메인 형식에 맞춰 더 수정해드릴게요.  
원하시면 `google1234567890.html` 파일을 Play Console에서 요구한 실제 파일명으로 바로 바꿔드리겠습니다.
