# Open Source Guide
테크포임팩트 랩의 오픈소스 제출을 위한 가이드라인입니다. 재사용 가능한 형태의 모듈화된 코드와 관련 문서를 포함합니다.

## 📦 제출 항목
1. **오픈소스 모듈**
   * 랩 당 최소 1개의 오픈소스 모듈 제출 필수 (추가 제출 가능)
   * 재사용 가능한 형태로 모듈화된 코드
   * 테스트 코드 포함

2. **문서화**
   * README.md (프로젝트 소개, 설치 방법, 사용 예시)
   * API 문서 (필요한 경우)
   * 기여 가이드라인
   * 라이센스 - [선택 기준](./guidelines/license-guide.md)

## 📂 Tech For Impact GitHub 레포지토리 생성 프로세스
1. **권한 요청**
- 슬랙 채널 #99-lab-qna에서 아래 정보와 함께 권한 요청:
```
- 프로젝트명:
- GitHub 계정:
- 필요 권한 기간:
- 사용 목적: 오픈소스 레포지토리 생성
```
- 담당자가 Organization member 권한 및 레포지토리 생성 권한 부여 (24시간 이내)

2. **레포지토리 생성**
- Organization 초대 수락 후 레포지토리 생성 가능
- 레포지토리명 형식: `oss-[오픈소스 프로젝트명]`
    - 예: `oss-abc-z`
    - Public으로 설정

3. **접근 권한 관리**
- 레포 생성자 권한
    - Organization 레벨: Repository creation 권한
    - Repository 레벨: Admin 권한 (팀원 초대 및 권한 관리 가능)
   
- 팀원 권한 관리
    - 레포 생성자가 GitHub Repository Settings에서 직접 관리
    - 권한 종류:
        - Write: 코드 Push, Pull Request 생성 가능
        - Read: 코드 확인 및 Pull Request 리뷰만 가능
   
- 메인테이너 권한
    - Admin 권한 부여 (코드 리뷰, 머지, 이슈 관리 등)
        - 메인테이너 권한은 레포 생성자가 직접 부여
        - 프로젝트 완료 후에도 Admin 권한 유지

## 📝 문서화 항목
1. **README.md**
   * 프로젝트 개요
   * 설치 방법
   * 사용 예시
   * 기술 스택
   * 라이센스 정보
   * 기여 방법
- 참고 : [README.md 템플릿](./templates/Readme-template.md)

2. **CONTRIBUTING.md**
   * 개발 환경 설정
   * 코드 스타일 가이드
   * Pull Request 절차
   * 이슈 등록 방법
- 참고 : 기여 가이드라인 템플릿 |[한글](./templates/contribute-guide-KOR.md)/[영어](./templates/contribute-guide-ENG.md)

3. **LICENSE**
   * [오픈소스 라이선스 가이드](./guidelines/license-guide.md) 참고하여 선택

4. **GitHub Templates**
   * Issue Template (Bug Report, Feature Request)
   * Pull Request Template

## 📋 템플릿 가이드라인
* 템플릿은 영어, 한글 모두 작성 권고
* 템플릿 최소 구성 요소 : ([Bug Report](./templates/bug-report-template.md), [Pull Request](./templates/pull-request-template.md), [Feature Request](./templates/feature-template.md))

## 👥 메인테이너 제도
> ⚠️ **알림**: 본 메인테이너 제도의 세부 운영 방안(공식 인증 절차, 커뮤니티 활동 등)은 현재 기획 중이며, 2025년 3월 초 확정하여 공지될 예정입니다.
1. **운영 방식**
   * 1년 단위 운영
   * 랩 당 1-2명의 메인테이너 선발

2. **메인테이너 역할**
   * 코드 리뷰 및 머지
   * 이슈 관리
   * 문서 업데이트
   * 장기적인 프로젝트 유지보수

3. **혜택** (2025년 3월 초 세부사항 확정 예정)
   * Tech for Impact GitHub 프로필 등재
   * 카카오임팩트 공식 컨트리뷰터 인증

- [메인테이너 제도 상세 보기](./guidelines/maintainer.md)

## 📌 참고 문서
* [GitHub 저장소 구조 가이드](./guidelines/github-structure-guide.md)
* [오픈소스 라이선스 가이드](./guidelines/license-guide.md)

## 🔍 문의
문의사항은 슬랙 채널로 연락주세요:
* 채널명: #99-lab-qna
* 담당자: 테일러(카카오임팩트)

## ⚖️ 라이센스
본 가이드라인은 카카오임팩트의 자산으로, 무단 복제 및 배포를 금지합니다. <br><br>
![카카오임팩트 로고](../../acknowledgement/assets/kakao_impact_logo.png)