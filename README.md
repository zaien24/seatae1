<h2 data-start="106" data-end="122" class="">📝 프로젝트 설명</h2>
<details>
<summary> 본문 확인 (👈 Click)</summary>
<h3 data-start="124" data-end="136" class="">1. 개요</h3>
<p data-start="138" data-end="289" class="">주어진 댓글 리스트로부터 유효한 <strong data-start="213" data-end="222">학교 이름</strong>을 추출하고,</br> 이를 학교별로 <strong data-start="238" data-end="248">빈도수 집계</strong>하여 결과 파일로 저장하는 프로그램을 Java로 개발하는 것이 목적입니다. </br> 댓글 리스트는 comments.csv 파일로 제공되었습니다.</p>
<hr data-start="291" data-end="294" class="" style="">
<h3 data-start="296" data-end="310" class="">2. 주요 요구사항</h3>
<ul data-start="312" data-end="644">
<li data-start="312" data-end="352" class="" style="">
<p data-start="314" data-end="352" class="">주어진 댓글 데이터에서 <strong data-start="328" data-end="341">유효한 학교 이름</strong>을 찾아내야 합니다.</p>
</li>
<li data-start="353" data-end="395" class="" style="">
<p data-start="355" data-end="395" class="">학교 이름은 중복될 수 있으며, 이를 <strong data-start="376" data-end="388">학교별로 카운트</strong>해야 합니다.</p>
</li>
<li data-start="444" data-end="482" class="" style="">
<p data-start="446" data-end="482" class="">개발 언어는 <strong data-start="453" data-end="474">Java 8 또는 Java 17</strong>로 제한됩니다.</p>
</li>
<li data-start="483" data-end="529" class="" style="">
<p data-start="485" data-end="529" class="">외부 라이브러리는 <strong data-start="495" data-end="509">오픈소스 혹은 무료</strong>인 경우 제한 없이 사용 가능합니다.</p>
</li>
<li data-start="530" data-end="644" class="" style="">
<p data-start="532" data-end="569" class="">출력 결과 및 로그는 각각 다음과 같은 형식으로 저장되어야 합니다:</p>
<ul data-start="572" data-end="644">
<li data-start="572" data-end="609" class="" style="">
<p data-start="574" data-end="609" class=""><code data-start="574" data-end="586">result.txt</code>: <code data-start="588" data-end="601">학교이름 \t 카운트</code> 형식으로 저장</p>
</li>
<li data-start="612" data-end="644" class="" style="">
<p data-start="614" data-end="644" class=""><code data-start="614" data-end="626">result.log</code>: 처리 과정 및 로깅 내용 저장</p>
</li>
</ul>
</li>
</ul>
<hr data-start="646" data-end="649" class="" style="">
<h3 data-start="651" data-end="669" class="">3. 결과 파일 형식 예시</h3>
<pre class="overflow-visible!" data-start="671" data-end="709"><div class="contain-inline-size rounded-md border-[0.5px] border-token-border-medium relative bg-token-sidebar-surface-primary"><div class="flex items-center text-token-text-secondary px-4 py-2 text-xs font-sans justify-between h-9 bg-token-sidebar-surface-primary dark:bg-token-main-surface-secondary select-none rounded-t-[5px]"></div><div class="sticky top-9"><div class="absolute right-0 bottom-0 flex h-9 items-center pe-2"><div class="bg-token-sidebar-surface-primary text-token-text-secondary dark:bg-token-main-surface-secondary flex items-center rounded-sm px-2 font-sans text-xs"><span class="" data-state="closed"></span><span class="" data-state="closed"></span></div></div></div><div class="overflow-y-auto p-4" dir="ltr"><code class="whitespace-pre!"><span><span>ㅇㅇ중학교	192
ㅇㅇㅇ고등학교	254
서울대학교	13
</span></span></code></div></div></pre>
<blockquote data-start="711" data-end="759">
<p data-start="713" data-end="759" class="">※ <code data-start="715" data-end="722">학교 이름</code>과 <code data-start="724" data-end="728">숫자</code> 사이에는 <strong data-start="734" data-end="742">탭 문자</strong>(<code data-start="743" data-end="747">\t</code>)가 들어가야 합니다.</p>
</blockquote>
<hr data-start="761" data-end="764" class="" style="">
<h3 data-start="766" data-end="778" class="">4. 제출 항목</h3>
<ul data-start="780" data-end="844">
<li data-start="780" data-end="795" class="" style="">
<p data-start="782" data-end="795" class="">J소스 코드</p>
</li>
<li data-start="796" data-end="821" class="" style="">
<p data-start="798" data-end="821" class="">실행 결과 파일 (<code data-start="808" data-end="820">result.txt</code>)</p>
</li>
<li data-start="822" data-end="844" class="" style="">
<p data-start="824" data-end="844" class="">로그 파일 (<code data-start="831" data-end="843">result.log</code>)</p>
</li>
</ul>
</details>

