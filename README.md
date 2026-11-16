<div align="center">

# UWorld Image Date · 이미지 일자변경

**Photos downloaded from iCloud show today's date? Put every photo back on the day it was taken.**
**iCloud에서 내려받은 사진의 날짜가 모두 오늘로 바뀌었나요? 사진을 찍은 그날로 되돌려 드립니다.**

[![Latest release](https://img.shields.io/github/v/release/UWorld-Group/uworldimagedate?label=Windows%20%7C%20macOS&logo=github&color=0a7bbd)](https://github.com/UWorld-Group/uworldimagedate/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/UWorld-Group/uworldimagedate/total?label=downloads&color=2ea043)](https://github.com/UWorld-Group/uworldimagedate/releases)

| Windows | macOS (Apple silicon) | macOS (Intel) |
|:---:|:---:|:---:|
| [**Download**](https://github.com/UWorld-Group/uworldimagedate/releases/latest/download/UWorldImageDate-windows-x64-setup.exe) | [**DMG**](https://github.com/UWorld-Group/uworldimagedate/releases/latest/download/UWorldImageDate-macos-arm64.dmg) | [**DMG**](https://github.com/UWorld-Group/uworldimagedate/releases/latest/download/UWorldImageDate-macos-x64.dmg) |

<img src="https://service.uworld.co.kr/assets/shots/uworldimagedate/screen-01.jpg?v=3" alt="UWorld Image Date — before and after · 내려받은 직후와 복원 후" width="820">

</div>

---

## Why UWorld Image Date · 왜 이미지 일자변경인가

When you download photos from **iCloud** (iCloud.com, iCloud for Windows) or copy them off a Mac, the files are written to disk again — so their **created and modified dates become the day you downloaded them**. Ten years of photos suddenly all say "today", and every folder, gallery and backup tool sorts them in the wrong order.

The good news: the original date is usually still **inside the photo** — in the EXIF data the camera or phone wrote when the picture was taken. UWorld Image Date reads that hidden date and puts it back where it belongs: in the **file name** and in the file's **created and modified dates**. It never touches the picture itself.

**iCloud**(iCloud.com, Windows용 iCloud)에서 사진을 내려받거나 맥에서 복사해 오면 파일이 디스크에 새로 쓰이면서 **생성일과 수정일이 모두 내려받은 날짜로 바뀝니다.** 10년 치 사진이 전부 "오늘"로 찍혀 탐색기·사진 앱·백업 프로그램에서 순서가 뒤죽박죽이 됩니다.

다행히 원래 날짜는 대부분 **사진 안에** 남아 있습니다 — 카메라나 휴대폰이 찍을 때 적어 둔 EXIF 추가정보입니다. 이미지 일자변경은 그 숨은 날짜를 읽어 **파일 이름**과 파일의 **생성일·수정일**을 원래대로 되돌립니다. 사진 내용은 전혀 건드리지 않습니다.

## Features · 주요 기능

### 📅 Finds the real date · 진짜 촬영일 찾기
- Reads the **EXIF capture date** first, then **XMP** dates (Photoshop and editors), **video** creation dates (iPhone MOV, MP4), and finally dates written in the **file name** (screenshots, `IMG_20230101_123456`, KakaoTalk …).
  **EXIF 촬영일**을 먼저 보고, 없으면 **XMP**(포토샵 등 편집 프로그램), **동영상** 촬영일(아이폰 MOV·MP4), 마지막으로 **파일 이름**의 날짜(스크린샷, `IMG_20230101_123456`, 카카오톡 …)를 찾습니다.
- The last-edited date is ignored on purpose, so an edited photo keeps the day it was *taken*, not the day it was retouched.
  편집한 날짜는 일부러 쓰지 않습니다 — 보정한 사진도 *찍은* 날짜로 돌아갑니다.

### ✏️ Name and dates in one go · 이름과 날짜를 한 번에
- Adds the date in front of the name — `20231222_182245_IMG_1234.jpg` — so files sort by when they were taken, everywhere.
  이름 앞에 날짜를 붙여(`20231222_182245_IMG_1234.jpg`) 어디서 보든 찍은 순서대로 정렬됩니다.
- Sets the file's **created** and **modified** dates to the capture time. Files that already carry the prefix are not renamed twice.
  파일의 **생성일**과 **수정일**을 촬영 시각으로 바꿉니다. 이미 날짜가 붙은 파일은 다시 붙이지 않습니다.

### 🗂️ Whole folders, subfolders included · 하위 폴더까지 통째로
- Pick one folder and every subfolder and file inside is found. The folder you chose last time is remembered.
  폴더 하나만 고르면 하위 폴더의 모든 파일을 찾습니다. 지난번에 고른 폴더를 기억합니다.

### ⚡ Built for huge libraries · 수십 GB도 빠르게
- Reads and processes files **in parallel**, with a progress bar, speed and time remaining. Tested for libraries of tens of gigabytes.
  여러 파일을 **동시에** 처리하고 진행률·속도·남은 시간을 보여 줍니다. 수십 GB 사진 보관함을 염두에 두고 만들었습니다.

### 🛡️ Your originals stay safe · 원본은 안전하게
- Three ways to save: **copy to another folder** with the same subfolder layout, **one ZIP file**, or **change the originals in place**. The first two never modify the originals.
  결과는 세 가지 중에서 고릅니다 — 하위 폴더 구성 그대로 **다른 폴더로 복사**, **ZIP 파일 하나로**, **원본을 그 자리에서 변경**. 앞의 두 방식은 원본을 바꾸지 않습니다.
- Photos without any date are left exactly as they are. A CSV report lists what was changed and why.
  날짜를 찾지 못한 사진은 그대로 둡니다. 무엇을 어떤 근거로 바꿨는지 CSV 보고서로 남깁니다.

### 🍎 Made for files that came from a Mac · 맥에서 온 파일도 깔끔하게
- Korean file names from macOS (decomposed jamo) are shown correctly, Mac helper files (`._*`, `.DS_Store`, `.Trashes`) are skipped, and the Photos library package is never touched.
  맥에서 온 한글 파일 이름(자모가 풀린 이름)을 정상으로 합쳐 보여 주고, 맥의 부속 파일은 건너뛰며, 사진 앱 보관함 안은 절대 건드리지 않습니다.

---

## Install · 설치 안내

### Windows

**Requirements · 사양**: Windows 10 / 11 (64-bit).

1. Download **`UWorldImageDate-<version>-windows-x64-setup.exe`** from the [latest release](https://github.com/UWorld-Group/uworldimagedate/releases/latest).
   [최신 릴리스](https://github.com/UWorld-Group/uworldimagedate/releases/latest)에서 설치 파일을 내려받습니다.
2. Run it and follow the installer. The installer and the app are code-signed by **유월드 (UWorld)**. A desktop shortcut is created.
   실행하면 설치가 진행됩니다. 설치 파일과 프로그램 모두 "유월드" 이름으로 서명되어 있으며, 바탕화면에 아이콘이 생깁니다.
3. *(Optional)* Verify the file with `SHA256SUMS.txt` from the same release:
   *(선택)* 같은 릴리스의 `SHA256SUMS.txt` 로 파일이 변조되지 않았는지 확인할 수 있습니다.
   ```powershell
   Get-FileHash .\UWorldImageDate-<version>-windows-x64-setup.exe -Algorithm SHA256
   ```

### macOS (DMG)

**Requirements · 사양**: macOS 14 or later (15 or later recommended). Choose **arm64** for Apple silicon (M1–M4) or **x64** for Intel Macs.
macOS 14 이상(15 이상 권장). Apple 실리콘(M1~M4)은 **arm64**, 인텔 맥은 **x64** 를 받으세요.

1. Download **`UWorldImageDate-<version>-macos-arm64.dmg`** (or `-x64.dmg`) from the [latest release](https://github.com/UWorld-Group/uworldimagedate/releases/latest) and open it.
   최신 릴리스에서 DMG를 내려받아 엽니다.
2. Drag **이미지 일자변경** onto **Applications**. The app is signed with UWorld's Developer ID and **notarized by Apple**.
   **이미지 일자변경**을 응용 프로그램 폴더로 끌어다 놓습니다. 유월드 Developer ID 서명과 Apple 공증을 받은 앱입니다.
3. The first time you pick a folder in Documents or on an external drive, macOS asks for permission — choose **Allow**.
   문서 폴더나 외장 드라이브를 처음 고르면 macOS가 접근을 묻습니다 — **허용**을 누르세요.

---

## About this repository · 이 저장소에 대해

This repository is used **only to distribute installers**. The source code is not published here.
The "Source code" archives that GitHub attaches to every release contain only this README and the license.

이 저장소는 **설치 파일 배포 전용**입니다. 앱 소스코드는 공개하지 않으며, 릴리스마다 GitHub가 자동으로 붙이는 "Source code" 압축 파일에는 이 안내문과 사용권 안내만 들어 있습니다.

## Support · 문의

- Website · 웹사이트: https://service.uworld.co.kr

<div align="center">

Part of **[UWorld Group](https://github.com/UWorld-Group)** · See [LICENSE.txt](LICENSE.txt) · © UWorld. All rights reserved.

</div>
