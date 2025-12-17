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
Backend
 ┣ db_folder
 ┃ ┣ fake //AI 이미지 저장 폴더
 ┃ ┣ real //Natural 이미지 저장 폴더
 ┃ ┗ text //AI 이유 텍스트 저장 폴더
 ┣ unet_autoencoder
 ┃ ┣ models
 ┃ ┃ ┗ model20.pth
 ┃ ┣ ae_core.py
 ┃ ┣ ae_explain.py
 ┃ ┣ config.py
 ┃ ┣ datasets_ae.py
 ┃ ┣ laion.py
 ┃ ┣ score_folder.py
 ┃ ┣ test.py
 ┃ ┣ train.py
 ┃ ┗ unet.py
 ┣ app.py //이미지 생성·분석 및 점수 관리 백엔드
 ┣ render.yaml //Render 배포 환경 설정 파일
 ┣ requirements.txt //백엔드 실행을 위한 파이썬 의존성 목록
 ┣ runtime.txt
 ┗ scores.db //사용자 점수 저장 데이터베이스
```


#### 실행 방법
`npm install` 후 `npm run dev` 혹은 배포 링크를 통해 확인 가능
