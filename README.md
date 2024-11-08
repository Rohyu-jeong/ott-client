# 클라이언트 🖥️

## 개발 개요 📜
- OTT 플랫폼(Netflix)을 새롭게 개발한 OTT 플랫폼 서비스입니다.

## 기술 스택 🔧
| 항목             | 내용                                         |
|------------------|--------------------------------------------|
| **디자인**       | Figma, Clip Studio                         |
| **개발 환경**    | VSCode                                      |
| **프로그래밍 언어** | HTML, CSS, TypeScript                      |
| **프레임워크/라이브러리** | React, TailwindCSS, SWR, Axios, React Router DOM |
| **버전 관리**    | Git, GitHub                                  |
| **커뮤니케이션** | Notion, KakaoTalk                           |
| **배포** | AZURE                           |

![logo](/public/devlogo.png)


## 팀원 🧑‍🤝‍🧑
- **Developer**: 김병찬, 김민서
- **Project Manager**: 김민서
- **Data Collector, QA**: 홍석환

### 업무 및 포지션

#### 👦🏻 김민서 (**Developer** , **Project Manager**)
- 홈/메인/프로필 페이지 개발
- REST API 설계 및 구현
- UI/UX 디자인 및 구현
- 프로젝트 가이드라인 수립
- 코딩 표준 정의
- 프로젝트 기획 구축

#### 🧒🏻 김병찬 (**Developer**)
- 로그인 페이지 개발
- 데이터 유효성 및 무결성 처리
- 회원가입 처리
- UI/UX 구현

#### 👨🏻‍🦱 홍석환 (**Data Collector, QA**)
- UI/UX 테스트
- 성능 테스트
- 버그 리포트 및 기록
- 데이터 수집


## 개발 기간 및 기획 📝

### 개발 기간 
#### 2024년 6월
- **디자인**: 6/29 ~ 6/30

#### 2024년 7월
- **가이드라인 구축**: 7/1 ~ 7/3
- **UI , 정적 페이지**: 7/3 ~ 7/14
- **REST API**: 7/14 ~ 7/21
- **UX 구현**: 7/21 ~ 7/29
- **빌드 및 배포**: 7/29 ~ 7/31

#### 2024년 8월
- **유지보수**: 7/31 ~ 8/3
- **문서화 및 피드백**: 8/3 ~ 8/6


### 기획
- **페이지**: 홈, 로그인, 메인, 프로필, 에러
- **디렉토리 구조**:
  - `public/`: 정적 파일을 보관하는 폴더
    - `image/`: 이미지 파일을 보관하는 폴더
  - `src/`: 소스 코드를 관리하는 폴더
    - `components/`: 각 구조의 컴포넌트를 관리하는 폴더
    - `pages/`: 각 페이지를 관리하는 폴더
    - `services/`: REST API 함수를 관리하는 폴더
    - `events/`: 모든 이벤트 핸들러를 관리하는 폴더
    - `styles/`: 사용자 정의의 유틸리티 스타일 속성을 관리하는 폴더
    - `types/`: 모든 타입 정의를 관리하는 폴더
    - `utils/`: 모든 유틸리티 함수 및 에러 처리, 데이터 무결성+유효성 등을 관리하는 폴더
    - `data/`: 클라이언트 측 정적 데이터 및 시드 데이터를 정의하고 관리하는 폴더
  
![files](/public/files.png)

- **코딩 표준**:
  - `atom`: 재사용 가능한 리프 노드를 정의합니다.
  - `molecule`: 리프 노드의 집합을 정의합니다.
  - `cluster`: 리프 노드의 집합인 `molecule` 집합을 정의하며 페이지 컴포넌트의 하위 노드로 정의됩니다.

## 페이지 📃
- **홈 (Home)**: 웹 서비스의 초기 화면이며 마케팅성 광고과 홍보 콘텐츠를 보여줍니다.
- **로그인 (Login)**: 로그인 서비스 및 회원가입 시스템을 제공합니다.
- **메인 (Main)**: 계정 서비스를 통해 OTT 플랫폼의 콘텐츠를 제공합니다.
- **프로필 (Profile)**: 계정 서비스 통해 OTT 플랫폼의 계정 관련 서비스를 제공합니다.
- **에러 (Error)**: 클라이언트 측 에러 발생 시 지원되는 안내 페이지입니다.

