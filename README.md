
# PoseCure_app

-윈도우에서 리눅스 환경 설치

1. 윈도우 최신 버전으로 업데이트
 - 제어판 -> 프로그램 기능 -> windows 기능 켜기/끄기 -> Linux 용 windows 하위 시스템, Hyper-V 체크
2. MicroSoft Store에서 Terminal, Ubuntu 20.04 LTS 설치
3. Terminal 접속 후 settings 접속
4. "defaultProfile" 에 설치한 Ubuntu guid 입력
5. ZSH 설치
 - sudo apt-get install zsh -> 재부팅
 - sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
6. 테마 설정
 - sudo vim .zshrc
 - ZSH_THEME="agnoster" 변경
7. "schemes" 에 아래 내용 입력
"schemes": [
        {
             "background" : "#002B36",
             "black" : "#002B36",
             "blue" : "#268BD2",
             "brightBlack" : "#657B83",
             "brightBlue" : "#839496",
             "brightCyan" : "#D33682",
             "brightGreen" : "#B58900",
             "brightPurple" : "#EEE8D5",
             "brightRed" : "#CB4B16",
             "brightWhite" : "#FDF6E3",
             "brightYellow" : "#586E75",
             "cyan" : "#2AA198",
             "foreground" : "#93A1A1",
             "green" : "#859900",
             "name" : "wsl",
             "purple" : "#6C71C4",
             "red" : "#DC322F",
             "white" : "#93A1A1",
             "yellow" : "#B58900"
        }
    ],

8. 폰트 설정, https://github.com/powerline/fonts.git
 - 해당 사이트 접속 후 code -> download zip
 - 압축 해제 후 원하는 폰트 설치
 - termianl -> setting -> defaults
           "fontFace":"설치한 폰트 이름",
           "fontSize":12
