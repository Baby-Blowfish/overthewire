# Bandit Level 0 → Level 1

OverTheWire: [Bandit](https://overthewire.org/wargames/bandit/)

---

## 📌 문제 요약

- **접속 방식**: SSH
- **사용자**: `bandit0`
- **비밀번호**: `bandit0`
- **호스트 주소**: `bandit.labs.overthewire.org`
- **포트 번호**: `2220`
- **목표**: 서버에 접속한 후 `/etc/bandit_pass/bandit0` 파일에서 다음 단계의 비밀번호를 확인

---

## 🧠 학습 내용 요약

### ✅ 1. SSH 포트 변경

기본 포트는 `22`이지만 Bandit 서버는 `2220`번 포트를 사용하므로 아래와 같이 접속해야 함:

```bash
ssh -p 2220 bandit0@bandit.labs.overthewire.org
```
### 2. sshpass를 사용한 자동로그인

```bash
sudo apt install sshpass
sshpass -p "bandit0" ssh -p 2220 bandit0@bandit.labs.overthewire.org
```

### 3.  scp로 원격 파일 복사
```bash
scp -P 2220 bandit0@bandit.labs.overthewire.org:/path/to/file ./localdir/
scp -r -P 2220 bandit0@bandit.labs.overthewire.org:/path/to/dir ./localdir/
sshpass -p "bandit0" scp -P 2220 bandit0@bandit.labs.overthewire.org:/path/to/file ./localdir/
```





