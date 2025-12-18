# 🔍 AI 리터러시 테스트

## 📝 프로젝트 소개
- 디지털 취약 계층의 AI 리터러시 능력을 향상시키기 위한 교육형 퀴즈 웹 서비스   
- 실제 이미지 vs AI 이미지 퀴즈를 통해  AI 리터러시 향상을 도모
## 🔗 프로젝트 링크
https://ai-literacy-test.netlify.app/

## 📁 프로젝트 폴더 및 파일 설명
### Frontend
[Frontend Repository](https://github.com/AILiteracyTest/Frontend)
```js
📦src
 ┣ 📂api
 ┃ ┣ 📜imageApi.ts //문제 호출 api
 ┃ ┗ 📜scoreApi.ts //순위 호출 api
 ┣ 📂assets
 ┃ ┣ 📜ai_logo.png
 ┃ ┗ 📜react.svg
 ┣ 📂components
 ┃ ┣ 📜Button.tsx
 ┃ ┣ 📜FontToggle.tsx
 ┃ ┣ 📜GrayCard.tsx
 ┃ ┣ 📜ProgressBar.tsx
 ┃ ┗ 📜WhiteCard.tsx
 ┣ 📂pages
 ┃ ┣ 📜MainPage.tsx //시작 페이지
 ┃ ┣ 📜ResultPage.tsx //결과 페이지
 ┃ ┗ 📜TestPage.tsx //테스트 페이지
 ┣ 📂store
 ┃ ┗ 📜useFontStore.ts //글자 크기 변경 기능을 위한 store
 ┣ 📜App.css
 ┣ 📜App.tsx
 ┣ 📜index.css
 ┗ 📜main.tsx
```


### Backend
[Backend Repository](https://github.com/AILiteracyTest/Backend)
```js
 ┣ 📂db_folder                 // 판별 문제용 이미지 및 설명 데이터
 ┃ ┣ 📂fake                    // AI 생성(Synthetic) 이미지
 ┃ ┣ 📂real                    // 실제(Natural) 이미지
 ┃ ┗ 📂text                    // AI 생성 판단 이유 텍스트
 ┣ 📂unet_autoencoder          // AI 생성 이미지 판별 및 설명 모듈
 ┃ ┣ 📂models                  // 학습된 모델 가중치(.pth)
 ┃ ┃ ┗ model20.pth
 ┃ ┣ ae_core.py                // 재구성 오차 계산 및 heatmap/overlay 시각화
 ┃ ┣ ae_explain.py             // 재구성 오차를 근거로 한 자연어 설명 생성
 ┃ ┣ config.py                 // 경로 및 학습/추론 하이퍼파라미터 설정
 ┃ ┣ datasets_ae.py            // Autoencoder 학습·추론용 데이터셋 정의
 ┃ ┣ laion.py                  // LAION 기반 Autoencoder 학습 데이터셋 생성 스크립트
 ┃ ┣ score_folder.py           // 재구성 오차(mean, p95) 통계 점수 계산 로직
 ┃ ┣ test.py                   // Autoencoder 추론 테스트 스크립트
 ┃ ┣ train.py                  // U-Net Autoencoder 학습 스크립트
 ┃ ┗ unet.py                   // U-Net 기반 Autoencoder 모델 정의
 ┣ app.py                      // 이미지 생성·판별·설명 및 점수 관리 백엔드 서버
 ┣ render.yaml                 // Render 배포 환경 설정 파일
 ┣ requirements.txt            // 백엔드 실행을 위한 Python 의존성 목록
 ┣ runtime.txt                 // Render Python 런타임 버전 명시
 ┗ scores.db                   // 사용자 점수 저장 데이터베이스
```


#### 실행 방법
`npm install` 후 `npm run dev` 혹은 배포 링크를 통해 확인 가능
