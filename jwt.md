![alt text](image.png)

![alt text](image-1.png)

![alt text](image-2.png)

![alt text](image-3.png)

MariaDB [test_NestJS]> INSERT INTO `test_NestJS`.`UsersAuthority` (users_id, authority_name) VALUES (1, 'ROLE_USER');

MariaDB [test_NestJS]> INSERT INTO `test_NestJS`.`UsersAuthority` (users_id, authority_name) VALUES (1, 'ROLE_ADMIN');

MariaDB [test_NestJS]> INSERT INTO `test_NestJS`.`UsersAuthority` (users_id, authority_name) VALUES (2, 'ROLE_USER');

권한 추가 로그인
![alt text](image-4.png)

로그인 후 다시 인증 요청
![alt text](image-5.png)

권한만 나오게 수정 

다시 로그인
![alt text](image-6.png)

권한 요청
![alt text](image-7.png)

어드민 권한에 따른 요청
다시 로그인
![alt text](image-8.png)

![alt text](image-9.png)

어드민 권한이 아닌 다른 요청
![alt text](image-10.png)


![alt text](image-11.png)