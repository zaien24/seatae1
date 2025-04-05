# 프로젝트 설명
## 개요
 주어진 댓글 리스트로부터 유효한 학교 이름을 추출하고,\n
 이를 학교별로 빈도수 집계하여 결과 파일로 저장하는 프로그램을 Java로 개발하는 것이 목적입니다.\n
 댓글 리스트 : comments.csv 파일 제공
## 주요 요구사항
 

<div class="markdown prose dark:prose-invert w-full break-words light"><p data-start="0" data-end="99" class="">좋습니다! 주어진 과제 내용을 바탕으로, <strong data-start="23" data-end="39">“과제 프로젝트 설명”</strong> 항목을 깔끔하게 작성해드릴게요. 아래는 예시이며, 문서나 README에 바로 넣을 수 있도록 정리했습니다:</p>
<hr data-start="101" data-end="104" class="" style="">
<h2 data-start="106" data-end="122" class="">📝 과제 프로젝트 설명</h2>
<h3 data-start="124" data-end="136" class="">1. 과제 개요</h3>
<p data-start="138" data-end="289" class="">본 프로젝트는 <strong data-start="146" data-end="177">카카오뱅크 기반기술 플랫폼 서비스 개발자 과제전형</strong>의 일환으로 수행된 과제입니다. 주어진 댓글 리스트로부터 유효한 <strong data-start="213" data-end="222">학교 이름</strong>을 추출하고, 이를 학교별로 <strong data-start="238" data-end="248">빈도수 집계</strong>하여 결과 파일로 저장하는 프로그램을 Java로 개발하는 것이 목적입니다.</p>
<hr data-start="291" data-end="294" class="" style="">
<h3 data-start="296" data-end="310" class="">2. 주요 요구사항</h3>
<ul data-start="312" data-end="644">
<li data-start="312" data-end="352" class="" style="">
<p data-start="314" data-end="352" class="">주어진 텍스트 데이터에서 <strong data-start="328" data-end="341">유효한 학교 이름</strong>을 찾아내야 합니다.</p>
</li>
<li data-start="353" data-end="395" class="" style="">
<p data-start="355" data-end="395" class="">학교 이름은 중복될 수 있으며, 이를 <strong data-start="376" data-end="388">학교별로 카운트</strong>해야 합니다.</p>
</li>
<li data-start="396" data-end="443" class="" style="">
<p data-start="398" data-end="443" class="">유효한 학교 이름의 정의는 과제 첨부 예시 및 전처리 조건을 참고하여 구현합니다.</p>
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
<pre class="overflow-visible!" data-start="671" data-end="709"><div class="contain-inline-size rounded-md border-[0.5px] border-token-border-medium relative bg-token-sidebar-surface-primary"><div class="flex items-center text-token-text-secondary px-4 py-2 text-xs font-sans justify-between h-9 bg-token-sidebar-surface-primary dark:bg-token-main-surface-secondary select-none rounded-t-[5px]"></div><div class="sticky top-9"><div class="absolute right-0 bottom-0 flex h-9 items-center pe-2"><div class="bg-token-sidebar-surface-primary text-token-text-secondary dark:bg-token-main-surface-secondary flex items-center rounded-sm px-2 font-sans text-xs"><span class="" data-state="closed"><button class="flex gap-1 items-center select-none px-4 py-1" aria-label="복사"><svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="icon-xs"><path fill-rule="evenodd" clip-rule="evenodd" d="M7 5C7 3.34315 8.34315 2 10 2H19C20.6569 2 22 3.34315 22 5V14C22 15.6569 20.6569 17 19 17H17V19C17 20.6569 15.6569 22 14 22H5C3.34315 22 2 20.6569 2 19V10C2 8.34315 3.34315 7 5 7H7V5ZM9 7H14C15.6569 7 17 8.34315 17 10V15H19C19.5523 15 20 14.5523 20 14V5C20 4.44772 19.5523 4 19 4H10C9.44772 4 9 4.44772 9 5V7ZM5 9C4.44772 9 4 9.44772 4 10V19C4 19.5523 4.44772 20 5 20H14C14.5523 20 15 19.5523 15 19V10C15 9.44772 14.5523 9 14 9H5Z" fill="currentColor"></path></svg>복사</button></span><span class="" data-state="closed"><button class="flex items-center gap-1 px-4 py-1 select-none"><svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="icon-xs"><path d="M2.5 5.5C4.3 5.2 5.2 4 5.5 2.5C5.8 4 6.7 5.2 8.5 5.5C6.7 5.8 5.8 7 5.5 8.5C5.2 7 4.3 5.8 2.5 5.5Z" fill="currentColor" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round"></path><path d="M5.66282 16.5231L5.18413 19.3952C5.12203 19.7678 5.09098 19.9541 5.14876 20.0888C5.19933 20.2067 5.29328 20.3007 5.41118 20.3512C5.54589 20.409 5.73218 20.378 6.10476 20.3159L8.97693 19.8372C9.72813 19.712 10.1037 19.6494 10.4542 19.521C10.7652 19.407 11.0608 19.2549 11.3343 19.068C11.6425 18.8575 11.9118 18.5882 12.4503 18.0497L20 10.5C21.3807 9.11929 21.3807 6.88071 20 5.5C18.6193 4.11929 16.3807 4.11929 15 5.5L7.45026 13.0497C6.91175 13.5882 6.6425 13.8575 6.43197 14.1657C6.24513 14.4392 6.09299 14.7348 5.97903 15.0458C5.85062 15.3963 5.78802 15.7719 5.66282 16.5231Z" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"></path><path d="M14.5 7L18.5 11" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"></path></svg>편집</button></span></div></div></div><div class="overflow-y-auto p-4" dir="ltr"><code class="whitespace-pre!"><span><span>ㅇㅇ중학교	192
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
<p data-start="782" data-end="795" class="">Java 소스 코드 전반</p>
</li>
<li data-start="796" data-end="821" class="" style="">
<p data-start="798" data-end="821" class="">실행 결과 파일 (<code data-start="808" data-end="820">result.txt</code>)</p>
</li>
<li data-start="822" data-end="844" class="" style="">
<p data-start="824" data-end="844" class="">로그 파일 (<code data-start="831" data-end="843">result.log</code>)</p>
</li>
</ul>
<hr data-start="846" data-end="849" class="" style="">
<p data-start="851" data-end="880" class="">원하신다면, 다음 항목도 함께 작성해드릴 수 있어요:</p>
<ul data-start="882" data-end="960">
<li data-start="882" data-end="897" class="" style="">
<p data-start="884" data-end="897" class="">구현 방식 및 로직 설명</p>
</li>
<li data-start="898" data-end="915" class="" style="">
<p data-start="900" data-end="915" class="">사용한 외부 라이브러리 목록</p>
</li>
<li data-start="916" data-end="933" class="" style="">
<p data-start="918" data-end="933" class="">주요 클래스 및 메서드 설명</p>
</li>
<li data-start="934" data-end="947" class="" style="">
<p data-start="936" data-end="947" class="">테스트 및 검증 방법</p>
</li>
<li data-start="948" data-end="960" class="" style="">
<p data-start="950" data-end="960" class="">개선 방향 / 회고</p>
</li>
</ul>
<p data-start="962" data-end="988" class="">필요하신 항목 있으면 언제든지 말씀해주세요 :)</p></div>



# 프로젝트 설명
테스트입니다.

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