## 테스트 케이스 ⚙️
### 홈
| 테스트 케이스 ID  | 제목                         | 목표                                                   | 전제 조건                                    | 실제 결과                                                  | 상태         | 처리                                      |
|------------------|------------------------------|---------------------------------------------------------|---------------------------------------------|------------------------------------------------------------|--------------|-------------------------------------------|
| H-TC01           | -       | - | -  | -     | -      | -                                     |

### 로그인
| 테스트 케이스 ID  | 제목                         | 목표                                                   | 전제 조건                                    | 실제 결과                                                  | 상태         | 처리                                      |
|------------------|------------------------------|---------------------------------------------------------|---------------------------------------------|------------------------------------------------------------|--------------|-------------------------------------------|
| L-TC01           | 로그인창에서 이메일 및 비밀번호 유효성 검사       | 이메일과 비밀번호 형식 맞지 않으면 문구가 뜨는지 확인 | 이메일 형식 및 비밀번호 형식 제한  | 형식이 맞지 않으면 문구가 뜨며 로그인 안됨     | 성공       | -                                     |
| L-TC02           | 로그인창에서 이메일 정보 저장       | 로그인창에서 로그인 정보 저장 아이콘 클릭 시 이메일 정보 저장 | 정보 저장 아이콘을 클릭 후 로그인하면 로컬스토리지에 저장 되는 조건  | 정보 저장 아이콘을 클릭 후 로그인 할 경우 이메일 정보 저장됨. 
반대로 아이콘 클릭 하지 않으면 정보 저장 안되는 것 확인     | 성공       | -                                     |
| L-TC03           | 가입하기 1단계 유효성 검사        | 이메일 형식, 비밀번호 형식, 비밀번호 일치 여부, 필수사항 체크 여부 유효성 검사 후 문제 없으면 다음 단계로 넘어감 | 이메일 형식, 비밀번호 형식, 비밀번호 일치 여부, 필수사항 체크 여부 유효성 검사  | 이 중 하나라도 형식에 어긋나면 다음 단계로 이동 안되는 것 확인. 4가지 모두 문제 없다면 다음 단계로 넘어가는 것 확인 
반대로 아이콘 클릭 하지 않으면 정보 저장 안되는 것 확인     | 성공       | -                                     |
| L-TC04           | 개인정보 처리방침 모달 띄우기        | 개인정보 처리방침(필수사항) 클릭하면 모달 띄워짐 | 개인정보 처리방침 텍스트 클릭  | 클릭하면 모달 정상적으로 띄워지는 것 확인     | 성공       | -                                     |
| L-TC05           | 멤버쉽 모달 데이터 맨 마지막 데이터로 통일되는 현상        | 멤버쉽 data와 모달이 일치되도록 수정 | -  | 모달과 data 불일치     | 실패       | -                                     |
| L-TC06           | 좌,우 아이콘 클릭하여 멤버쉽 선택        | 아이콘 클릭하면 멤버쉽 데이터 좌 우로 이동함 | -  | 클릭하면 좌 우로 데이터 이동하는것 확인     | 성공       | -                                     |
| L-TC07           | 자세히 알아보 클릭시 모달 띄우기        | 클릭을 하면 해당 모달 뜨도록 수정 | -  | 모달은 뜨지만 멤버쉽 data와 불일치     | 실패       | -                                     |
| L-TC08           | 카드번호, 유효기간, 이름, 카드 비밀번호 유효성검사       | 각각 유효성 검사 후 형식에 맞지 않으면 문구가 뜨는지 확인 | 각각 유효성 검사 및 형식 제한  | 형식에 어긋나면 문구가 뜨는 것 확인     | 실패       | -                                     |
| L-TC09           | 이용약관 동의 가입 제한       | 이용약관 동의해야 가입이 되도록 제한 | 체크되지 않으면 에러창 띄움  | 체크되지 않으면 에러창 띄워졌고 체크하면 문제 x     | 성공       | -                                     |
| L-TC09           | 은행 선택       | 은행을 선택해야 다음단계로 진행하는지 확인   | 은행 선택하지 않으면 에러창 띄움  | 은행 선택해야만 다음 단계로 넘어가는 것 확인     | 성공       | -                                     |

