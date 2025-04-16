# Bandit Level 1 → Level 2

OverTheWire: [Bandit](https://overthewire.org/wargames/bandit/level1.html)

---

## 🎯 문제 요약

- **현재 계정**: `bandit1`
- **접속 방법**:
  ```bash
  ssh -p 2220 bandit1@bandit.labs.overthewire.org
  ```
## 학습 내용 요약

### `-`로 시작하는 파일 이름 처리
- 파일 이름이 `-`인 경우 명령어가 이를 옵션으로 오인
- 명령어가 옵션으로 오인하지 않도록 해야함
- `--`
- 경로


### sed, head
```bash
sed [옵션] '명령' 파일
sed -n '2' file.txt
sed -n '2,4p` file.txt

head [옵션] 파일
head -n 3 file.txt
```

