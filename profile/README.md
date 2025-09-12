# AI 산업 RSS 뉴스 큐레이션 서비스 Redfin

급변하는 AI 산업 동향을 최소한의 노력으로 확인할 수 있는 RSS 뉴스 추천 서비스입니다.

```
1. 맞춤형 RSS 뉴스 추천 
2. 챗봇 기반 맞춤형 트렌드 인사이트
3. RAG 기반 단위 기간별 트렌드 인사이트
```

# 시연 영상
[데모 영상](https://www.youtube.com/watch?v=O2XDuq-arEw)

# 프로젝트 구성
- [redfin_ui](https://github.com/team-spark-code/redfin_ui):
    - 설명: 개인 맞춤형 뉴스 피드 및 AI 산업 트렌드 대시보드
    - 스택: Next.js, Typescript, TailwindCSS
- [redfin_core](https://github.com/team-spark-code/redfin_core):
    - 설명: FE/BE 통합 리포. 인증 권한 관리 & 사용자 컨텐츠 관리 기능 포함
    - 스택: Java, Spring Boot, MariaDB
- [redfin_api](https://github.com/team-spark-code/redfin_api):
    - 설명: 처리 완료된 정적 뉴스 데이터 제공하는 RESTful API
    - 스택: Python, FastAPI
- [redfin_scrap_api](https://github.com/team-spark-code/redfin_scrap_api):
    - 설명: RSS 뉴스 소스 수집 및 기사 크롤링 기능 제공하는 RESTful API
    - 스택: Python, FastAPI, reader, feedparser, scrapy
- [redfin_label_api](https://github.com/team-spark-code/redfin_label_api):
    - 설명: 키워드 추출, 태그/카테고리 분류를 제공하는 AI 텍스트 분석 기능 제공하는 RESTful API
    - 스태: Python, FastAPI, Elasticsearch, HuggingFace, SentenceTransformer, Ollama
- [redfin_rag](https://github.com/team-spark-code/redfin_rag):
    - 설명: RSS 뉴스를 RAG 시스템으로 기사 요약, 사용자별 맞춤형 답변하는 기능을 제공하는 RESTful API
    - 스택: Python, FastAPI, LangChain, ChromaDB
- [redfin_infra](https://github.com/team-spark-code/redfin_infra): 
    - 설명: 서비스에 필요한 MariaDB, MongoDB, Elasticsearch, Airflow, Tomcat 등 인프라 명세 및 소스
    - 스택: Bash, Docker Compose, MongoDB, Tomcat
- [redfin_airflow](https://github.com/team-spark-code/redfin_airflow):
    - 설명: ETL 파이프라인 스케줄러로, 주기적으로 RSS 뉴스 기사를 수집 및 전처리하는 기능 제공
    - 스택: Python, Airflow

# 시스템 구성
![](./RedFin.png)



# 팀 소개
- 우성민(프로젝트 총괄)
    - 기획, 산출물 관리
    - 인프라/애플리케이션 설계 및 구현
    - ETL 파이프라인 API 개발
- 서익희(프로젝트 리더)
    - 일정 관리
    - 회원가입, 개인별 콘텐츠 관리 기능 개발
- 강충원 (LLM 개발)
    - RAG 기반 서비스 고도화
    - 프롬프트 엔지니어링 
- 김승환 (추천 시스템 개발)
    - ETL 파이프라인 전처리 로직 구현
    - Elasticsearch 기반 콘텐츠 추천 알고리즘 개발
- 정회성 (FE/BE 개발)
    - 메인 페이지 및 상세 페이지 UI 개발
    - LLM 튜닝 보조

# 참고자료
### [프로젝트 보고서](https://docs.google.com/presentation/d/18YM5UBKSPUVFEgYoLb2qJ9IpfbK4b7eU/edit?usp=sharing&ouid=116180314530610093024&rtpof=true&sd=true)
### [프로젝트 보고서(별첨)](https://docs.google.com/presentation/d/18YhOz2jKubgo4qoq2XnblXzUaMaS4kPa/edit?usp=sharing&ouid=116180314530610093024&rtpof=true&sd=true)
