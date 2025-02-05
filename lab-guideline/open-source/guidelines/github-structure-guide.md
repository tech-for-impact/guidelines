# 프로젝트 별 Github구성

- 웹 개발
- App 개발
- AI Model 개발
- 모듈 개발

## 1. **Web 개발 프로젝트 오픈소스화**

### GitHub 구조
```
web-project/
├── src/                     # 웹 애플리케이션 소스 코드
│   ├── components/          # React/Vue/Angular 등 UI 컴포넌트
│   ├── services/            # API 호출 및 비즈니스 로직
│   ├── assets/              # 이미지, 스타일 등 정적 자원
│   ├── pages/               # 페이지별 구조
│   └── tests/               # 테스트 코드
├── public/                  # 정적 파일 (index.html, favicon 등)
├── package.json             # 프로젝트 메타데이터 및 의존성 관리
├── README.md                # 프로젝트 설명 및 사용법
├── LICENSE                  # 라이선스 파일
├── CONTRIBUTING.md          # 기여 가이드
├── .gitignore               # Git에 추가되지 않을 파일 목록
└── .github/
    ├── ISSUE_TEMPLATE.md    # 이슈 템플릿
    ├── PULL_REQUEST_TEMPLATE.md # 풀 리퀘스트 템플릿
    └── workflows/           # GitHub Actions 파일 (CI/CD 설정)
```

