# 프로젝트 유형별 GitHub 구성 가이드라인

프로젝트 유형에 따른 오픈소스 GitHub 저장소 구성 및 문서화 가이드라인입니다.

## 목차
- [1. Web 개발 프로젝트](#1-web-개발-프로젝트)
- [2. App 개발 프로젝트](#2-app-개발-프로젝트)
- [3. AI 모델 개발 프로젝트](#3-ai-모델-개발-프로젝트)
- [4. 모듈 개발 프로젝트](#4-모듈-개발-프로젝트)

---

## 1. Web 개발 프로젝트

### 디렉토리 구조
```
web-project/
├── src/                     # 웹 애플리케이션 소스 코드
│   ├── components/          # React/Vue/Angular 등 UI 컴포넌트
│   ├── services/           # API 호출 및 비즈니스 로직
│   ├── assets/             # 이미지, 스타일 등 정적 자원
│   ├── pages/              # 페이지별 구조
│   └── tests/              # 테스트 코드
├── public/                 # 정적 파일 (index.html, favicon 등)
├── package.json            # 프로젝트 메타데이터 및 의존성 관리
├── README.md               # 프로젝트 설명 및 사용법
├── LICENSE                 # 라이선스 파일
├── CONTRIBUTING.md         # 기여 가이드
├── .gitignore              # Git에 추가되지 않을 파일 목록
└── .github/
    ├── ISSUE_TEMPLATE.md   # 이슈 템플릿
    ├── PULL_REQUEST_TEMPLATE.md # PR 템플릿
    └── workflows/          # GitHub Actions 파일 (CI/CD 설정)
```

### 필수 문서
1. **README.md**
   - 프로젝트 설명
   - 설치 및 실행 방법
   - 기술 스택
   - 기여 방법

2. **LICENSE**
   - 오픈소스 라이선스 명시 (MIT, Apache 등)

3. **CONTRIBUTING.md**
   - 기여 방법
   - 코드 스타일
   - 브랜치 전략
   - 코드 리뷰 규칙

4. **템플릿**
   - 이슈 템플릿
   - PR 템플릿

5. **API 문서** (필요시)
   - Swagger 또는 Postman 문서

### 주의사항
- **보안**: API 키, DB 접속 정보 등은 `.gitignore`에 포함
- **브라우저 호환성**: 다양한 브라우저 테스트 완료
- **UI/UX 문서화**: 컴포넌트 설명 및 디자인 시스템 문서화

---

## 2. App 개발 프로젝트

### 디렉토리 구조
```
app-project/
├── android/                # 안드로이드 소스 코드
├── ios/                    # iOS 소스 코드
├── src/                    # 공통 소스 코드 (React Native, Flutter 등)
├── assets/                 # 이미지, 폰트, 기타 리소스
├── tests/                  # 테스트 코드
├── README.md               # 프로젝트 설명 및 설치 가이드
├── LICENSE                 # 라이선스 파일
├── CONTRIBUTING.md         # 기여 가이드
├── .gitignore              # Git에 추가되지 않을 파일 목록
├── .github/
│   ├── ISSUE_TEMPLATE.md   # 이슈 템플릿
│   └── PULL_REQUEST_TEMPLATE.md # PR 템플릿
└── build/                  # 빌드 스크립트 (안드로이드/iOS)
```

### 필수 문서
1. **README.md**
   - 프로젝트 소개
   - 플랫폼별 설치 및 실행 방법
   - 기술 스택
   - 기여 방법

2. **LICENSE**
   - 오픈소스 라이선스

3. **CONTRIBUTING.md**
   - 기여 규칙
   - 코드 스타일 가이드
   - 브랜칭 전략

4. **테스트 문서**
   - 테스트 전략
   - 사용 툴 설명 (Jest, Detox, XCTest)

5. **디자인 문서**
   - UI/UX 가이드라인
   - Figma 파일 또는 스크린샷

### 주의사항
- **플랫폼별 의존성**: Android/iOS 의존성 관리 문서화
- **보안**: API 키 등 민감 정보 관리
- **배포**: 플랫폼별 패키징/배포 방법 설명

---

## 3. AI 모델 개발 프로젝트

### 디렉토리 구조
```
ai-project/
├── models/                 # 학습된 모델 파일
├── src/                    # 모델 학습 및 추론 코드
│   ├── data/               # 데이터 처리 코드
│   ├── train.py           # 모델 학습 코드
│   └── inference.py       # 모델 추론 코드
├── notebooks/              # Jupyter 노트북 파일
├── requirements.txt        # 파이썬 의존성
├── README.md               # 프로젝트 설명
├── LICENSE                 # 라이선스 파일
├── CONTRIBUTING.md         # 기여 가이드
├── .gitignore              # Git 제외 파일
├── .github/
│   ├── ISSUE_TEMPLATE.md   # 이슈 템플릿
│   └── PULL_REQUEST_TEMPLATE.md # PR 템플릿
└── tests/                  # 모델 성능 테스트 코드
```

### 필수 문서
1. **README.md**
   - 프로젝트 개요
   - 모델 설명
   - 데이터셋 사용법
   - 설치 및 실행 방법

2. **LICENSE**
   - 데이터 및 모델 라이선스

3. **CONTRIBUTING.md**
   - 기여 방법
   - 모델 학습 규칙
   - 데이터셋 사용법
   - 성능 평가 지침

4. **테스트 문서**
   - 모델 검증 방법
   - 평가 지표
   - 테스트 데이터 설명

5. **데이터 문서**
   - 데이터셋 설명
   - 전처리 방법

### AI 모델 가중치 공개 방법
GitHub의 파일 크기 제한으로 인해 대형 가중치 파일은 외부 저장소를 활용하여 저장 후, README에 URL을 포함합니다.
README.md에 다음 정보를 반드시 포함해야 합니다:

```
1. 가중치 파일 정보
- 파일명: model_v1.0.weights
- 크기: 500MB
- 체크섬: [MD5 해시값]

2. 다운로드 링크
- [Google Drive](링크)
- [AWS S3](링크)
- [Hugging Face](링크)

3. 가중치 파일 사용 방법
# 예시 코드
import torch
model = YourModel()
model.load_state_dict(torch.load('model_v1.0.weights'))

4. 버전 정보
v1.0: 초기 릴리즈 (2024.01.15)
v1.1: 성능 개선 (2024.02.01)

```
### 데이터셋 공개 가이드라인

직접 구축한 오픈 데이터셋을 공개하려는 경우, [오픈 데이터셋 가이드라인](../../open-dataset/README.md)을 참고해 주세요.

### 주의사항
- **데이터셋 라이선스**: 사용된 데이터셋 라이센스 확인 후 사용 규칙 명시
- **모델 버전 관리**: 버전별 성능 기록
- **실행 환경**: 다양한 환경에서 모델이 실행되는지 확인 및 필요 라이브러리 및 환경 명시

---

## 4. 모듈 개발 프로젝트

### 디렉토리 구조
```
module-project/
├── src/                    # 모듈 소스 코드
│   └── main_module.py      # 메인 모듈 파일
├── tests/                  # 테스트 코드
├── docs/                   # API 문서
├── setup.py                # 설치 스크립트
├── requirements.txt        # 파이썬 의존성
├── README.md               # 프로젝트 설명
├── LICENSE                 # 라이선스 파일
├── CONTRIBUTING.md         # 기여 가이드
├── .gitignore              # Git 제외 파일
├── .github/
│   ├── ISSUE_TEMPLATE.md   # 이슈 템플릿
│   └── PULL_REQUEST_TEMPLATE.md # PR 템플릿
└── build/                  # 빌드 스크립트
```

### 필수 문서
1. **README.md**
   - 모듈 기능
   - 설치 및 사용법
   - 코드 예시

2. **LICENSE**
   - 모듈 라이선스

3. **CONTRIBUTING.md**
   - 기여 방법
   - 코드 스타일
   - 테스트 절차
   - 코드 리뷰 절차

4. **API 문서**
   - 함수 및 클래스 설명
   - docstring 기반 문서

5. **테스트 문서**
   - 테스트 방법
   - 테스트 커버리지

### 주의사항
- **의존성 관리**: 명확한 의존성 정의 (예: `requirements.txt` 또는 `package.json`)
- **배포**: PyPI/npm 배포 절차 문서화
- **사용성**: 사용자가 모듈을 쉽게 활용할 수 있도록 다양한 환경 테스트 및 예제 제공