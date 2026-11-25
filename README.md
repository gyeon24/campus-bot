# 캠퍼스 AI 도우미 (campus-bot)

학교의 학사, 장학금, 졸업 관련 문서를 근거로 학생의 질문에 답하고, 출처와 마감일을 함께 안내하는 RAG 기반 학사 안내 챗봇입니다.
문서에서 근거를 찾지 못하면 임의로 답하지 않고 담당 부서를 안내합니다.

> 현재 상태: 기본 환경 구축 완료 (테스트 API 배포, 문서 저장소 구성)

## 주요 기능 (계획)

- 근거 기반 질의응답과 출처 표시 (문서명, 게시일, 근거 문장, 원문 링크)
- 학년, 학과, 학번 프로필 맞춤 검색
- 신청 마감일 안내
- 졸업 요건 확인 (영역별 이수 학점 비교)
- 근거 부족 시 답변 대신 담당 부서 안내

## 아키텍처

| 구성 요소 | 사용 서비스 | 현재 상태 |
|---|---|---|
| 웹 프론트엔드 | Amazon S3 + CloudFront | 미구축 |
| 백엔드 API | Amazon API Gateway + AWS Lambda | 테스트 API 배포 완료 |
| 인증 | Amazon Cognito | 예정 |
| 문서 저장소 | Amazon S3 | 구축 완료 |
| 벡터 검색 저장소 | Amazon S3 Vectors (Bedrock Knowledge Bases 연동) | 예정 |
| 임베딩·생성 모델 | Amazon Bedrock (Titan Text Embeddings V2, LLM) | 예정 |