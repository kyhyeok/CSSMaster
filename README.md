# CSSMaster

CssMasterClassWithNomadCoder

# =========================== Flex 시작 ===========================

flex는 부모와 자식 관계에서만 작용된다.

display: flex;가 적용된 태그에서 justify-content 등의 명령어를 사용할 수 있다.

justify-content는 가로(수평)로 배열해주는 CSS 명령어, align-items는 세로(수직)로 배열해주는 CSS 명령어

Main Axis는 justify-content 이고 Cross Axis는 align-items 이다.

flex-direction의 기본값은 row이고 flex-direction의 방향에 따라 Main Axis와 Cross Axis가 달라진다.

Flex Warp은 nowrap이 기본값이다. flex안에 아이템들이 서로 잘 맞지 않을 때 사용한다.

Align Self 설정한 간 flex만 적용된다.

# =========================== Flex 끝 ===========================

# =========================== Grid 시작 ===========================

# 2020-03-09 기준으로 크롬, 파이어폭스, 네이버 웨일, 익스 엣지는 되고 익스는 적용이 안 된다.

grid는 부모자식 관계에 적용된다. display: grid;로 적용한다.

grid-template-columns는 가로방향의 값, grid-template-rows는 세로 방향의 값, grid-gap는 사이에 값이다.

columns는 width, rows는 height라고 개념 잡으면 편할 듯

grid는 auto-columns와 auto-rows가 존재한다.

grid-auto-rows: 60px하면 rows값을 60px으로 정의를 해 놓는 것이다.

값이 정해지지 않는 rows의 값을 60px로 설정이 되는 것

grid-template-areas는 "header"나 "content sidebar" 이런식으로 사용가능

ex) grid-template-areas "header header" "content sidebar" "footer footer"로 지정한다음

자식 요소에서 grid-area: header나 grid-area: content grid-area: sidebar grid-area: footer로

미리 지정한 요소를 가져다가 사용할 수 있다

"" 안에 header가 2개면 column을 3개 차지한다는 뜻이고 3개면 3개 찾이 한다는 뜻이다.

입력한 숫자만큼의 컬럼을 차지한다는 뜻

fr은 컬럼이 m/n을 지정하는 방식으로

grid가 네 상자가 있다는 가정하에 grid-template-columns 2fr 1fr 2fr 1fr을 할 경우

총 6/6fr이고 여기서 위 fr을 적용하면 2/6fr 1/6fr 2/6fr 1/6fr이 된다.

repeat은 반복은 주는 것이다.

repeat(4, 1fr)은 1/4fr으로 나누는 것과 같고

repeat(3, 1fr) 4fr은 총 7/7fr에서 앞에 3개는 1/7fr 뒤에는 4/7fr로 css가 적용이 된다.

minmax(400px, 2fr)이면 최소로 줄여도 400px이하로는 줄어들지 않는 것

max-content나 min-content는 content를 기반으로 작용한다.

max-content는 최대한 공간을 사용하게 해준다.

min-content는 max-content랑 반대로 최대한 공간을 줄여서 사용한다. rows값을 잘 봐야 한다.

auto-fill은 공간을 남기지 않고 다 채우지만

auto-fit은 빈 공간에 허상의 box를 만들어 채운다/

Justify-content는 수평에 적용하고 Align-content은 수직에 적용된다.

place-content는 2개의 아규먼트가 있는데 첫 번째는 align(수직)이고 두 번째는 justify(수평)이다

place-content: center end;를 하면 수직은 가운데 수평은 끝이다.

Justify-Items box안에서 수평에 적용하고 Align-Items는 박스안에서 수평에 적용된다.

Place-Items는 2개의 아규먼트가 있는데 첫 번째는 박스 안에서의 align(수직)이고 두 번째는 박스 안에서의 justify(수평)이다

grid-column-start: 1 grid-column-end: 5

grid-column-start과 grid-column-end은 column1부터 5까지가 아니라 line으로 잡는다.

grid-column 1 / 5 하면 start1 / end5와 같다 end를 -1로 하면 그 줄에 전체를 의미한다.

grid-row로 똑같다

grid-row : span 기능이 있다 span은 처음부터 바로 끝을 간다 span 5 하면 start1 end5dhk 같은 의미이다.

grid-row : span3 grid-column: span3하면 가로 세로 3칸씩이다.

grid-area도 있다.

Justify, Align, Place Self도 flexbox와 비슷하게 사용 가능하다(모르면 검색 ㄱㄱ)

# =========================== Grid 끝 ===========================

# =========================== PostCSS 시작 ===========================

npm init -y scripts에서 test 지우고

npm install -g parcel-bundler 해서 설치하고

index.html 파일 만들고 styles.css만들고

# =========================== PostCSS 끝 ===========================
