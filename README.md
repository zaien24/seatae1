<h2>🛠 프로젝트 설계 (WBS)</h2>
<details>
<summary>본문 확인 (👈 Click)</summary>

<!-- 1. 요구사항 분석 -->
<h3>1️⃣ 요구사항 분석</h3>
<ul>
  <li>주어진 댓글 리스트(CSV)에서 대한민국의 유효한 학교명을 추출하고, 학교별 등장 횟수를 집계해야 합니다.</li>
  <li>하나의 댓글에는 여러 개의 행정구역명, 학교명, 이모지, 특수문자가 혼합되어 있어 정제가 필요합니다.</li>
</ul>

<!-- 2. 외부 API 선정 및 분석 -->
<h3>2️⃣ 외부 학교 정보 API 선정 및 분석</h3>
<ul>
  <li>선정 API: 
    <a href="https://www.career.go.kr/cnet/front/openapi/openApiMainCenter.do" target="_blank" style="color: #007bff; text-decoration: underline; font-weight: bold;">
      커리어넷 오픈 API 🔗
    </a>
  </li>
  <li>API 인증키 신청 후 테스트 진행</li>
  <li>API 분석 결과:</li>
</ul>

<details>
  <summary>📸 API 분석 1 (Click)</summary>
  <br>
  <img src="https://github.com/user-attachments/assets/36f3e71e-5393-43eb-9af6-ae3703fd1bd7" alt="API 분석 1" width="600">
</details>

<details>
  <summary>📸 API 분석 2 (Click)</summary>
  <br>
  <img src="https://github.com/user-attachments/assets/38188b4a-fbf0-4514-a6d5-7d394d54bcd8" alt="API 분석 2" width="600">
</details>

<details>
  <summary>📸 API 테스트 결과 (Click)</summary>
  <br>
  <img src="https://github.com/user-attachments/assets/ca449012-3446-45ad-9685-c8c5c53efe28" alt="API 테스트" width="600">
</details>

<!-- 3. 정책 및 기능 정의 -->
<h3>3️⃣ 정책 및 기능 정의</h3>
<ul>
  <li><strong>정책</strong>: 중복, 비표준 표현, 이모지 등을 정제하여 정확한 학교명만 추출</li>
  <li><strong>기능</strong>: 외부 API 호출 → 댓글 데이터 정제 → 학교명 매칭 → 통계 생성</li>
</ul>

<!-- 4. 개발 구현 항목 -->
<h3>4️⃣ 개발</h3>
<ul>
  <li>API 연동 및 CSV 파일 로드</li>
  <li>댓글 및 학교 데이터 정제</li>
  <li>중복 행정구역 제거, 중복 학교명 리스트화</li>
  <li>데이터 비교(학교구분/학교명/행정구역)</li>
  <li>결과 파일(result.txt) 및 로그(result.log) 생성</li>
</ul>

<!-- 5. 결과 검증 -->
<h3>5️⃣ 결과 확인</h3>
<ul>
  <li>생성된 결과 파일을 검토하여 요구사항 충족 여부를 확인</li>
</ul>

<!-- 6. 산출물 목록 -->
<h3>6️⃣ 산출물</h3>
<ul>
  <li>📄 README.md</li>
  <li>📁 result.txt / result.log</li>
  <li>🧾 comments.csv</li>
  <li>💻 실행 파일: app.jar</li>
  <li>📦 소스 코드</li>
</ul>

</details>
