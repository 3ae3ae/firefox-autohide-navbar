# Firefox 주소창 자동 숨김 기능

[ENGLISH](README.md) | 한국어

이 userChrome.css 스니펫은 Firefox 브라우저의 주소창과 제목 표시줄을 자동으로 숨기는 기능을 제공합니다. 마우스를 위쪽으로 이동하면 요소들이 나타나고, 마우스를 다른 곳으로 이동하면 자동으로 숨겨집니다.

## Features

- 주소창과 제목 표시줄 자동 숨김
- 마우스 호버 시 요소 표시
- 부드러운 전환 효과

## Installation

1. Firefox의 설정에서 `about:config`를 열고 `toolkit.legacyUserProfileCustomizations.stylesheets`를 `true`로 설정합니다.
2. Firefox 프로파일 폴더를 찾습니다. (`about:support`에서 "프로파일 폴더" 항목 참조)
3. 프로파일 폴더 내에 `chrome` 폴더를 생성합니다. (없는 경우)
4. `chrome` 폴더 안에 `userChrome.css` 파일을 생성하고 다음 코드를 붙여넣습니다:

```css
#navigator-toolbox:not(:hover) > #titlebar,
#navigator-toolbox:has(#PersonalToolbar:hover) > #titlebar,
#navigator-toolbox:not(:hover) > #nav-bar,
#navigator-toolbox:has(#PersonalToolbar:hover) > #nav-bar {
  margin-top: -36px;
  opacity: 0;
}

#titlebar, #nav-bar {
  transition: all 0.3s ease-in-out !important;
}
```

5. Firefox를 재시작합니다.

## Customization

- `-36px`의 값을 조절하여 숨김 정도를 변경할 수 있습니다.
- `0.3s`의 값을 조절하여 전환 속도를 변경할 수 있습니다.

## Caution

이 CSS 스니펫은 Firefox의 최신 버전을 기준으로 작성되었습니다. 향후 Firefox 업데이트로 인해 동작이 변경될 수 있습니다.

## Troubleshooting

주소창이 보이지 않는 경우, 마우스를 브라우저 상단으로 이동하세요. 그래도 문제가 지속된다면 `about:support`에서 "Firefox 새로고침"을 시도해보세요.
