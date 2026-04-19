# RU Reply

러시아어 물류 비즈니스 커뮤니케이션 AI 앱

## 배포 방법 (Vercel)

### 1. GitHub에 올리기
```bash
git init
git add .
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/ru-reply.git
git push -u origin main
```

### 2. Vercel 연결
1. https://vercel.com 접속 → GitHub 로그인
2. "Add New Project" → 방금 만든 저장소 선택
3. **Environment Variables** 에서 아래 추가:
   - Key: `ANTHROPIC_API_KEY`
   - Value: `sk-ant-...` (본인 Anthropic API 키)
4. Deploy 클릭

### 3. 완료
- 배포된 URL로 어느 기기에서든 API 키 입력 없이 바로 사용 가능

## 구조
```
ru-reply/
├── api/
│   └── translate.js   ← 서버리스 함수 (API 키 여기 보관)
├── public/
│   └── index.html     ← 프론트엔드
└── vercel.json        ← Vercel 설정
```