<h2>📌 요구사항 분석</h2>
<details>
<summary>본문 확인 (👈 Click)</summary>

<ul>
  <li>
    <p>주어진 댓글 리스트(CSV 파일)에서 대한민국 내 유효한 <strong>학교 이름</strong>을 추출하고, 이를 <strong>학교별로 등장 횟수</strong>를 집계하는 프로그램을 작성해야 합니다.</p>
  </li>
  <li>
    <p>댓글은 <strong>큰따옴표(")</strong>로 구분되며, 하나의 댓글에는 복수 개의 <strong>행정구역명, 학교명, 이모지, 특수문자</strong> 등이 혼재되어 있습니다.</p>
  </li>
  <li>
    <p>대상 학교는 대한민국의 <strong>초등학교, 중학교, 고등학교, 대학교</strong>로 한정하며, 유사 표현이나 비표준 명칭은 제외되어야 합니다.</p>
  </li>
  <li>
    <p>하나의 댓글에 <strong>여러 개의 학교명</strong>이 존재할 수 있으므로, 모든 유효한 학교명을 <strong>정확히 식별하고 집계</strong>해야 합니다.</p>
  </li>
  <li>
    <p>결과는 다음의 두 파일로 출력되어야 합니다:</p>
    <ul>
      <li><code>result.txt</code>: <strong>학교명 + 탭(\t) + 카운트</strong> 형식으로 저장<br>예) <code>서울중학교\t12</code></li>
      <li><code>result.log</code>: 처리 중 발생한 <strong>로그 및 예외 정보</strong>를 저장</li>
    </ul>
  </li>
  <li>
    <p>정확한 학교명 추출을 위해 <strong>텍스트 정제</strong> 및 <strong>패턴 인식</strong> 처리가 필요합니다.<br>예: 이모지 제거, 괄호 제거, 개행 문자 정리 등</p>
  </li>
  <li>
    <details>
      <summary>📸 댓글 분석 이미지 (Click)</summary>
      <br>
      <img src="https://github.com/user-attachments/assets/344ae0a2-bb6f-4b34-a0d0-f5838976c56f" alt="댓글분석" width="600">
      </details>
  </li>
</ul>

</details>





<h2>🛠 프로젝트 설계 (WBS)</h2>
<details>
<summary>본문 확인 (👈 Click)</summary>

<h3>1. 요구사항 분석</h3>
<h3>2. 전체 학교 정보를 가져올 API 선정</h3>
<ul>
  <li>
    학교 정보를 제공하는 API를 탐색하고 선정합니다.<br>
    (선정된 API: <a href="https://www.career.go.kr/cnet/front/openapi/openApiMainCenter.do" target="_blank">커리어넷 오픈 API</a>)
  </li>
  <li>API 사용을 위한 인증키를 신청합니다.</li>
  <li>선정된 API의 응답 형식과 활용 가능성을 테스트합니다.</li>
  <li>
      <ul>
        <li>
        <details>
      <summary>📸 API분석1(Click)</summary>
      <br>
      <img src="https://github.com/user-attachments/assets/36f3e71e-5393-43eb-9af6-ae3703fd1bd7" alt="API분석1" width="600">
      </details>
      </li>
      <li>
        <details>
      <summary>📸 API분석2 (Click)</summary>
      <br>
      <img src="https://github.com/user-attachments/assets/38188b4a-fbf0-4514-a6d5-7d394d54bcd8" alt="API분석1" width="600">
      </details>
      </li>
      <li>
        <details>
      <summary>📸 API테스트 (Click)</summary>
      <br>
      <img src="https://github.com/user-attachments/assets/ca449012-3446-45ad-9685-c8c5c53efe28" alt="API테스트" width="600">
      </details>
      </li>
      </ul>
  </li>
</ul>

