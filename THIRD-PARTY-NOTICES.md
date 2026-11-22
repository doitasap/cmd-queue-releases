# 서드파티 고지 (Third-Party Notices)

CmdQ 는 아래 서드파티 구성요소를 포함하거나 링크한다. 각 구성요소는 자신의 라이선스를
따르며, 이 파일은 그 라이선스들이 요구하는 고지를 한곳에 모은 것이다. CmdQ 자체의
라이선스는 [LICENSE](LICENSE) 를 참조한다.

이 파일은 배포물(DMG)과 배포 저장소에 함께 포함된다 — 고지 의무는 사본마다 발생하므로
소스 저장소에만 두어서는 이행되지 않는다.

---

## 1. 번들 폰트 — D2Coding · Pretendard

앱은 D2Coding 폰트를 `src/assets/fonts/D2Coding.ttf` 로 번들해 배포한다. 한글 글자폭이
라틴의 정확히 2배(1000:500)라 대화형 터미널의 East Asian Wide 배치와 일치하기 때문이다.

```
Copyright (c) 2015-2016 NHN Corporation. All rights reserved.
Font designed by FONTRIX Inc.

D2Coding is a registered trademark of NHN Corporation.

This Font Software is licensed under the SIL Open Font License, Version 1.1.
```

- 배포처: https://github.com/naver/d2codingfont
- 예약 폰트 이름(Reserved Font Name): `D2Coding`

앱은 UI 본문 글꼴로 Pretendard Variable 을 `src/assets/fonts/PretendardVariable.woff2` 로 번들해
배포한다. 배포본 v1.3.9 의 `dist/web/variable/woff2/PretendardVariable.woff2` 를 고치지 않고 그대로
넣었다(서브셋·이름 변경 없음). CDN 에서 받지 않으므로 오프라인에서도 같은 글꼴로 그려진다.

```
Copyright (c) 2021, Kil Hyung-jin (https://github.com/orioncactus/pretendard),
with Reserved Font Name Pretendard.

This Font Software is licensed under the SIL Open Font License, Version 1.1.
```

- 배포처: https://github.com/orioncactus/pretendard
- 예약 폰트 이름(Reserved Font Name): `Pretendard`

OFL 1.1 조건 2 는 폰트를 소프트웨어와 함께 번들·재배포할 때 **사본마다 위 저작권 고지와
라이선스 전문이 포함될 것**을 요구한다. 두 폰트 모두 같은 OFL 1.1 이므로 그 전문을 아래에 한 번
그대로 싣는다.

### SIL Open Font License 1.1 전문

