# Bandit Level 5 → Level 6

OverTheWire: [Bandit Level 5](https://overthewire.org/wargames/bandit/level5.html)

---

## 🎯 문제 요약

- **현재 계정**: `bandit5`
- **접속 정보**:
  ```bash
  ssh -p 2220 bandit5@bandit.labs.overthewire.org
  ```

## solution

find [경로] [조건] [동작]


# 1. 크기가 1033바이트인 파일 찾기
find inhere/ -type f -size 1033c
find . -name "file.txt"
find . -name "*.log"
find . -iname "*.jpg"

find . -type f        # 일반 파일만 찾기
find . -type d        # 디렉토리만 찾기
find . -type i        # simbolic link

find . -size 1033c         # 1033바이트인 파일
find . -size +1M -type f   # 1MB 초과 파일
find . -size -100k -type f   # 100kb under

find . -perm 755          # 권한이 정확히 755
find . -perm -111         # 실행 권한이 있는 파일

find . -type f -name "*.txt" -exec cat {} \;

find . -mtime -1       # 1일 이내 수정된 파일
find . -newer 기준파일  # 기준 파일보다 나중에 수정된 파일


# 예: 결과가 1개라면
file inhere/mysteryfile
ls -l inhere/mysteryfile

# 2. 사람이 읽을 수 있고 실행 불가능하면 출력
cat inhere/mysteryfile

# 종료
exit