<h3>3. 기능 및 정책 정의 (Flow Chart 포함 예정)</h3>
<ul>
  <li><strong>정책</strong></li>
  <ul>
    <li>중복된 행정구역명, 학교명은 정제 처리</li>
    <li>비표준 표현은 필터링하여 유효한 학교명만 추출</li>
  </ul>
  <li><strong>기능</strong></li>
  <ul>
    <li>공공데이터 기반의 학교 정보를 제공하는 API 호출</li>
    <li>CSV 파일 로드 및 댓글 리스트화</li>
    <li>공공데이터 기반의 학교 정보를 제공하는 API 호출 데이터 정제</li>
    <li>댓글 데이터 정제</li>
    <li>정제된 댓글과 학교 정보를 매칭하여 통계 생성</li>
    <li>결과 파일(result.txt) 생성</li>
    <li>
        <details>
      <summary>📸 시퀀스다이어그램 (Click)</summary>
      <br>
      <img src="https://github.com/user-attachments/assets/5e0a9f66-d5ea-4161-acfe-68cac421945d" alt="시퀀스다이어그램" width="600">
      </details>
  </ul>
</ul>
<ul>
</ul>

<h3>4. 개발</h3>
<ul>
  <li>공공데이터 기반의 <strong>학교 정보를 제공하는 API 호출</strong></li>
  <li><strong>CSV 파일 로드</strong> 및 댓글 리스트화</li>
  <li>
    <strong>공공데이터 기반의 학교 정보를 제공하는 API 호출 데이터 정제</strong>
    <ul>
      <li>행정구역명 정리</li>
      <li>학교명 형식 통일</li>
    </ul>
  </li>
  <li>
    <strong>댓글 데이터 정제</strong>
    <ul>
      <li>중복된 행정구역 정보 → <strong>단일 저장 처리</strong></li>
      <li>댓글 내 중복된 학교명 → <strong>리스트화</strong> 처리</li>
    </ul>
  </li>
  <li>
    <strong>댓글 데이터와 학교 데이터를 비교하여 통계 생성</strong>
    <ul>
      <li><strong>학교 구분</strong>: 초/중/고/대</li>
      <li><strong>행정구역 정보</strong> 일치 여부</li>
      <li><strong>학교명 유사도</strong> 판단</li>
    </ul>
  </li>
  <li><strong>결과 파일(result.txt) 생성</strong></li>
  <li><strong>로그 파일(result.log) 처리</strong></li>
</ul>



<h3>📌 5. 결과 확인</h3>
<ul>
  <li>출력된 결과 파일과 로그 파일을 통해 정상 수행 여부 확인</li>
</ul>

<h3>📌 6. 산출물 목록</h3>
<ul>
  <li>README (설치 및 실행 방법 포함)</li>
  <li>결과 파일: <code>result.txt</code></li>
  <li>로그 파일: <code>result.log</code></li>
  <li>소스 코드</li>
  <li>실행 파일: <code>app.jar</code></li>
  <li>입력 파일: <code>comments.csv</code></li>
</ul>
</details>


<h2>🧩 서비스 아키텍처 </h2>
<details>
  <summary>본문 확인 (👈 Click)</summary>
      <br>
      <img src="https://github.com/user-attachments/assets/ae426f4b-81d6-41f5-9f87-3b9c35ecb13c" alt="시퀀스다이어그램" width="600">
</details>

<h2>💻 개발 환경 및 기술 스택</h2>
<details>
<summary>본문 확인 (👈 Click)</summary>

<h3>1. 개발 환경</h3>
<ul>
  <li><strong>IDE:</strong> IntelliJ IDEA</li>
  <li><strong>Java 버전:</strong> Java 17</li>
  <li><strong>빌드 도구:</strong> Gradle 8.1.3</li>
  <li><strong>프레임워크:</strong> Spring Boot 3.4.4</li>
  <li><strong>기타 도구:</strong> Lombok</li>
</ul>

<h3>2.오픈 소스 및 라이브러리</h3>
<ul>
  <li><strong>OpenCSV 5.7.1:</strong> CSV 파일 파싱 및 매핑 처리</li>
  <li>
    <strong>LevenshteinDistance:</strong> 문자열 유사도 계산 알고리즘<br>
    (라이브러리: <code>commons-text-1.10.0.jar</code>)
  </li>
  <li>
    <strong>커리어넷 오픈 API:</strong> 
    <a href="https://www.career.go.kr/cnet/front/openapi/openApiMainCenter.do" target="_blank">학교 정보 수집용 외부 공공 데이터 API</a>
  </li>
</ul>
</details>