```
-----------------------------------------------------------
SIL OPEN FONT LICENSE Version 1.1 - 26 February 2007
-----------------------------------------------------------

PREAMBLE
The goals of the Open Font License (OFL) are to stimulate worldwide
development of collaborative font projects, to support the font creation
efforts of academic and linguistic communities, and to provide a free and
open framework in which fonts may be shared and improved in partnership
with others.

The OFL allows the licensed fonts to be used, studied, modified and
redistributed freely as long as they are not sold by themselves. The
fonts, including any derivative works, can be bundled, embedded,
redistributed and/or sold with any software provided that any reserved
names are not used by derivative works. The fonts and derivatives,
however, cannot be released under any other type of license. The
requirement for fonts to remain under this license does not apply
to any document created using the fonts or their derivatives.

DEFINITIONS
"Font Software" refers to the set of files released by the Copyright
Holder(s) under this license and clearly marked as such. This may
include source files, build scripts and documentation.

"Reserved Font Name" refers to any names specified as such after the
copyright statement(s).

"Original Version" refers to the collection of Font Software components as
distributed by the Copyright Holder(s).

"Modified Version" refers to any derivative made by adding to, deleting,
or substituting -- in part or in whole -- any of the components of the
Original Version, by changing formats or by porting the Font Software to a
new environment.

"Author" refers to any designer, engineer, programmer, technical
writer or other person who contributed to the Font Software.

PERMISSION & CONDITIONS
Permission is hereby granted, free of charge, to any person obtaining
a copy of the Font Software, to use, study, copy, merge, embed, modify,
redistribute, and sell modified and unmodified copies of the Font
Software, subject to the following conditions:

1) Neither the Font Software nor any of its individual components,
in Original or Modified Versions, may be sold by itself.

2) Original or Modified Versions of the Font Software may be bundled,
redistributed and/or sold with any software, provided that each copy
contains the above copyright notice and this license. These can be
included either as stand-alone text files, human-readable headers or
in the appropriate machine-readable metadata fields within text or
binary files as long as those fields can be easily viewed by the user.

3) No Modified Version of the Font Software may use the Reserved Font
Name(s) unless explicit written permission is granted by the corresponding
Copyright Holder. This restriction only applies to the primary font name as
presented to the users.

4) The name(s) of the Copyright Holder(s) or the Author(s) of the Font
Software shall not be used to promote, endorse or advertise any
Modified Version, except to acknowledge the contribution(s) of the
Copyright Holder(s) and the Author(s) or with their explicit written
permission.

5) The Font Software, modified or unmodified, in part or in whole,
must be distributed entirely under this license, and must not be
distributed under any other license. The requirement for fonts to
remain under this license does not apply to any document created
using the Font Software.

TERMINATION
This license becomes null and void if any of the above conditions are
not met.

DISCLAIMER
THE FONT SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO ANY WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT
OF COPYRIGHT, PATENT, TRADEMARK, OR OTHER RIGHT. IN NO EVENT SHALL THE
COPYRIGHT HOLDER BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY,
INCLUDING ANY GENERAL, SPECIAL, INDIRECT, INCIDENTAL, OR CONSEQUENTIAL
DAMAGES, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING
FROM, OUT OF THE USE OR INABILITY TO USE THE FONT SOFTWARE OR FROM
OTHER DEALINGS IN THE FONT SOFTWARE.
```

---

## 2. Rust 의존성 — MPL-2.0

아래 크레이트는 Mozilla Public License 2.0 이다. 이 앱은 해당 크레이트를 **수정하지 않고
링크만** 하므로, MPL-2.0 §3.3(Distribution of a Larger Work)에 따라 앱 전체를
PolyForm Perimeter 로 배포하면서 해당 크레이트에 대해서만 MPL 의 고지·소스 제공 요구를
지킨다.

| 크레이트 | 버전 | 소스 |
|---|---|---|
| `cssparser` | 0.36.0 | https://crates.io/crates/cssparser/0.36.0 |
| `cssparser-macros` | 0.6.1 | https://crates.io/crates/cssparser-macros/0.6.1 |
| `dtoa-short` | 0.3.5 | https://crates.io/crates/dtoa-short/0.3.5 |
| `option-ext` | 0.2.0 | https://crates.io/crates/option-ext/0.2.0 |
| `selectors` | 0.36.1 | https://crates.io/crates/selectors/0.36.1 |

각 크레이트의 소스는 위 crates.io 주소에서 해당 버전 그대로 내려받을 수 있으며, MPL-2.0
전문은 https://mozilla.org/MPL/2.0/ 에 있다. 수정본을 배포하게 되면 그 시점에 수정된 파일의
소스를 같은 라이선스로 제공해야 한다.

버전 목록은 `src-tauri/Cargo.lock` 기준이다. 의존성을 갱신하면 이 표도 함께 갱신한다.

---

## 3. 그 밖의 의존성

Rust 570 개, npm 패키지의 라이선스를 전수 조회한 결과 GPL·AGPL 계열은 0 건이다. 다만 나머지가
고지 의무에서 자유롭다는 뜻은 아니다. MIT 는 "위 저작권 고지와 이 허가 고지를 소프트웨어의 모든
사본 또는 상당 부분에 포함할 것"을 요구하고, Apache-2.0 은 §4(a) 에서 라이선스 사본 동봉을,
§4(d) 에서 NOTICE 파일이 있으면 그 내용의 전달을 요구한다. 이 앱은 npm 의존성 코드를 번들에
인라인해 배포하므로 그 의무가 실제로 발생하며, 해당 고지는 아래 4 절에서 이행한다.

