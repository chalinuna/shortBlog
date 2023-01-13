# shortBlog

Github: https://github.com/chalinuna/shortBlog

Hosting: https://chalinuna.github.io/

Blog : https://make-somthing.tistory.com/6

## Tool
React (Redux Toolkit, useSelector, useNavigator, useState, useDispatch, useEffect, localStorage, Route, URL Prams, sessionStorage)


### LocalsPost.js
▶ sessionStorage.getItem을 사용해 현재 로그인 상태인지 세션값을 받아와, 로그인 상태일 경우 1페이지를, 로그인하지 않은 상태일 경우 2페이지를 출력한다..

★ 만일 포스트를 Redux 에만 저장하면 새로고침 할 경우 사라진다. Local Storage에 추가로 저장하지 않고 Redux에만 저장할 경우에는 아래 코드를 사용한다. useSelector를 이용해 store.js에 있는 Redux 내의 state값을 모두 불러오고, dispatch로 리듀서들을 사용한다. 

### Profile.js , LoginPage.js, Register.js

▶ 이메일, 닉네임, 비밀번호로 회원가입 및 로그인 기능을 제공한다.(db나 백엔드 서버가 꾸려져 있는 것이 아니기 때문에 LocalStorage에 저장한다.)

▶로그인 상태에 따라 Profile UI 및 상단바가 다르게 보이도록 컴포넌트를 IF문 처리한다.


### Write.js 

▶ 글쓰기 창을 보여준다.

▶제출을 누르면 Redux Store와 Local Storage에 값을 추가한다.


### Rightlist.js

▶ 로그인 한 상태라면 아래처럼 현재 작성한 포스트의 제목들을 출력한다.

▶제목을 클릭하면, 내가 작성한 글을 볼 수 있는 detail 페이지로 이동한다.


### Postdetail.js, Edit.js 

▶ 로그인 한 상태에서 포스트 목록, 또는 포스트 디테일 페이지의 [ 수정 ] 버튼을 누르면, 포스트를 수정할 수 있는 Edit 창으로 이동한다.

▶ 수정한 글은 Redux Store와 Local Storage에 모두 반영되어 제출 버튼을 누르면 home화면에서 즉시 업데이트 된다.
