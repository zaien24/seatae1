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
      아래는 전체 기능 흐름을 시퀀스 다이어그램으로 표현한 예시입니다:
      <div class="mermaid">
        sequenceDiagram
          participant Client
          participant Server
          participant 커리어넷 API
          participant CSV 파일

          Client->>Server: 서비스 실행 요청
          Server->>커리어넷 API: 학교 정보 API 호출
          커리어넷 API-->>Server: 학교 정보 데이터 수신
          Server->>Server: 학교 정보 데이터 정제

          Server->>CSV 파일: 댓글 데이터 로드
          CSV 파일-->>Server: 댓글 리스트 반환
          Server->>Server: 댓글 데이터 정제

          Server->>Server: 학교 데이터 + 댓글 매칭
          Server->>Server: 통계 집계

          Server->>Client: 결과 파일(result.txt) 생성 완료
      </div>
    </li>
  </ul>
</ul>

<h3>📌 4. 개발</h3>
<ul>
  <li><strong>공통 및 예외 처리 포함</strong></li>
  <ul>
    <li>외부 API 호출 및 JSON 파싱</li>
    <li>CSV 파일 로드 및 각 댓글 리스트화</li>
    <li>외부 학교 데이터 정제 (행정구역명, 학교명)</li>
    <li>댓글 데이터 정제 (이모지 제거, 줄바꿈 정리 등)</li>
    <li>중복된 행정구역 정보 단일화</li>
    <li>댓글 내 중복 학교명 리스트화</li>
    <li>댓글 데이터와 외부 학교 데이터를 비교하여 통계 생성</li>
    <ul>
      <li>학교 구분(초/중/고)</li>
      <li>행정구역 정보 일치 여부</li>
      <li>학교명 유사도 판단</li>
    </ul>
    <li>결과 파일(result.txt) 생성</li>
    <li>로그 파일(result.log) 처리</li>
  </ul>
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












## 📝 [목차](#index) <a name = "index"></a>
- [요구사항](#request)
- [프로세스](#process)
- [개발 환경](#env)
- [기술 스택](#skill)
- [FAQ](#faq)

## 요구사항 <a name = "request"></a>
## 프로세스 <a name = "process"></a>  
## 기능 목록 
## 개발 환경 <a name = "env"></a>
## 기술 스택 <a name = "skill"></a>
<details>
   <summary> 본문 확인 (👈 Click)</summary>
<br />
+ JDK 11 </br>
+ Spring Boot 2.6.7 </br>
+ Spring Data JPA </br>
+ Gradle </br>
+ Handlebars </br>
+ Lombok </br>
+ Github </br>
+ Docker </br>
+ AWS EC2 </br>
+ Redis </br>
+ MariaDB </br>
+ Spock    </br>

</details>

<br>

## 아키텍쳐

## DB 

## 테스트 및 모니터링

## 왜 이 기술을 사용했는가?

## 코드실행방법

## Result   

## 참조 및 출처

## FAQ <a name = "faq"></a>
<details>
   <summary> 본문 확인 (👈 Click)</summary>
<br />
취미 생활 및 자기계발 활동에 금전적으로 투자하는 사람들이 지속적으로 증가하고 있으며, 20 ~ 30대 대상 685명 설문조사 결과 사람들은 취미를 혼자보다 

</details>

<br>

## 제출 방식
- 소스코드
  - 작성한 소스코드를 본인의 Github에 올리고 해당 URL을 문서 파일에 명시하여 채용사이트에 업로드 합니다.
  - 소스를 압축해서 업로드하지 마세요.
  - 과제 소스가 올라가 있는 github의 해당 repository는 public으로 설정해 두셔야 코드레벨 평가가 가능합니다.
  - private로 설정되어 접근이 불가능한 경우 코드레벨 평가를 진행하지 않습니다.

- 기능 점검을 위한 빌드 결과물
  - 빌드 결과물을 Executable jar 형태로 만들어 위 Github에 업로드 하시고 README에 다운로드 링크 정보를 넣어주시기 바랍니다.
  - Github의 용량 문제로 업로드가 안되는 경우 다른 곳(개인 구글 드라이브 등)에 업로드 한 후 해당 다운로드 링크 정보를 README에 넣어주셔도 됩니다.
  - 해당 파일을 다운로드 및 실행(실행 예: java -jar kakaobank.jar)하여 요구 사항 기능 검증을 진행하게 됩니다.
  - 해당 파일을 다운로드할 수 없거나 실행시 에러가 발생하는 경우에는 기능 점검을 진행하지 않습니다.
  - 과제 제출 전 해당 실행파일 다운로드 및 정상 동작 여부를 체크해 주시기 바랍니다.

## 진행 일정
- 코딩테스트 출제일
  - 2025년 4월 6일 (목) 오전 10:00
- 코딩테스트 마감일
  - 2025년 4월 22일 (수) 오후 11:59
 
```
{
  "counselId": 1,
  "appliedAt": "2022-10-18 21:37:00",
  "name": "Member Kim",
  "cellPhone": "010-1111-2222",
  "email": "mail@abc.de",
  "memo": "I hope to get a loan!",
  "zipCode": "123456",
  "address": "Somewhere in Gangnam-gu, Seoul",
  "addressDeatil": "What Apartment No. 101, 1st floor No. 101"
}
```

<!-- Mermaid.js 로딩 스크립트 추가 -->
<script type="module">
  import mermaid from 'https://cdn.jsdelivr.net/npm/mermaid@10/dist/mermaid.esm.min.mjs';
  mermaid.initialize({ startOnLoad: true });
</script>