<h2>📄 기능 구현 프로세스</h2>
<details>
  <summary>본문 확인 (👈 Click)</summary>
  <ul>
    <li>공공데이터 기반의 학교 정보를 제공하는 API 호출 및 결과 데이터 정제
      <br>
      <img src="https://github.com/user-attachments/assets/e09ea107-8940-4c5b-8599-018030d33b55" alt="시퀀스다이어그램" width="600">
    </li>
    <li>CSV 파일 로드 후 댓글 리스트화 및 댓글데이터 정제
      <br>
      <img src="https://github.com/user-attachments/assets/6afc01b1-168e-41a5-ab7e-f0d48d5b51fe" alt="시퀀스다이어그램" width="600">
    </li>
    <li>댓글 정제 데이터와 학교 정제 데이터를 비교하여 통계 생성
      <br>
      <img src="https://github.com/user-attachments/assets/5514f4d3-6878-44fc-aa93-ebcf7d1f2725" alt="시퀀스다이어그램" width="600">
    </li>
  </ul>
 <img src="[ttps://github.com/user-attachments/assets/f0b39bca-2698-44c1-b485-8b96f10460f7" alt="시퀀스다이어그램" width="600">
  
</details>


<h2>📄 결과 확인 방법</h2>
<details>
  <summary>본문 확인 (👈 Click)</summary>
  <ul>
    <li>
      <p><strong>결과 호출 URL:</strong><br>
      <code>http://localhost:8080/api/school/downloadResult</code></p>
    </li>
    <li>
      <p><strong>comments.csv 파일 업로드 방법:</strong></p>
      <ul>
        <li><code>java -jar app.jar</code> 실행한 위치 기준으로
        <li><code>/upload/csv/comments.csv</code> 경로에 파일 배치</li>
      </ul>
    </li>
  </ul>

</details>


<h2>🧠 보완 및 확장 가능성</h2>
<details>
<summary>본문 확인 (👈 Click)</summary>

<h3>1. 학교 데이터의 DB화</h3>
<ul>
  <li>커리어넷 API에서 수집한 학교 정보를 RDB 또는 NoSQL에 저장하면 재사용성과 조회 효율이 높아집니다.</li>
  <li>정제 및 필터링된 데이터를 기반으로 한 통계 생성 및 UI 연계도 유리합니다.</li>
</ul>

<h3>2. 디자인 패턴 적용</h3>

<h3>3. 유사도 알고리즘 개선</h3>
<ul>
  <li>LevenshteinDistance 외에도 Jaro-Winkler, Cosine Similarity 등 다양한 알고리즘을 테스트하여 성능을 최적화할 수 있습니다.</li>
</ul>

<h3>4. 비동기 처리 및 성능 최적화</h3>
<ul>
  <li>Java 병렬 스트림, CompletableFuture, ExecutorService 또는 Spring Batch를 사용하여 대용량 데이터 처리 속도를 개선할 수 있습니다.</li>
</ul>

<h3>5. CSV 업로드 UI 연동</h3>
<ul>
  <li>CSV 파일을 업로드할 수 있는 웹 UI를 제공하면 사용 편의성이 향상됩니다.</li>
</ul>

<h3>6. 분석 결과 시각화</h3>
<ul>
  <li>학교별 분포, 지역별 통계, 상위 랭킹 등 다양한 시각화를 통해 데이터 활용도를 높일 수 있습니다.</li>
  <li>Chart.js, Apache ECharts 등의 오픈소스 라이브러리를 활용할 수 있습니다.</li>
</ul>

</details>


<h2>🧾 프로젝트 마무리 및 회고</h2>
<details>
<summary>본문 확인 (👈 Click)</summary>

<p>
이번 과제를 통해 주어진 비정형 댓글 데이터에서 유효한 학교 정보를 식별하고 통계 처리하는 백엔드 기능을 설계하고 구현하였습니다.<br>
텍스트 정제, 정규화, 유사도 기반 매칭, 외부 API 연계 등 실무에서도 중요한 요소들을 고려하여 처리한 점이 의미 있었습니다.
</p>

<p>
카카오뱅크 기반기술 백엔드 직무는 시스템 안정성과 확장성, 다양한 외부 시스템과의 통합 경험이 중요한 역량이라고 생각합니다.<br>
과제 개발 과정에서 이러한 관점을 반영하려 노력했고, 특히 데이터 흐름 중심의 설계와 기능 분리에 신경을 썼습니다.
</p>

<p>
향후에는 비동기 처리 성능 개선, 로직 모듈화, 시각화 도입 등을 통해 완성도를 더욱 높일 수 있을 것으로 기대합니다.<br>
이 과제를 기반으로 더 깊이 있는 시스템 설계와 성능 최적화를 고민하는 백엔드 엔지니어로 성장하고 싶습니다.
</p>

</details>

