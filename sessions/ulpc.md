# Peer-to-Peer Folder Poetry – ulpc

![](images/poster.png)

## 세션 준비

### 1. 실험 세션 자료를 한 부 씩 가져가세요.
아래 명령을 한 줄 씩 터미널에 붙여넣고 엔터를 쳐보세요.

```bash
cd ~
git clone https://github.com/ff4f01/Peer-to-Peer-Folder-Poetry.git
```

### 2. Node.js와 Dat을 설치합시다.

```bash
touch ~/.bash_profile
curl https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.0/install.sh | bash
source ~/.bash_profile
nvm install --lts
nvm use --lts
npm install -g dat
```

### 3. 그리고 tree를 설치합시다.

#### macOS

> homebrew가 설치되어있는 분은 첫 번째 명령을 건너뛰세요.

```bash
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew install tree
```

#### Windows10 (WSL)

```bash
sudo apt-get update
sudo apt-get install tree
```

### 4. 오늘의 시제는 '내가 사는 동네'입니다.

실험 세션에 모인 우리는 각기 다른 동네에서 왔습니다. 내가 사는 동네는 어떤 곳인가요? 아래 몇 가지 질문을 읽으며 떠오르는 생각을 글이나 그림으로 스케치해봅시다.

- 동네 이름은 무엇인가요? 혹시 이름의 유래를 알고 계세요?
- 오래된 동네인가요, 비교적 새로 생긴 동네인가요?
- 나는 이 동네에 얼마나 오래 살았나요?
- 이 동네에 사는 친구들이 많나요?
- 산책하기 좋은 공원이 있나요?
- 이 동네에서 꼭 가봐야 하는 곳이 있나요?
- 동네에서 있었던 재미있는 에피소드를 떠올려보세요.
- 동네에 나만 아는 구석이 있나요?

## 파트 I: 폴더, 폴더 시

- 파일시스템과 폴더
- 우리가 평소에 폴더를 관리하는 방법
- 폴더 시를 소개합니다

> 컴퓨터 폴더 구조를 이용해 쓰는 시. 폴더와 파일에 리드미컬한 이름을 붙여 운율을 만들거나, 폴더를 타고 타고 들어가며 이어지는 스토리를 만들거나, 눈 앞에 펼쳐진 여러 개의 폴더 중에 독자가 스스로 선택해나가는 모험을 만들어보세요.

