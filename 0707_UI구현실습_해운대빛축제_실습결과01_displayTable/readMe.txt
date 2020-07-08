● UI(User Interface, 사용자 화면)
    사용자 + 표면, 얼굴, 대면

[사용자 화면의 발전]
CLI  (Command   Line  Interface)
         명령어           줄      화면
=> GUI  (Graphic User Interface)
               그래픽    사용자  화면

[Wire Frame]
 와이어       프레임
 선(=줄)   형태(=틀)


[Banner, 배너]
광고


[Shortcut, 숏컷]
바로가기


[Process, 처리과정]
  작업순서


[UI 개발 환경에 따른 편집기 분류]

1. HTML, CSS, JS, jQuery, Vue
    작성용 에디터
=> Editplus, Brackets, 
      Visual Studio Code, ...

2. Java, JSP, ...
    작성용 에디터
=> Eclipse 이클립스
     (Editplus, Brackets, 
      Visual Studio Code 등등
      이 편집기들도 작업 가능함)

3. Android 작성용 에디터
=> IntelliJ 인텔리 제이
     (= Android Studio, 
         안드로이드 스튜디오)

------------------------------

[브라켓 기능]
인텔리센스 팝업


[2열 구조 생성방법]
1. Float
   => 3차원으로 대상을 띄워서
        좌/우측으로 배치함
   (내비게이션 메뉴의 메인메뉴
    또는 슬라이드쇼)

2. Position
   =>
   3차원으로 대상을 띄워서
   원하는 위치에 자유자재로
   배치함 + relative, absolute를
   적절히 사용하여 2차원요소들과의
   관계를 유지할 수 있음
   (내비게이션 메뉴의 서브메뉴,
    슬라이드쇼의 텍스트 문구등의
    화면 특정 위치 배치)
    
        
3. Display: Table
   => 2차원구조에서 표형식의
        배치를 만들기 좋은 구조
  (전체 화면의 구조, 
   대상들의 좌우 정렬 및 세로 정렬에
   용이함)

4. Display: Flex
   => Flexbox에 적합한 구조
        박스모델들의 배치에 적합함.
  (전체 화면의 구조,
   갤러리 게시판, 페이지 번호 나누기에
   용이함 - 균등한 배치에 적합)


[해운대 빛축제 전체 2열 구조 적용1]
Display: Table 적용을 위한 3개의 구조
1. display: table;
2. display: table-row;
3. display: table-cell;


<body>
  <div id="wrap"> =>display: table;
    
     <div.tblRow> => display: table-row;
        <#header>  => 왼쪽 1열
                                 display: table-cell;
        
        <div#rightArea> => 오른쪽 2열
                                 display: table-cell;
          <#slideshow>  => 오른쪽 2열        
          <#main>  => 오른쪽 2열        
          <#footer>  => 오른쪽 2열
        </div>

     </div>
  </div>
</body>



[해운대 빛축제 전체 2열 구조 적용2]
Float를 적용을 위한 2개의 구조

<body>
  <div id="wrap">

        <#header>  => 왼쪽 1열
                                 width: 200px; (가정)
                                  float: left;        
                                 
                                 오른쪽 2열은 모두
                                 width: 800px; (가정)
                                  float: right;  또는
                                  float 필요없음 

          <#slideshow>  => 오른쪽 2열              
          <#main>  => 오른쪽 2열        
          <#footer>  => 오른쪽 2열

  </div>
</body>




[해운대 빛축제 전체 2열 구조 적용3]
Position을 적용을 위한 2개의 구조

<body>
  <div id="wrap"> => position: relative;

        <#header>  => 왼쪽 1열
                                 width: 200px; (가정)
                                 position: absolute;        
                                 left: 0px;
                                 top: 0px;
                                 
                                 오른쪽 2열은 모두
                                 width: 800px; (가정)
                                 position: absolute;        
                                 left: 210px;

          <#slideshow>  => 오른쪽 2열              
                                 top: 0px;
          <#main>  => 오른쪽 2열   
                                 top: slideshow
                                     높이만큼 적용
          <#footer>  => 오른쪽 2열
                                 top: slideshow+main
                                     높이만큼 적용
  </div>
</body>


[해운대 빛축제 전체 2열 구조 적용4]
Display:flex 를 적용을 위한 2개의 구조

<body>
  <div id="wrap"> => display: flex;

        <#header>  => 왼쪽 1열
                                 width: 200px; (가정)
                                 
        <div#rightArea> => 오른쪽 2열
                                       width: 800px;(가정)
          <#slideshow>
          <#main>
          <#footer>
        </div> <!--#rightArea -->
  </div>
</body>




