# Bandit Level 4 → Level 5

OverTheWire: [Bandit Level 4](https://overthewire.org/wargames/bandit/level4.html)

---

## 🎯 문제 요약

- **현재 계정**: `bandit4`
- **접속 정보**:
  ```bash
  ssh -p 2220 bandit4@bandit.labs.overthewire.org
  ```

## 학습내용

```bash
file [옵션] 파일이름
```
- 파일의 **형식(type)** 을 출력합니다.
- 예: 텍스트, 바이너리, 실행 파일, 이미지, 압축파일, 키 파일 등


## 🔍 예시

```bash
file hello.txt
```

출력:
```
hello.txt: ASCII text
```

```bash
file program
```

출력:
```
program: ELF 64-bit LSB executable, x86-64, ...
```


## 📁 예시: 다양한 파일 형식 결과

| 명령어                       | 출력 예시                                | 설명 |
|-----------------------------|------------------------------------------|------|
| `file test.txt`             | ASCII text                               | 일반 텍스트 |
| `file image.png`            | PNG image data, 800 x 600, 8-bit/color   | 이미지 |
| `file script.sh`            | Bourne-Again shell script, ASCII text    | bash 스크립트 |
| `file binaryfile`           | data                                     | 사람이 읽을 수 없는 데이터 |
| `file mykey.asc`            | PGP public key block                     | 키 파일 |


## ✅ 자주 사용하는 옵션

| 옵션        | 설명 |
|-------------|------|
| `-b`        | 파일 이름을 출력하지 않고 타입만 표시 |
| `-i`        | MIME 타입 출력 (ex: `text/plain; charset=us-ascii`) |
| `--mime`    | 위와 동일 |
| `-f 파일목록` | 여러 파일 이름이 들어 있는 파일로 일괄 검사 |
| `-z`        | 압축되어 있는 파일의 내부까지 검사 (gzip 등) |

---

## 📚 실용적인 예제

### 여러 파일 검사
```bash
file *
```

### 숨김 파일 포함해서 검사
```bash
file .*
```

---

## 🧠 file이 어떻게 동작하나?

- 파일 내용을 **Magic Number**로 분석합니다.
- `/usr/share/file/magic.mgc` 파일에 정의된 **파일 시그니처** 정보를 기반으로 분석합니다.
- 파일 확장자와 관계없이 동작 → 보안/포렌식/스크립트 자동화에서 매우 유용
---