- `r-efi` — `MIT OR Apache-2.0 OR LGPL-2.1-or-later` → MIT 를 택한다.
- `ignore`·`globset` — `Unlicense OR MIT` → MIT 를 택한다.
- npm `dompurify` — `MPL-2.0 OR Apache-2.0` → Apache-2.0 을 택한다.

조사 근거와 판단 과정은 이 저장소의 아키텍처 결정 기록(ADR-0001)에 정리되어 있다.

---

## 4. npm 의존성 — MIT·Apache-2.0

`vite.config.ts` 에는 `rollupOptions.external` 설정이 없다. 그래서 Vite 는 프로덕션 npm
의존성의 코드를 `dist/assets/*.js` 에 인라인해 컴파일하고, 그 `dist/` 가
`src-tauri/tauri.conf.json` 의 `frontendDist` 로 앱에 들어간다. 아래 패키지의 코드는 배포물에
그대로 실려 나가므로 각 라이선스가 요구하는 고지를 이 절에서 이행한다.

`@types/pako`·`@types/raf`·`@types/trusted-types` 3 건은 타입 선언 전용 패키지라 런타임
코드가 번들에 포함되지 않으므로 아래 목록에서 제외한다.

### 4.1 MIT 를 적용하는 패키지

저작권 고지는 각 패키지에 동봉된 라이선스 파일(`LICENSE`·`LICENSE.md`·`LICENSE.txt`·
`LICENSE_MIT`·`LICENSE-MIT.txt`·`license.txt`·`LICENSE.spdx`)에서 그대로 옮긴 것이다.