- 몇가지 폴더 시 예시
  - 📒[Download: Folder Poetry - SFPC Yamaguchi Japan Zine](https://melanie-hoff.com/folder-poetry/sfpc-ycam/zine-pdfs-ycam-folder-poetry.zip)
  - 📒[Download: Folder Poetry - SFPC Detroit Zine](https://melanie-hoff.com/folder-poetry/sfpc-detroit/detroit-zine-reader.pdf.zip)
  - [folderpoetry.club](http://folderpoetry.club)

## 파트 II: CLI, Bash, 그리고 터미널

| 용어 | 해설 |
| - | - |
| CLI | Command line interface. 터미널을 통해 사용자와 컴퓨터가 상호 작용하는 방식. 작업 명령은 사용자가 컴퓨터 키보드 등을 통해 문자열의 형태로 입력하며, 컴퓨터로부터의 출력 역시 문자열의 형태로 주어진다. ([출처](https://ko.wikipedia.org/wiki/%EB%AA%85%EB%A0%B9_%EC%A4%84_%EC%9D%B8%ED%84%B0%ED%8E%98%EC%9D%B4%EC%8A%A4)) |
| 셸 | 키보드로 명령어를 입력하고 운영체제가 구동하도록 하는 프로그램 ([출처](http://www.looah.com/article/view/1451)) |
| Bash | Unix의 기본 셸 프로그램인 sh의 개량형 ([출처](http://www.looah.com/article/view/1451)) |
| 터미널 | 윈도우상에서 쉘에 명령어를 보내고 결과를 받아볼수 있는 프로그램 ([출처](http://www.looah.com/article/view/1451)) |

### 몇 가지 Bash 명령

| 명령 | 설명 |
| - | - |
| `cd` | 홈 디렉토리 이동 |
| `cd ulpc` | `ulpc` 디렉토리로 이동 |
| `cd ..` | 디렉토리 한 단계 위로 이동 |
| `ls` | 파일 및 디렉토리 목록 보기 |
| `pwd` | 현재 위치한 디렉토리 경로 확인 |
| `mkdir foldername` | `foldername`이라는 이름의 디렉토리 생성 |
| `touch kitty.txt` | `kitty.txt`라는 이름의 빈 파일 생성 |
| `echo "woof woof" > kitty.txt` | "woof woof"라는 내용으로 `kitty.txt` 파일 생성 |
| `cat kitty.txt` | 파일 내용 보기 |
| `rm -i kitty.txt` | 파일 삭제 |
| `mv kitty.txt doggy.txt` | 파일 이름 바꾸기 |
| `cp kitty.txt kitty2.txt` | 파일 복사 |
| `say "안녕하세요"` | (macOS) 소리내어 읽기 |

### 파일 내용 쓰기
| 명령 | Description |
| - | - |
| `echo "woof woof" > kitty.txt` | "woof woof"라는 내용으로 `kitty.txt` 파일 생성 |
| `nano kitty.txt` | nano 텍스트 에디터에서 파일 열기 |
| `CTRL + x`, `y`, `ENTER` | 변경사항 저장하고 파일 닫기 |

### 몇 가지 유용한 팁

| 명령 | 설명 |
| - | - |
| 위 아래 화살표 키 | 이전 명령 목록에서 선택 |
| Tab | 명령 자동완성 |
| CMD + CTRL + SPACE | (MacOS) Emoji 키보드 |
| 윈도우 로고키 + ;  | (Windows) Emoji 키보드 |

## 파트 III: 오늘의 폴더 시 - 내가 사는 동네

아까 준비한 스케치를 참고해 폴더 시를 써봅시다.

* 내가 사는 동네를 묘사하는 시를 써도 좋고
* 동네의 공간적인 구성을 폴더로 표현해도 좋고
* 동네만의 매력을 느낄 수 있는 [어드벤처](http://bit.ly/2D2fC00)를 소개해도 좋습니다. 

### 폴더 시는 여기에 쓸 거에요

```bash
cd
mkdir folder-friends
mkdir folder-poetry
cd folder-poetry
mkdir {yourname}-home
cd {yourname}-home
 ```

## Part IV: 폴더 시 P2P 네트워크로 전달하기

### Dat P2P 네트워크로 시를 전송할 때 주의점

폴더 시를 Dat P2P 네트워크로 전달하기 위해서는 몇 가지 규칙을 따라야 합니다. 규칙을 따르지 않아도 여러분은 멋진 시를 쓸 수 있지만, 서로에게 시를 전달하기 위해서는 규칙을 지켜주시기 바랍니다.

* 빈 폴더는 전달되지 않습니다.
* 빈 파일은 전달되지 않습니다.
* 폴더명, 파일명은 공백 없이 한글 또는 영문으로 지어주세요.
  * 공백은 밑줄(`_`)로 대체 가능합니다. 예를 들면: `my_file.txt`

### Dat P2P 네트워크로 폴더 시 공유하기

- 새 터미널 창을 엽니다.
- `cd folder-poetry` 내 폴더 시가 있는 디렉토리로 이동합니다. 
- `dat share` Dat P2P 네트워크에 내 폴더시를 공유합니다.
- 출력된 Dat 주소를 복사해 [이 스프레드시트](https://docs.google.com/spreadsheets/d/17sJfU76S0reKXdZQFf2pfvhvlxMezjNOh4cIqMIU7ac/edit?usp=sharing)의 본인 이름 옆에 붙여넣으세요.
- 여러분의 폴더 시는 이 창이 살아있는 동안 Dat으로 공유됩니다. 창을 그대로 최소화하고 건드리지 마세요. 

### Dat P2P 네트워크로 친구의 폴더 시 가져오기

- `cd folder-friends`
- `dat clone {스프레드시트에서 복사한 친구의 Dat Hash 주소}`
- `cd {Dat Hash}`
- `tree` 친구의 폴더 시 펼쳐보기
