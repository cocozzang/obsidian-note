# 📚 Coco's Learning Vault Collection

개인 학습 및 연구 노트 모음입니다.

## 🗂️ Vault 구조

이 디렉토리는 주제별로 분리된 여러 Obsidian vault를 포함합니다:

### 📁 mathmatic/

- **주제:** 대학 기초 수학
- **내용:** 미적분학, 극한, 연속, 미분 등
- **출처:** Q-Study 대학기초수학 강의 노트
- **상태:** 진행 중 (함수의 극한 파트 완료)

### 💻 dev/

- **주제:** 개발 관련 학습 노트
- **내용:** 프로그래밍, 도구, 기술 스택 등

### 📊 경제/ (예정)

- **주제:** 경제학 학습 노트

### 💰 금융공학/ (예정)

- **주제:** 금융공학 관련 학습

---

## 🎯 프로젝트 관리

### Git 전략

- 각 vault는 독립적인 Git 저장소로 관리 가능
- 주제별 선택적 백업 및 버전 관리
- 민감한 정보는 각 vault별 `.gitignore`로 제외

### 백업 정책

- 정기적인 커밋으로 학습 진행 상황 기록
- 중요한 마일스톤마다 태그 생성
- 원격 저장소를 통한 클라우드 백업

---

## 📝 작업 방식

### 노트 작성 규칙

- Markdown 기반 문서화
- YAML frontmatter로 메타데이터 관리
- 내부 링크를 통한 지식 연결
- 수식은 LaTeX 표기법 사용

### 파일 구조

```
vault/
├── 00-project-plan.md          # 프로젝트 계획서
├── 01-topic-name.md             # 주제별 노트
├── 02-topic-name.md
├── images/                      # 이미지 자료
│   └── topic-name/
└── .obsidian/                   # Obsidian 설정
```

---

## 🔄 업데이트 이력

### 2025-01-18

- **mathmatic vault**: 함수의 극한 파트 완료 (7개 강의)
  - 01-function-limit-1.md ~ 07-function-limit-7.md
  - 중간값 정리, 최대최소 정리까지 완성

---

## 🛠️ 사용 도구

- **Obsidian**: 메인 노트 작성 도구
- **Claude**: AI 어시스턴트를 활용한 학습 정리
- **Git**: 버전 관리
- **Python**: 이미지 처리 및 자동화 스크립트

---

## 📌 참고사항

### 각 Vault 초기화 방법

```bash
# vault별 Git 초기화
cd ~/obsidian/[vault-name]
git init
git add .
git commit -m "Initial commit: [vault-name]"
```

### .gitignore 기본 설정

각 vault에 다음 파일을 생성 권장:

```gitignore
.obsidian/workspace*.json
.obsidian/cache
.DS_Store
*.tmp
```

---

## 📧 Contact

치킨 먹고싶당

---

**Last Updated**: 2025-01-18
