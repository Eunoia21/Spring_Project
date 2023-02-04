# Spring_Project
크롤링 프로젝트 연계 프로젝트

# 크롤링 베이스 페이지
- yes24 월별 베스트 셀러 :http://www.yes24.com/24/category/bestseller?CategoryNumber=001&sumgb=09

# 크롤링 Data
- Rank 랭크
- Category 카테고리
- Title 제목
- Author 저자
- Pub 출판사
- Price  가격
- Summary 줄거리
- Grade 평점 
- Pictureurl지이미지

# DB

CREATE TABLE Book (
 num number(35) primary key,
 Category NVARCHAR2(1000),
 Title NVARCHAR2(1000), 
 Price NVARCHAR2(20), 
 Summary VARCHAR2(4000 BYTE),
 Author NVARCHAR2(1000), 
 Pub NVARCHAR2(1000),
 Grade NVARCHAR2(20),
 Pictureurl varchar2(4000 BYTE)
);

create table member(
    id varchar2 (20 BYTE) PRIMARY key,
    pass varchar2 (20 BYTE),
    name varchar2 (10 BYTE),
    phone char (15 BYTE),
    email varchar2 (20 BYTE),
    lev char(1) DEFAULT 'B'   --권한 'A' -> 관리자 // 'B' -> 일반회원
);


commit;
