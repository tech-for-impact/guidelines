# Tech for Impact Labs : Open Dataset Guidelines

## Overview
Tech for Impact의 오픈 데이터셋은 사회문제 해결을 위한 기술 개발에 필요한 데이터를 공유하고, 이를 통해 더 큰 임팩트를 만들어내는 것을 목표로 합니다.

자세한 기술 가이드라인은 [데이터셋 기술 가이드라인](./guidelines/opendataset-guide.md)을 참조하세요.

## 데이터셋 공개 원칙
1. **데이터 품질 기준**
   - 단순 원본 데이터가 아닌 가공/정제된 데이터셋
   - 명확한 라이센스 및 사용 조건 명시
   - 상세한 메타데이터 및 문서화 필수

2. **공개 범위 설정**
   - 펠로우 조직과의 협의를 통한 공개 범위 결정
   - 학술/연구 목적 활용을 위한 제한적 공개 가능
   - 데이터 특성에 따른 맞춤형 공개 정책 수립

## 📂 데이터셋 저장 구조
1. **GitHub 저장소 구조**
   - Repository: `techforimpact/opendataset`
   - 각 데이터셋은 개별 폴더로 관리
     ```
     /opendataset
     ├── project1-data/
     │   ├── README.md
     │   └── metadata.json
     ├── project2-data/
     │   ├── README.md
     │   └── metadata.json
     └── ...
     ```

2. **데이터셋 폴더 구성**
   - README.md: 데이터셋 설명 문서
   - metadata.json: 메타데이터 정보
   - 실제 데이터는 외부 저장소 링크로 제공

## 📝 데이터셋 문서화 요구사항
1. **기본 문서화**
- 모든 데이터셋은 제공된 README 템플릿을 기반으로 작성
- 각 섹션별 필수 포함 내용:
 - 개요: 데이터셋 목적, 특징, 펠로우 조직 정보
 - 데이터 명세: 버전, 크기, 레코드 수, 업데이트 일자
 - 다운로드: 접근 방법 및 제한사항
 - 사용 방법: 기본적인 데이터 로드 예시
 - 라이센스: 활용 범위 및 제한사항
 - 인용: 데이터셋 인용 방법
 - 연락처: 담당자 정보

➡️ [README 템플릿](./templates/dataset-readme-template.md) 참고

2. **테크포임팩트 보증**
- README.md에 테크포임팩트 보증 섹션 포함
- 데이터셋 메타데이터에 출처 정보 명시
- 자세한 내용은 [보증 가이드라인](../../Certification/README.md) 참고