### 필요한 문서
- [**README.md**](http://readme.md/): 프로젝트 설명, 설치 및 실행 방법, 기술 스택, 기여 방법
- **LICENSE**: 오픈소스 라이선스 (MIT, Apache 등)
- [**CONTRIBUTING.md**](http://contributing.md/): 기여 방법, 코드 스타일, 브랜치 전략, 코드 리뷰 규칙
- **ISSUE_TEMPLATE.md & PULL_REQUEST_TEMPLATE.md**: 이슈와 풀 리퀘스트 생성 시 사용할 템플릿
- **API 문서**: 백엔드와의 통신이 있는 경우 API 문서 제공 (Swagger 또는 Postman 활용)

### 주의 사항
- **보안 관련 코드**: API 키나 데이터베이스 연결 정보가 깃헙에 노출되지 않도록 주의 (예: `.env` 파일을 `.gitignore`에 포함)
- **브라우저 호환성 테스트**: 다양한 브라우저에서 호환되는지 테스트가 완료된 코드를 제공
- **UI/UX**: 오픈소스 참여자들이 쉽게 이해할 수 있도록 UI 구성요소를 문서화 (디자인 시스템 또는 컴포넌트 설명)

## 2. **App 개발 프로젝트 오픈소스화**

### GitHub 구조
```
app-project/
├── android/                 # 안드로이드 소스 코드
├── ios/                     # iOS 소스 코드
├── src/                     # 공통 소스 코드 (React Native, Flutter 등)
├── assets/                  # 이미지, 폰트, 기타 리소스
├── tests/                   # 테스트 코드
├── README.md                # 프로젝트 설명 및 설치 가이드
├── LICENSE                  # 라이선스 파일
├── CONTRIBUTING.md          # 기여 가이드
├── .gitignore               # Git에 추가되지 않을 파일 목록
├── .github/
│   ├── ISSUE_TEMPLATE.md    # 이슈 템플릿
│   └── PULL_REQUEST_TEMPLATE.md # 풀 리퀘스트 템플릿
└── build/                   # 빌드 스크립트 (안드로이드/iOS)
```

### 필요한 문서

- [**README.md**](http://readme.md/): 프로젝트 소개, 설치 및 실행 방법 (각 플랫폼별), 기술 스택, 기여 방법
- **LICENSE**: 오픈소스 라이선스 (MIT, Apache 등)
- [**CONTRIBUTING.md**](http://contributing.md/): 기여 규칙, 코드 스타일 가이드, 기능별 브랜칭 전략
- **테스트 문서**: 테스트 전략과 어떤 툴을 사용하는지 설명 (예: Jest, Detox, XCTest)
- **디자인 문서**: 앱 UI/UX를 문서화하여 새로운 기여자가 쉽게 적응할 수 있도록 제공 (Figma 파일 또는 스크린샷

### 주의 사항

- **플랫폼별 의존성 관리**: Android와 iOS 의존성을 따로 관리해야 하므로, 각각의 빌드 및 설치 방법을 명확히 문서화
- **보안 문제**: 웹 개발과 마찬가지로, API 키나 민감한 정보는 `.gitignore`에 추가하거나 환경 변수로 처리해야 함
- **패키징 및 배포**: 각 플랫폼에서 테스트 후 배포 가능한 패키지 구성 방법을 명확히 설명

## 3. **AI 모델 개발 프로젝트 오픈소스화**

### GitHub 구조
```
ai-project/
├── models/                  # 학습된 모델 파일 (예: .h5, .pt 파일)
├── src/                     # 모델 학습 및 추론을 위한 코드
│   ├── data/                # 데이터 처리 코드
│   ├── train.py             # 모델 학습 코드
│   └── inference.py         # 모델 추론 코드
├── notebooks/               # Jupyter 노트북 파일 (모델 개발 프로세스)
├── requirements.txt         # 파이썬 의존성 관리 파일
├── README.md                # 프로젝트 설명, 사용법
├── LICENSE                  # 라이선스 파일
├── CONTRIBUTING.md          # 기여 가이드
├── .gitignore               # Git에 추가되지 않을 파일 목록
├── .github/
│   ├── ISSUE_TEMPLATE.md    # 이슈 템플릿
│   └── PULL_REQUEST_TEMPLATE.md # 풀 리퀘스트 템플릿
└── tests/                   # 모델 성능 및 유효성 테스트 코드
```

### 필요한 문서

- [**README.md**](http://readme.md/): 프로젝트 개요, 모델 설명, 데이터셋 사용 방법, 설치 및 실행 방법 (추론 및 학습), 기여 가이드
- **LICENSE**: 데이터 및 모델 사용에 대한 라이선스 정보 (오픈소스 모델 및 데이터셋 이용 시 주의)
- [**CONTRIBUTING.md**](http://contributing.md/): 기여 방법, 모델 학습 규칙 및 데이터셋 사용법, 코드 리뷰 및 성능 평가 지침
- **테스트 문서**: 모델 검증 방법, 평가 지표 및 테스트 데이터 설명
- **데이터 문서화**: 사용된 데이터셋 설명 및 데이터 전처리 방법 문서화

### 주의 사항

- **데이터셋 라이선스**: 사용된 데이터셋의 라이선스를 확인하고, 데이터셋 사용 규칙을 명확히 명시해야 함
- **모델 버전 관리**: 학습된 모델 파일의 버전 관리를 명확히 해야 하며, 각 버전별 성능 기록을 남기는 것이 좋음
- **실행 환경 문제**: 다양한 환경에서 모델이 잘 실행되는지 확인하고, 필요한 라이브러리와 실행 환경을 명확히 기재

### **AI 모델 가중치(weight) 공개 방법**

(1) **가중치 파일 외부 저장소 활용**

대형 가중치 파일은 GitHub에 직접 올리기보다는, **외부 스토리지 서비스**(예: Google Drive, AWS S3, Hugging Face Model Hub 등)에 업로드하고, 해당 URL을 README 파일에 포함시키는 방법을 사용합니다.

(2) **README.md에 가중치 다운로드 링크 제공**

README 파일에 가중치 파일을 어떻게 사용할 수 있는지 명확히 안내하는 것이 중요합니다. 예를 들어, 가중치 다운로드 링크와 함께 모델 로드 방법을 설명할 수 있습니다.

### 직접 구축한 데이터셋 오픈소스화

(1) **데이터셋 라이선스 고려**

데이터셋을 오픈소스화할 때는 해당 데이터셋에 대한 **저작권 및 라이선스**를 확인해야 합니다. 데이터가 타인에게서 수집된 경우, 그 데이터의 저작권과 사용 허가를 명확히 해야 합니다. 데이터셋 라이선스 예시로는 다음이 있습니다:

- **Creative Commons (CC BY)**: 데이터셋을 사용할 수 있으나, 출처를 명시해야 함.
- **Open Data Commons Public Domain Dedication and License (PDDL)**: 누구나 자유롭게 데이터셋을 사용할 수 있음.
- **CC0 (Public Domain Dedication)**: 데이터셋이 공공재로 간주되어 자유롭게 사용 가능.

데이터셋 공개 시 반드시 적절한 라이선스를 명시해야 하며, README나 라이선스 파일에 이를 기록합니다.

(2) **데이터셋 저장 및 공유**

데이터셋의 크기에 따라 GitHub에 직접 업로드할 수 없는 경우가 많기 때문에, 일반적으로 **외부 스토리지 서비스**를 사용합니다.

사용할 수 있는 외부 스토리지 예시:

- **Google Drive**: 데이터셋을 쉽게 공유할 수 있으며, 다운로드 링크 제공.
- **Kaggle**: 데이터 과학 커뮤니티에서 많이 사용하는 플랫폼으로, 데이터셋을 공유하고 활용할 수 있음.
- **AWS S3**: 데이터셋을 저장하고 다운로드 링크를 생성할 수 있음.
- **Kakao cloud:** 데이터셋을 저장하고 다운로드 링크를 생성할 수 있음.

(3) **README.md에 데이터셋 사용 정보 추가**

**README 파일에 데이터셋 관련 정보를 추가**하여, 데이터셋이 어디에 저장되어 있는지, 어떻게 사용할 수 있는지 설명해야 합니다.

## 4. **모듈 개발 프로젝트 오픈소스화**

### GitHub 구조
```
module-project/
├── src/                     # 모듈 소스 코드
│   └── main_module.py       # 메인 모듈 파일
├── tests/                   # 테스트 코드
├── docs/                    # 모듈에 대한 문서 (API 문서 포함)
├── setup.py                 # 설치 스크립트 (파이썬 패키지의 경우)
├── requirements.txt         # 파이썬 의존성 관리 파일
├── README.md                # 프로젝트 설명 및 사용법
├── LICENSE                  # 라이선스 파일
├── CONTRIBUTING.md          # 기여 가이드
├── .gitignore               # Git에 추가되지 않을 파일 목록
├── .github/
│   ├── ISSUE_TEMPLATE.md    # 이슈 템플릿
│   └── PULL_REQUEST_TEMPLATE.md # 풀 리퀘스트 템플릿
└── build/                   # 빌드 스크립트 (패키지화 및 배포 관련)
```

### 필요한 문서

- [**README.md**](http://readme.md/): 모듈의 기능, 설치 및 사용법, 코드 예시
- **LICENSE**: 모듈 사용에 대한 라이선스 정보
- [**CONTRIBUTING.md**](http://contributing.md/): 기여 방법, 코드 스타일, 테스트 및 코드 리뷰 절차
- **API 문서**: 모듈의 주요 함수 및 클래스에 대한 설명 (docstring 기반 자동 문서화 도구 사용 가능)
- **테스트 문서**: 모듈의 테스트 방법 및 테스트 커버리지 설명

### 주의 사항

- **의존성 관리**: 의존성을 명확히 정의하여 설치와 테스트가 원활하게 이루어질 수 있도록 함 (예: `requirements.txt` 또는 `package.json`)
- **패키지화 및 배포**: PyPI, npm과 같은 레지스트리에 쉽게 배포할 수 있도록 배포 절차와 설정을 문서화
- **사용성 테스트**: 사용자가 모듈을 쉽게 활용할 수 있도록 여러 환경에서 테스트 및 예제 코드 제공
