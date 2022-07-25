# 요구사항 분석

- 목록 화면
    - 전체 목록을 페이징 처리해서 조회
    - 제목/내용/작성자 항목으로 검색과 페이징처리
- 등록 화면
    - 새로운 글을 등록
    - 등록 처리 후 다시 목록 화면으로 이동
- 조회 화면
    - 목록 화면에서 특정한 글을 선택하면 자동으로 조회 화면으로 이동
    - 조회 화면에서는 수정/삭제가 가능한 화면으로 버튼을 클릭해서 이동
- 수정/삭제 화면
    - 수정화면에서 삭제가 가능
    - 삭제 후 목록 페이지로 이동
    - 수정후 다시 조회 화면으로 이동


# API규격서
![API](https://user-images.githubusercontent.com/97961558/180807971-b210a977-ca58-48e0-9ff1-eb6803c1c329.PNG)

- 목록
    - URL
        - /guestbook/list
            - GET
            - 기능 : 목록/페이징/검색
            - Redirect URL : NULL
- 등록
    - URL
        - /guestbook/register
            - GET
            - 기능 : 입력화면
            - Redirect URL :
    - URL
        - /guestbook/register
            - POST
                - moddate : 2022-07-24 18:55:44.912000
                - regdate : 2022-07-24 18:55:44.912000
                - content : Content…1
                - title : Title….1
                - writer : user1
            - 기능 : 등록 처리
            - Redirect URL : /guestbook/list
- 조회
    - URL: /guestbook/read
        - GET
        - 기능 : 조회 화면
        - Redirect URL : NULL
- 수정
    - URL:/guestbook/modify
        - GET
        - 기능 : 수정/삭제 가능 화면
        - Redirect URL :
    - URL:/guestbook/modify
        - POST
            - moddate : 2022-07-24 18:55:44.912000
            - regdate : 2022-07-24 18:55:44.912000
            - title : title…2
            - content : content….2
        - 기능 : 수정처리
        - Redirect URL : /guestbook/read
- 삭제
    - URL:/guestbook/remove
        - POST
            - moddate : NULL
            - regdate : NULL
            - content : NULL
            - title : NULL
            - writer : NULL
        - 기능 : 삭제처리
        - Redirect URL : /guestbook/list

# 엔티티 관계도
![엔티티1](https://user-images.githubusercontent.com/97961558/180763244-f89baaf8-0985-4060-ac6f-8027c5abd68c.PNG)
![엔티티2](https://user-images.githubusercontent.com/97961558/180763248-ab49c90f-31e2-4ebc-940a-c722585f16f3.PNG)
![엔티티3](https://user-images.githubusercontent.com/97961558/180763249-a1dbc50d-c2fc-4b10-9c1c-a326838103e8.PNG)


# 색깔 바꾸기
![캡처](https://user-images.githubusercontent.com/97961558/180749739-20bc9e51-1343-475c-ae8d-963e40635144.PNG)
