# Tech for Impact Labs : Service Code Guide

테크포임팩트 랩의 서비스 코드 제출을 위한 가이드라인입니다. <br>
실제 서비스 운영에 필요한 전체 코드와 기술 문서를 포함합니다.

## 📦 제출 항목

1. **서비스 코드**
 - 실제 서비스 운영에 필요한 전체 소스 코드
 - 테스트 코드 포함

2. **기술 문서 및 사용자 매뉴얼**
 - [프로젝트 유형별 문서](./guidelines/project-type-guide.md)
 - 환경 설정 및 배포 문서
 - 사용자 매뉴얼 | (참고)[템플릿](./templates/user-manual.md)
 - 운영 인수인계 문서 | (참고)[템플릿](./templates/handover-doc.md)

3. **테크포임팩트 보증**
 - 웹사이트, 모바일 앱, 오픈소스 등 결과물 유형에 따라 테크포임팩트 보증을 적용해야 합니다
 - 자세한 내용은 [보증 가이드라인](../../attribution/service-certification.md) 참고

## 📂 저장소 옵션

프로젝트 특성에 따라 아래 저장소 중 하나를 선택하여 제출합니다:

1. **Tech For Impact GitHub (Private)**
 - 카카오임팩트가 직접 운영/관리하는 서비스
 - 민감한 정보가 포함된 프로젝트
 
 ### Tech For Impact GitHub 저장소 생성 프로세스
 1. **권한 요청**
  - 슬랙 채널 #99-lab-qna에서 아래 정보와 함께 권한 요청:
  ```
  - 프로젝트명:
  - GitHub 계정:
  - 필요 권한 기간:
  - 사용 목적: 서비스 코드 레포지토리 생성
  ```
  - 담당자가 Organization member 권한 및 레포지토리 생성 권한 부여 (24시간 이내)
 
 2. **레포지토리 생성**
  - Organization 초대 수락 후 레포지토리 생성 가능
  - 레포지토리명 형식: `services-[프로젝트명]`
    - 예: `services-a-eye`, `services-dva`
  Private로 설정 권장
 
 3. **접근 권한 관리**
  - 레포 생성자 권한
    - Organization 레벨: Repository creation 권한
    - Repository 레벨: Admin 권한 (팀원 초대 및 권한 관리 가능)
    
 - 팀원 권한 관리
  - 레포 생성자가 GitHub Repository Settings에서 직접 관리
    - 권한 종류:
      - Write: 코드 Push, Pull Request 생성 가능
      - Read: 코드 확인 및 Pull Request 리뷰만 가능
    - 이관 완료 후 전체 팀원 Read-only로 변경됨

2. **펠로우 조직 GitHub or Local 환경**
 - 펠로우 조직이 직접 운영/관리하는 서비스
 - 기존 시스템과 통합되는 프로젝트

## 📝 문서 작성 가이드
- [프로젝트 유형별 문서 가이드라인](./guidelines/project-type-guide.md)
- [Web](./guidelines/web-development-guide.md)
- [App](./guidelines/app-development-guide.md)
- [MLOps](./guidelines/ml-ops-guide.md)
- [AI Model](./guidelines/ai-model-guide.md)
- [Model](./guidelines/model-guide.md)

## 📌 참고 사항

- 모든 문서는 마크다운(.md) 형식으로 작성
- 이미지 등 미디어 파일은 `/assets` 폴더에 저장
- 환경 변수 등 민감 정보는 별도 관리 (.env.example 파일 제공)
- 코드 및 문서는 한글 작성 권장 (영문 혼용 가능)

## ❓ 자주 묻는 질문
자주 묻는 질문 사항은 [서비스 코드 FAQ](./FAQ.md)를 참고해 주세요. 코드 범위, 저장소 관리, 문서화 요구사항, 기술 구현, 인수인계 절차 등에 대한 상세한 답변을 확인하실 수 있습니다.