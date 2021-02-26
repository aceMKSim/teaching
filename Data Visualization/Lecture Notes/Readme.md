## Lecture Notes (2020 Spring)

## L4.Sec2 pdf문서관련 추가내용

+ `L4,p11`에서 나눔고딕, 나눔명조, 나눔고딕코딩을 다운로드 해서 설치하라고 하였는데,
+ 이 과정을 거치고도 `pdf_plain.Rmd`가 폰트가 없다는 에러메시지가 뜨면서 컴파일이 안 되는 경우가 있다.
+ 이럴 때에는 아래의 과정을 거치면 된다.
    1. Windows 시작 버튼을 누르고 `TeX Live command-line`라는 프로그램을 찾아 실행한다. 그렇다면 도스창이 뜬다.
    2. 다음의 코드를 입력한다: `tlmgr repository add http://ftp.ktug.org/KTUG/texlive/tlnet/ ktug` (마지막의 띄어쓰기 조심)
    3. 다음의 코드를 입력한다: `tlmgr install nanumttf`
+ 그래도 안되면 이메일을 보내주세요.
