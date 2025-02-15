# 트러블슈팅
- 2025.01.13 로그인을 하자마자 로그인이 해제되는 문제
  - (해결) 2025.01.17<br>Next.js next/link의 Link 다음 리소스를 빠르게 불러오기 위해 해당 리소스를 미리 로드하는 prefetch 속성이 존재한다.<br>근데 로그아웃 버튼에 Link 태그와 함께 백엔드의 로그아웃 api를 바로 호출하도록 코드를 작성하였었고, prefetching 기능으로 인해 로그아웃이 계속 처리되고 있었던 것.<br>Link prefetch={false} 설정을 통해 해결

- CI/CD 테스트
