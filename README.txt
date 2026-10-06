대신삼 PWA 배포 파일

구성
- index.html : 기존 v21 + PWA 설치 기능
- manifest.webmanifest : 앱 이름/아이콘/실행 방식
- sw.js : 오프라인 캐시 및 앱 실행 지원
- icons/ : 앱 아이콘

Vercel/GitHub에 올릴 때
1. ZIP을 풀어 네 저장소의 배포 루트에 파일 구조 그대로 올립니다.
2. 기존 HTML이 있다면 index.html로 교체합니다.
3. manifest.webmanifest, sw.js, icons 폴더도 반드시 같이 올립니다.
4. Vercel 배포 후 HTTPS 주소를 Android Chrome으로 엽니다.
5. 설정 > 앱 설치에서 '대신삼 앱 설치' 버튼이 나타나면 누릅니다.
   브라우저 환경에 따라 Chrome 메뉴의 '앱 설치' 또는 '홈 화면에 추가'로도 설치할 수 있습니다.

중요
- content://downloads/... 로 직접 연 HTML에서는 PWA 설치/Service Worker가 동작하지 않습니다.
- localhost 또는 HTTPS 배포 주소에서 동작합니다.
- 현재 버전은 '설치 가능한 앱 + 오프라인 실행 기반'까지 적용했습니다.
- 앱이 완전히 종료된 상태에서도 예약 시각에 상태바 알림을 보내는 Web Push 서버 기능은 아직 포함하지 않았습니다.
