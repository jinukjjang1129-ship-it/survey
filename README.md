# 설문 응답 기반 성향 프로필 시각화

1~7점 설문 응답을 축별 점수와 유형 설명으로 변환해 보여주는 Streamlit 프로토타입입니다. 관계 상담 챗봇에서 사용하는 설문·프로필 UI를 별도로 살펴볼 수 있습니다.

## 구현 내용

- 문항별 응답 수집, 역채점과 점수 집계
- 자기/타인 모형, 감정 표현, 자기효능감 기준의 유형 설명
- 사분면·점수 막대 등 Matplotlib 시각화
- 설문과 결과 화면 전환, 세션 상태 관리

점수와 유형은 코드에 정의된 규칙입니다. 심리 척도의 타당도·임상 진단 정확도를 검증한 프로젝트로 소개하지 않습니다. 코드에 중복 정의된 함수와 프로토타입 기준값이 있어 유지보수 개선이 필요합니다.

## 파일과 실행

```text
설문조사및프로필.py          Streamlit 설문·점수·결과 화면
Freesentation-6SemiBold.ttf 표시용 폰트
requirements.txt           의존성
```

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
streamlit run '설문조사및프로필.py'
```

외부 LLM API를 사용하는 앱은 아닙니다. 이번 정리는 실제 코드를 확인한 소개·실행 안내 개선이며 전체 브라우저 흐름을 새로 시험하지 않았습니다. 폰트 이용 조건과 설문 문항 출처를 보강할 필요가 있습니다.

[연결된 챗봇 프로젝트](https://github.com/jinukjjang1129-ship-it/attachment-profile-chatbot)에서는 Chroma 검색과 대화 기능을 다룹니다. 두 프로젝트의 점수 기준이 동일하다고 가정하지 않습니다.
