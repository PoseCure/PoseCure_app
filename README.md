
# PoseCure_app

-윈도우에서 리눅스 환경 설치

1. 윈도우 최신 버전으로 업데이트
 - 제어판 -> 프로그램 기능 -> windows 기능 켜기/끄기 -> Linux 용 windows 하위 시스템, Hyper-V 체크
2. MicroSoft Store에서 Terminal, Ubuntu 20.04 LTS 설치
3. Terminal 접속 후 settings 접속
4. "defaultProfile" 에 설치한 Ubuntu guid 입력 //하단에 보면 있음 ㅎㅎ
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
 - 압축 해제 후 DejaVu Sans Mono Powerline 설치
 - termianl -> setting -> defaults
           "fontFace":"DejaVu Sans Mono Powerline",
           "fontSize":12
           
###### 위 설정을 하고 이상하다면 아래 내용을 setting에 복붙하시오#####
// This file was initially generated by Windows Terminal 1.2.2381.0
// It should still be usable in newer versions, but newer versions might have additional
// settings, help text, or changes that you will not see unless you clear this file
// and let us generate a new one for you.

// To view the default settings, hold "alt" while clicking on the "Settings" button.
// For documentation on these settings, see: https://aka.ms/terminal-documentation
{
    "$schema": "https://aka.ms/terminal-profiles-schema",

    "defaultProfile": "{07b52e3e-de2c-5db4-bd2d-ba144ed6c273}",

    // You can add more global application settings here.
    // To learn more about global settings, visit https://aka.ms/terminal-global-settings

    // If enabled, selections are automatically copied to your clipboard.
    "copyOnSelect": false,

    // If enabled, formatted data is also copied to your clipboard
    "copyFormatting": false,

    // A profile specifies a command to execute paired with information about how it should look and feel.
    // Each one of them will appear in the 'New Tab' dropdown,
    //   and can be invoked from the commandline with `wt.exe -p xxx`
    // To learn more about profiles, visit https://aka.ms/terminal-profile-settings
    "profiles":
    {
        "defaults":
        {
           "fontFace":"DejaVu Sans Mono for Powerline",
           "fontSize":12
        },
        "list":
        [
            {
                // Make changes here to the powershell.exe profile.
                "guid": "{61c54bbd-c2c6-5271-96e7-009a87ff44bf}",
                "name": "Windows PowerShell",
                "commandline": "powershell.exe",
                "hidden": false
            },
            {
                // Make changes here to the cmd.exe profile.
                "guid": "{0caa0dad-35be-5f56-a8ff-afceeeaa6101}",
                "name": "명령 프롬프트",
                "commandline": "cmd.exe",
                "hidden": false
            },
            {
                "guid": "{b453ae62-4e3d-5e58-b989-0a998ec441b8}",
                "hidden": false,
                "name": "Azure Cloud Shell",
                "source": "Windows.Terminal.Azure"
            },
            {
                "guid": "{07b52e3e-de2c-5db4-bd2d-ba144ed6c273}",
                "hidden": false,
                "name": "Ubuntu-20.04",
                "source": "Windows.Terminal.Wsl",
	    "colorScheme": "wsl",
            }
        ]
    },

    // Add custom color schemes to this array.
    // To learn more about color schemes, visit https://aka.ms/terminal-color-schemes
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

    // Add custom keybindings to this array.
    // To unbind a key combination from your defaults.json, set the command to "unbound".
    // To learn more about keybindings, visit https://aka.ms/terminal-keybindings
    "keybindings":
    [
        // Copy and paste are bound to Ctrl+Shift+C and Ctrl+Shift+V in your defaults.json.
        // These two lines additionally bind them to Ctrl+C and Ctrl+V.
        // To learn more about selection, visit https://aka.ms/terminal-selection
        { "command": {"action": "copy", "singleLine": false }, "keys": "ctrl+c" },
        { "command": "paste", "keys": "ctrl+v" },

        // Press Ctrl+Shift+F to open the search box
        { "command": "find", "keys": "ctrl+shift+f" },

        // Press Alt+Shift+D to open a new pane.
        // - "split": "auto" makes this pane open in the direction that provides the most surface area.
        // - "splitMode": "duplicate" makes the new pane use the focused pane's profile.
        // To learn more about panes, visit https://aka.ms/terminal-panes
        { "command": { "action": "splitPane", "split": "auto", "splitMode": "duplicate" }, "keys": "alt+shift+d" }
    ]
}
############################################