### 메인
| 테스트 케이스 ID  | 제목                         | 목표                                                   | 전제 조건                                    | 실제 결과                                                  | 상태         | 처리                                      |
|------------------|------------------------------|---------------------------------------------------------|---------------------------------------------|------------------------------------------------------------|--------------|-------------------------------------------|
| M-TC01           | 티저 모달의 찜 기능 확인       | 찜 버튼을 클릭하였을 때 버튼의 이벤트가 정상 동작하는지 확인 | 로그인 상태이며 티저 모달이 렌더링 되어야 한다.  | 찜한 후 티저 모달을 다시 이동하여도 찜 상태가 유지되지 않음     | 실패       | 미처리                                     |
| M-TC02           | 티저 모달의 UI 버튼 확인       | 티저 모달의 UI 숨김 처리 버튼이 정상 작동하는지 확인 | 로그인 상태이며 티저 모달의 UI가 렌더링 되어야 한다.  | 숨김, 보임 처리가 정상 작동한다.    | 성공       | 버튼이 텍스트 요소로 정의되어 버튼 요소로 직관적으로 보일 수 있도록 변경    
| M-TC03           | 카테고리에서 로고 클릭하여 메인으로 이동       | 카테고리에서 로고를 클릭하여 메인으로 이동할 수 있는지 확인 | 카테고리와 메인이 존재하고 클릭 이벤트가 있어야 한다.  | 카테고리가 동적 렌더링을 통한 처리로 클릭 시 카테고리가 유지된다.     | 실패       | 카테고리를 닫고 열 수 있는 상태 값을 정의하여 각 클릭 이벤트에 전달하여 처리함   |

### 프로필
| 테스트 케이스 ID  | 제목                         | 목표                                                   | 전제 조건                                    | 실제 결과                                                  | 상태         | 처리                                      |
|------------------|------------------------------|---------------------------------------------------------|---------------------------------------------|------------------------------------------------------------|--------------|-------------------------------------------|
| P-TC01           | 멤버 전환 모달 버튼 확인       | 멤버 전환 모달에서 2개의 버튼이 정상 작동하는 지 확인 | 로그인 유저의 멤버 데이터가 존재해 멤버 리스트가 렌더링 되어야한다.  | 모달의 뒤로가기 버튼이 클릭되지 않음     | 실패       | 해당 버튼요소에 이벤트 핸들러가 정의되지 않아 새롭게 정의하여 처리함 |
| P-TC02           | 멤버 프로필 수의 제한       | 각 멤버쉽에 따른 멤버 프로필 수를 제한하는 기능을 확인 | 로그인 상태로 멤버쉽 등급을 가져야하고 멤버를 생성할 수 있어야 한다.  | 멤버 제한이 없어 무한대로 생성된다.     | 실패       | 로그인 유저의 멤버쉽 등급을 확인하고 각 멤버쉽에 따른 현재 멤버 프로필 수를 조건문으로 제한하여 생성 불가 모달로 처리함   |
| P-TC03           | 멤버 프로필 전환 상태에서 멤버 삭제       | 멤버 프로필 전환 상태에서 멤버 접근 권한을 부여하지 않음을 확인 | 멤버 프로필로 전환된 상태와 멤버 삭제 기능이 존재해야한다.  | 멤버 프로필 전환 상태에서 다른 멤버에 접근 권한 제한이 없어 모든 계정을 삭제 할 수 있다.     | 실패       | 메인 계정 상태에서만 접근 권한을 부여하고 멤버 프로필 전환 상태에서 멤버 접근 시 제한 모달을 구현함    |
| P-TC04           | 프로필의 시청기록 관리       | 시청기록의 기록 순서와 삭제 기능의 정상 작동  | 시청한 콘텐츠의 데이터가 존재해야 하며 로그인 상태 이여야 한다.  | 시청기록의 기록순서의 뒤섞임 현상 발생      | 실패       | 미처리    |



## 참고 자료 및 출처 📡
- **디자인**: 
  - YouTube: [https://www.youtube.com](https://www.youtube.com)
  - Netflix: [https://www.netflix.com/kr/](https://www.netflix.com/kr/)
- **UI/UX**: 
  - Netflix: [https://www.netflix.com/kr/](https://www.netflix.com/kr/)
- **데이터**: 
  - YouTube: [https://www.youtube.com](https://www.youtube.com)
  - Netflix: [https://www.netflix.com/kr/](https://www.netflix.com/kr/)
  - 나무위키: [https://namu.wiki](https://namu.wiki)
  - Pinterest: [https://kr.pinterest.com/](https://kr.pinterest.com/)
