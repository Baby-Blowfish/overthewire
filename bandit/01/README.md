문제 : ssh 접속
아이디 : bandit0
비밀번호 : bandit0
주소 : bandit.labs.overthewire.org
포트번호 : 2220

기본 ssh 접속 포트 설정은 22
접속 포트 번호를 수정해야함
기본 접속 포트번호 바꾸려면 /etc/ssh/sshd_config 파일의 Port = 포트번호로 수정

ssh -p 포트번호 사용자@호스트

scp -p 포트번호 사용자@호스트:원격경로 로컬경로

scp -r -p 포트번호 사용자@호스트:원격경로 로컬경로

sshpass -p "비밀번호" ssh 사용자@주소

sshpass -p "비밀번호" ssh -p 포트번호 사용자@주소


sshpass -p "비밀번호" scp -P 포트번호 사용자@호스트:원격경로 로컬경로



`-`인 파일 이름 읽기
touch에서 `touch -`하면 명령어가 옵션으로 생각함
`--`를 통해서 여기서부터는 옵션 아님이라는 옵션을 줘야함
`touch -- -`
아니면 경로로 지정해서 옵션으로 해석되지 않게함
`cat ./-`