| 패키지 | 버전 | 라이선스 | 저작권 고지 |
|---|---|---|---|
| `@babel/runtime` | 7.29.7 | MIT | Copyright (c) 2014-present Sebastian McKenzie and other contributors |
| `@tauri-apps/api` | 2.11.1 | `Apache-2.0 OR MIT` → MIT | Copyright (c) 2017 - Present Tauri Apps Contributors |
| `@tauri-apps/plugin-autostart` | 2.5.1 | `MIT OR Apache-2.0` → MIT | 2019-2022, The Tauri Programme in the Commons Conservancy |
| `@tauri-apps/plugin-dialog` | 2.7.2 | `MIT OR Apache-2.0` → MIT | 2019-2022, The Tauri Programme in the Commons Conservancy |
| `@tauri-apps/plugin-opener` | 2.5.4 | `MIT OR Apache-2.0` → MIT | 2019-2022, The Tauri Programme in the Commons Conservancy |
| `@xterm/addon-fit` | 0.10.0 | MIT | Copyright (c) 2019, The xterm.js authors (https://github.com/xtermjs/xterm.js) |
| `@xterm/addon-web-links` | 0.11.0 | MIT | Copyright (c) 2017, The xterm.js authors (https://github.com/xtermjs/xterm.js) |
| `@xterm/xterm` | 5.5.0 | MIT | Copyright (c) 2017-2019, The xterm.js authors (https://github.com/xtermjs/xterm.js)<br>Copyright (c) 2014-2016, SourceLair Private Company (https://www.sourcelair.com)<br>Copyright (c) 2012-2013, Christopher Jeffrey (https://github.com/chjj/) |
| `base64-arraybuffer` | 1.0.2 | MIT | Copyright (c) 2012 Niklas von Hertzen |
| `canvg` | 3.0.11 | MIT | Copyright (c) 2010 - present Gabe Lerner (gabelerner@gmail.com) - https://github.com/canvg/canvg |
| `core-js` | 3.49.0 | MIT | Copyright (c) 2013–2025 Denis Pushkarev (zloirock.ru)<br>Copyright (c) 2025–2026 CoreJS Company (core-js.io) |
| `css-line-break` | 2.1.0 | MIT | Copyright (c) 2017 Niklas von Hertzen |
| `fast-png` | 6.4.0 | MIT | Copyright (c) 2015 Michaël Zasso |
| `fflate` | 0.8.3 | MIT | Copyright (c) 2026 Arjun Barrett |
| `html2canvas` | 1.4.1 | MIT | Copyright (c) 2012 Niklas von Hertzen |
| `iobuffer` | 5.4.0 | MIT | Copyright (c) 2015 Michaël Zasso |
| `jspdf` | 4.2.1 | MIT | Copyright<br>(c) 2010-2025 James Hall, https://github.com/MrRio/jsPDF<br>(c) 2015-2025 yWorks GmbH, https://www.yworks.com/ |
| `marked` | 18.0.13 | MIT | Copyright (c) 2018+, MarkedJS (https://github.com/markedjs/)<br>Copyright (c) 2011-2018, Christopher Jeffrey (https://github.com/chjj/)<br>(Markdown 원 고지는 아래 참조) |
| `pako` | 2.2.0 | `MIT AND Zlib` | Copyright (C) 2014-2017 by Vitaly Puzrin and Andrei Tuputcyn (Zlib 부분은 4.2 참조) |
| `performance-now` | 2.1.0 | MIT | Copyright (c) 2013 Braveg1rl |
| `raf` | 3.4.1 | MIT | Copyright 2013 Chris Dickinson `<chris@neversaw.us>` |
| `regenerator-runtime` | 0.13.11 | MIT | Copyright (c) 2014-present, Facebook, Inc. |
| `rgbcolor` | 1.0.1 | `MIT OR SEE LICENSE IN FEEL-FREE.md` → MIT | Copyright (c) 2016 Stoyan Stefanov, http://phpied.com/ |
| `stackblur-canvas` | 2.7.0 | MIT | Copyright (c) 2010 Mario Klingemann |
| `svg-pathdata` | 6.0.3 | MIT | Copyright © 2017 Nicolas Froidure |
| `text-segmentation` | 1.0.3 | MIT | Copyright (c) 2021 Niklas von Hertzen |
| `utrie` | 1.0.2 | MIT | Copyright (c) 2021 Niklas von Hertzen |

수집 경로에 설명이 필요한 항목은 다음과 같다.

- `@tauri-apps/api` 는 `LICENSE_MIT` 와 `LICENSE_APACHE-2.0` 을 함께 배포한다. MIT 를 택하고
  `LICENSE_MIT` 의 저작권 줄을 실었다.
- `@tauri-apps/plugin-autostart`·`plugin-dialog`·`plugin-opener` 는 라이선스 본문 파일 없이
  `LICENSE.spdx` 만 동봉한다. 위 저작권 줄은 그 파일의 `PackageCopyrightText` 값이다.
- `rgbcolor` 의 `FEEL-FREE.md` 는 라이선스 조건이 아니라 저자의 자유 이용 안내문이므로,
  선택지 중 조건이 명확한 MIT 를 택하고 `LICENSE.md` 의 저작권 줄을 실었다.
- `marked` 의 `LICENSE` 는 MIT 고지("## Marked") 뒤에 John Gruber 의 원본 Markdown 고지
  ("## Markdown", BSD 형식)를 함께 싣는다. 이 고지는 바이너리 배포 시에도 재현을 요구하므로 아래
  MIT 허가 고지 다음에 원문 그대로 옮겼다.

위 패키지에 공통으로 적용되는 MIT 허가 고지 전문을 한 번만 싣는다. 각 패키지의 저작권 고지는
위 표의 해당 줄로 갈음한다.

```
Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
```

`marked` 의 `LICENSE` 에 동봉된 Markdown 고지 원문은 다음과 같다.

```
Copyright © 2004, John Gruber
http://daringfireball.net/
All rights reserved.

Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:

* Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
* Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
* Neither the name “Markdown” nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.

This software is provided by the copyright holders and contributors “as is” and any express or implied warranties, including, but not limited to, the implied warranties of merchantability and fitness for a particular purpose are disclaimed. In no event shall the copyright owner or contributors be liable for any direct, indirect, incidental, special, exemplary, or consequential damages (including, but not limited to, procurement of substitute goods or services; loss of use, data, or profits; or business interruption) however caused and on any theory of liability, whether in contract, strict liability, or tort (including negligence or otherwise) arising in any way out of the use of this software, even if advised of the possibility of such damage.
```

### 4.2 pako 의 Zlib 부분

`pako` 의 npm 라이선스 필드는 `MIT AND Zlib` 다. `AND` 는 선택형이 아니라 두 라이선스가 동시에
적용된다는 뜻이다. 패키지의 `README.md` 가 밝히듯 `/lib/zlib` 폴더만 Zlib 라이선스이고 나머지는
MIT 다. Zlib 고지 원문은 별도 라이선스 파일이 아니라 `node_modules/pako/lib/zlib/*.js` 각
파일의 머리말 주석으로 동봉되어 있으며, 그 내용은 다음과 같다.

```
(C) 1995-2013 Jean-loup Gailly and Mark Adler
(C) 2014-2017 Vitaly Puzrin and Andrey Tupitsin

This software is provided 'as-is', without any express or implied
warranty. In no event will the authors be held liable for any damages
arising from the use of this software.

Permission is granted to anyone to use this software for any purpose,
including commercial applications, and to alter it and redistribute it
freely, subject to the following restrictions:

1. The origin of this software must not be misrepresented; you must not
  claim that you wrote the original software. If you use this software
  in a product, an acknowledgment in the product documentation would be
  appreciated but is not required.
2. Altered source versions must be plainly marked as such, and must not be
  misrepresented as being the original software.
3. This notice may not be removed or altered from any source distribution.
```

### 4.3 dompurify — Apache-2.0

`dompurify` 3.4.14 는 `MPL-2.0 OR Apache-2.0` 이중 라이선스이며, 3 절이 선언한 대로
Apache-2.0 을 택한다.

이 패키지가 동봉한 `LICENSE` 파일은 저작권자 자리가 `Copyright [yyyy] [name of copyright
owner]` 로 비어 있는 Apache-2.0 템플릿이라 저작권자를 특정할 수 없다. 그래서 배포 산출물
`node_modules/dompurify/dist/purify.js` 첫 줄의 소스 배너를 저작권 근거로 삼는다. 즉 아래
문구의 출처는 라이선스 파일이 아니라 **소스 배너**다.

```
DOMPurify 3.4.14 | (c) Cure53 and other contributors | Released under the Apache license 2.0 and Mozilla Public License 2.0 | github.com/cure53/DOMPurify/blob/3.4.14/LICENSE
```

Apache-2.0 §4(a) 는 라이선스 사본을 함께 전달할 것을 요구한다. 전문은
https://www.apache.org/licenses/LICENSE-2.0 에 있으며, 패키지에 동봉된 사본은
`node_modules/dompurify/LICENSE` 에 있다. §4(d) 는 배포물에 `NOTICE` 파일이 있을 때 그 내용을
전달할 것을 요구하는데, `dompurify` 3.4.14 배포물에는 `NOTICE` 파일이 없으므로 이 항목에서
전달할 추가 고지는 없다. 위 소스 배너는 번들된 코드 안에 그대로 남아 있어 §4(b) 의 수정 고지
요건과도 충돌하지 않는다.

### 4.4 버전 기준

이 절의 버전 목록은 `package-lock.json` 에 실제 설치된 버전 기준이다(`package.json` 의 semver
범위가 아니다). 의존성을 갱신하면 이 절의 표와 저작권 고지도 함께 갱신한다.
