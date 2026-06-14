## 리눅스 및 맥OS 환경 설치 가이드 (Installation on Linux/MacOS)

- 와인(Wine)을 이용해 윈도우용 설치 파일(`.exe`)을 실행하는 방식으로 설치할 수 있습니다.
- 또는 다음과 같이 수동 설치를 진행할 수도 있습니다:
  1. [최신 릴리즈 페이지](https://github.com/BGforgeNet/Fallout2_Restoration_Project/releases/latest)에서 `rpu_v*.zip` 파일을 다운로드합니다.
  2. 만약 게임이 대소문자를 구분하는(case-sensitive) 파일 시스템에 있는 경우, 게임 디렉토리 및 파일명을 모두 소문자로 변환해 줍니다.
  3. 다운로드한 압축 파일의 내용을 게임 메인 디렉토리에 풀고, 덮어쓸 것인지 묻는 메시지가 나오면 모두 덮어씁니다.
  4. 리눅스 환경에서는 `rpu-install.sh`를, 맥OS 환경에서는 `rpu-install.command`를 실행합니다.

### 중요 유의사항
게임을 실행할 때 반드시 다음과 같이 DLL 재정의(override) 옵션을 설정해야 합니다: `WINEDLLOVERRIDES='ddraw.dll=n,b' wine fallout2.exe` (또는 `winecfg`에서 직접 구성해 주세요). 이 설정을 누락할 경우 게임은 실행될 수 있으나 복원 프로젝트(RPU)의 기능들이 정상적으로 적용되지 않습니다.
