## 💻 `프로젝트 소개`
_다양한 짐을 보관할 수 있는 공간을 제공하고 이용하는 중개 사이트_
- 자신이 소유하고 있는 공간 내에서 보관할 수 없는 짐을 맡기고 싶은 사용자와, 남는 공간이 있지만 활용하지 못해 아쉬운 사용자가 모두 모여 공간을 제공하거나 이용할 수 있는 중개 플랫폼

##  ⌨️ `개발 기간`
* 2024.08.27 ~ 2024.10.11
* 2024.08.27 ~ 09.09 기획설계
* 2024.09.10 ~ 10.10 프로젝트 개발
* 2024.10.11 완료

## 🧑‍🤝‍🧑 `멤버구성`
 - 팀장 : 양혜연
 - 팀원 : 위성민
 - 팀원 : 김강현
 - 팀원 : 박하얀

## ⚙️ `개발 환경`
- FRAMEWORK : SPRING, REACT
- FRONTEND : Visual Studio Code
- BACKEND : IntelliJ IDEA, MYSQL, SMTP GMAIL
- LIBRARY : AWS S3, SMTP GMAIL, JPA HIBERNATE
- CONFIGURATION MANAGEMENT : GITHUB, DISCORD
  
## 📂 `패키지구조`
```
## 📂 `백엔드 구조`
C:.
+---java
|   \---com
|       \---quantum
|           \---holdup
|               |   HoldupProjectApplication.java
|               |
|               +---common
|               |       AuthConstants.java
|               |
|               +---config
|               |       AwsS3Config.java
|               |       JacksonConfig.java
|               |       JacksonCustomizerConfig.java
|               |       MailConfig.java
|               |       SwaggerConfig.java
|               |       WebConfig.java
|               |       WebSecurityConfig.java
|               |       WebSocketConfig.java
|               |
|               +---controller
|               |       AdminController.java
|               |       ChatController.java
|               |       ChatRoomController.java
|               |       EmailController.java
|               |       InquiryController.java
|               |       MemberController.java
|               |       ReportController.java
|               |       ReservationController.java
|               |       ReviewController.java
|               |       SpaceController.java
|               |
|               +---domain
|               |   +---dto
|               |   |   |   ChatMessageDTO.java
|               |   |   |   ChatRoomDTO.java
|               |   |   |   CreateInquiryDTO.java
|               |   |   |   CreateMemberDTO.java
|               |   |   |   CreateReportDTO.java
|               |   |   |   CreateReservationDTO.java
|               |   |   |   CreateReviewDTO.java
|               |   |   |   EmailRequestDTO.java
|               |   |   |   InquiryDetailDTO.java
|               |   |   |   InquiryDTO.java
|               |   |   |   LoginMemberDTO.java
|               |   |   |   MemberDTO.java
|               |   |   |   PasswordCheckRequestDTO.java
|               |   |   |   RechargeCreditsDTO.java
|               |   |   |   ReportCommentDTO.java
|               |   |   |   ReportDetailDTO.java
|               |   |   |   ReportDTO.java
|               |   |   |   ReservationListDTO.java
|               |   |   |   ReviewCommentDTO.java
|               |   |   |   ReviewDetailDTO.java
|               |   |   |   ReviewDTO.java
|               |   |   |   SearchMemberEmailDTO.java
|               |   |   |   UpdateInquiryDTO.java
|               |   |   |   UpdateMemberDTO.java
|               |   |   |   UpdateReportDTO.java
|               |   |   |   UpdateReviewDTO.java
|               |   |   |   VerificationDTO.java
|               |   |   |   VerificationRequestDTO.java
|               |   |   |
|               |   |   \---spaces
|               |   |           CreateSpaceDTO.java
|               |   |           SpaceDetailDTO.java
|               |   |           SpacePageDTO.java
|               |   |
|               |   \---entity
|               |           ChatRoom.java
|               |           Comment.java
|               |           Inquiry.java
|               |           InquiryImage.java
|               |           Member.java
|               |           Message.java
|               |           Report.java
|               |           ReportImage.java
|               |           Reservation.java
|               |           Review.java
|               |           ReviewImage.java
|               |           Role.java
|               |           Space.java
|               |           SpaceImage.java
|               |           VerificationCode.java
|               |
|               +---filter
|               |       CustomAuthenticationFilter.java
|               |       HeaderFilter.java
|               |       JwtAuthorizationFilter.java
|               |
|               +---handler
|               |       CustomAuthenticationProvider.java
|               |       CustomAuthFailUserHandler.java
|               |       CustomAuthSuccessHandler.java
|               |
|               +---message
|               |       ResponseMessage.java
|               |
|               +---Page
|               |       Pagination.java
|               |       PagingButtonInfo.java
|               |
|               +---repository
|               |       ChatRoomRepository.java
|               |       CommentRepository.java
|               |       InquiryImageRepository.java
|               |       InquiryRepository.java
|               |       MemberEmailRepository.java
|               |       MemberRepository.java
|               |       MessageRepository.java
|               |       ReportImageRepository.java
|               |       ReportRepository.java
|               |       ReservationRepository.java
|               |       ReviewImageRepository.java
|               |       ReviewRepository.java
|               |       SpaceImageRepository.java
|               |       SpaceRepository.java
|               |       VerificationCodeRepository.java
|               |
|               +---service
|               |       AdminMemberService.java
|               |       ChatRoomService.java
|               |       ChatService.java
|               |       CommentService.java
|               |       CustomUserDetails.java
|               |       CustomUserDetailService.java
|               |       EmailService.java
|               |       InquiryService.java
|               |       MemberService.java
|               |       ReportService.java
|               |       ReservationService.java
|               |       ReviewService.java
|               |       S3Service.java
|               |       SpaceService.java
|               |
|               \---util
|                       ConvertUtil.java
|                       TokenUtils.java
|
\---resources
    |   application.yml
    |
    \---mysql
            createDummy.sql
            holdupdb.sql

## 📂 `프론트 엔드`
C:.
|   App.js
|   index.css
|   index.js
|   Store.js
|
+---apis
|       AdministratorAPICall.js
|       Api.js
|       CommentAPICall.js
|       EmailVerificationAPICall.js
|       InquiryAPICall.js
|       MypageAPICall.js
|       ReportAPICall.js
|       ReservationAPICall.js
|       ReviewAPICall.js
|       SignupFormAPICall.js
|       SpaceAPICalls.js
|       UserAPICalls.js
|
+---components
|   +---commons
|   |       CommunitySidebar.js
|   |       Footer.js
|   |       Header.js
|   |       MyPageSidebar.js
|   |
|   \---forms
|           AddressPopup.js
|           AdministratorForm.js
|           CreateInquiryForm.js
|           CreateReportCommentForm.js
|           CreateReportForm.js
|           CreateReservationForm.js
|           CreateReviewCommentForm.js
|           CreateReviewForm.js
|           CreateSpaceForm.js
|           CreditPage.js
|           EmailDomainSelector.js
|           EmailVerification.js
|           FindEmailForm.js
|           InquiryDetailForm.js
|           InquiryForm.js
|           InquiryUpdateForm.js
|           LoginForm.js
|           MypageForm.js
|           MyReservationsForm.js
|           Pagination.js
|           ParentComponent.js
|           Ratingform.js
|           ReportCommentForm.js
|           ReportDetailForm.js
|           ReportForm.js
|           ReportUpdateForm.js
|           ReviewCommentForm.js
|           ReviewDetailForm.js
|           ReviewForm.js
|           ReviewUpdateForm.js
|           SignupForm.js
|           SignupFormUI.js
|           SpaceDetailForm.js
|           SpacePage.js
|           SuccessScreen.js
|           TermsPopup.js
|
+---css
|       AdministratorForm.module.css
|       CommunitySidebar.module.css
|       CreateInquiryForm.module.css
|       CreateReportComment.module.css
|       CreateReportForm.module.css
|       CreateReservation.module.css
|       CreateReviewCommentForm.module.css
|       CreateReviewForm.module.css
|       CreateSpaceForm.module.css
|       CreditPage.module.css
|       EmailDomainSelector.module.css
|       EmailVerification.module.css
|       FindEmailForm.module.css
|       Footer.module.css
|       Guideline.module.css
|       Header.module.css
|       InquiryDetailForm.module.css
|       InquiryForm.module.css
|       InquiryUpdateForm.module.css
|       Login.module.css
|       Main.module.css
|       MyPage.module.css
|       MyPageForm.module.css
|       MypageSidebar.module.css
|       MyReservation.module.css
|       ReportCommentForm.module.css
|       ReportDetailForm.module.css
|       ReportForm.module.css
|       ReportUpdateForm.module.css
|       ReviewCommentForm.module.css
|       ReviewDetail.module.css
|       ReviewForm.module.css
|       ReviewUpdateForm.module.css
|       Signup.module.css
|       SignupForm.module.css
|       SignupFormUI.module.css
|       SpaceDetail.module.css
|       SpacePage.module.css
|       SuccessScreen.module.css
|       TermsPopup.module.css
|
+---layouts
|       Layout.js
|
+---modules
|       index.js
|       InquiryCreateModule.js
|       InquiryDeleteModule.js
|       InquiryDetailModule.js
|       InquiryModule.js
|       MyReservationModule.js
|       ReportCommentCreateModule.js
|       ReportCommentModule.js
|       ReportCreateModule.js
|       ReportDetailModule.js
|       ReportModule.js
|       ReservationModule.js
|       ReviewCommentCreateModule.js
|       ReviewCommentModule.js
|       ReviewCreateModule.js
|       ReviewDeleteModule.js
|       ReviewDetailModule.js
|       ReviewModule.js
|       SpaceDetailModule.js
|       SpaceModule.js
|       SpacePageModule.js
|       UserModule.js
|
\---pages
        Administrator.js
        CreateInquiry.js
        CreateReport.js
        CreateReservation.js
        CreateReview.js
        CreateSpace.js
        CreateSpaceSuccessPage.js
        Guideline.js
        Inquiry.js
        InquiryDetail.js
        Login.js
        Main.js
        Mypage.js
        MyReservations.js
        Report.js
        ReportDetail.js
        Review.js
        ReviewDetail.js
        Signup.js
        SpaceDetail.js
        Spaces.js
        UpdateInquiry.js
        UpdateReport.js
        UpdateReview.js
```


## 📌 주요 기능
### 🚧 공간 관련
- 공간 생성 : 공간 등록 페이지에서 공간 정보를 입력하여 제공할 공간을 등록할 수 있다.
- 공간 사진 등록 : 공간 등록 시 사진을 첨부할 수 있다.
- 공간 예약 : 등록되어있는 공간에 예약을 접수하여 사용 신청을 할 수 있다.

###  🚥 회원관리
- 로그인 :
  비회원이 로그인에서 아이디 와 비밀번호를 입력했을때 DB 에 존재하는 아이디와 비밀번호이면 메인페이지로 이동
- 회원가입 :
  비회원은 이름 닉네임 이메일 전화번호 이메일 을 입력해야하며 빈칸이 있으면 빈칸에 오류문구가 출력되며 회원가입이 되지않음 이메일은 인증을 통해 실제로 사용된 이메일임을 인증
  중복된 아이디로 회원가입을 중복된 아이디로는 새로운 계정이 생성되지않고 경고 창으로 중복확인을 요구함
- 마이페이지 :
  로그인한 회원의 닉네임 이메일 전화번호를 확인할 수 있다. 회원정보는 자신의 현재비밀번호를 입력하여 수정할 수 있으며 크레딧을 충전할 수 있다.
- 관리자 페이지 :
  모든 회원을 조회할 수 있으며 , 사용자의 역할 , 닉네임 , 탈퇴 , 정지 여부를 설정할 수 있다.
  다른 일반 회원이 관리자페이지로 이동하는 버튼이나 이벤트를 넣지않고 URL 로 관리했습니다.

### 🖼️ 게시판 관련
- 게시글 조회 : 모든 게시글을 조회 할 수 있다
- 게시글 추가 : 글과 이미지를 추가 할 수 있다.
- 게시글 상세 조회 : 등록된 글과 이미지를 조회하여 볼 수 있다
- 게시글 수정 : 게시글 작성한 본인만 글의 내용을 수정 할 수 있다.
- 게시글 삭제 : 게시글 작성한 본인만 글을 삭제 할 수 있다.
- 댓글 추가 : 게시글 상세페이지에서 댓글을 추가 할 수 있다.
- 댓글 조회 : 상세페이지에 달린 댓글을 조회 할 수 있다.


## 🗣️ 후기
### 위성민
이번 프로젝트를 통해서 처음으로 스프링과 리액트를 연동시켜보았는데 처음에는 정말 막막한 과정이었지만, 연동에 성공하여 리액트에서 입력하여 보낸 값이 스프링을 통해 데이터베이스에 저장되고 데이터베이스에 저장된 값을 리액트에서 가져와서 사용하는 방식이 너무 재밌었습니다.
예약을 확인하고, 처리하고, 예약이 끝난 후의 유효성 검사를 통해 리뷰 작성으로 연동되는 기능 등을 구현하지 못해 아쉽고 앞으로의 개선방향이 될 것 같습니다. 이번엔 비록 처음으로 스프링과 리액트를 연동하는 경험이었기에 설계시 놓치는 부분이 많았다고 하지만 다음 프로젝트의 설계시엔 이번의 경험을 살려 두 설계시에 엔티티의 조인 구조, REST API의 URL 설계, 사용자 인증 방식 설계 등을 좀더 개선하고 이슈트래킹 과정에서 좀더 상세한 기술로 추후에 누가봐도 이해할 수 있도록 개선하고 싶습니다.

### 김강현
프로젝트 기간내에 전반적으로 좀 아쉬움이 없지않았습니다.
기획 단계에서 나름 완벽하게 하기 위해서 여러 회의를 통해 세부적으로 프로젝트
를 기획하였지만 부족한 DB 추가로 작성할 컬럼등이 좀 있었고 추가 기능을 만들면서
목표한 기능들에 대한 부족함이 있어서 다음에는 좀더 계획적인 설계를 통해
개발단계에서 방향성을 잡을 수 있도록 하고싶습니다.
가장 프로젝트 개발을 하면서 마일스톤과 같이 중간 목표가 없어서 막연하게 개발했었는데 이부분을 좀더
체계적으로 관리를해서 개발를 했으면 좋겠고 , 개발을 하면서 하드코딩 되거나 무분별하게 나열되어있는 파일을 
정리해서 보다 가독성이 좋게 개선하고싶습니다.

### 양혜연
기획할 때 나름 꼼꼼하게 한다고 열심히 했지만, 실제 기능 구현을 할때 짰던 계획과 좀 틀어졌었습니다. 기획에 포함되지 않은 내용도 있었고, 일부 기능 구현에 예상보다 많은 시간이 소요되어 완성하지 못한 부분도 있어 아쉬움이 남았습니다.
그러나 이번 프로젝트를 통해 s3같은 새로운 기능에 도전을 해 본것이 중요한 경험이 되어 다른 것들도 도전해보고 싶다는 생각이 들었습니다.
그리고, 이러한 경험을 통해 다음 프로젝트에서는 시간 관리를 더욱 효율적으로 하여 전반적인 완성도를 높일 수 있을 것 같다는 자신감을 얻었습니다.
앞으로의 프로젝트에서는 특히 게시판 기능을 더욱 발전시키고 싶고, 이번에 구현하지 못한 다양한 게시판 관련 기능들을 다음 기회에는 꼭 구현해 보고 싶은 욕심이 생겼습니다.

## 추가하고 싶은 기능
크레딧 충전 시 실제 결제 기능 도입
- 휴대폰 결제 api 등을 사용해서 결제 기능 도입
게시글 추가 시 실제 작성폼처럼 다양한 옵션 선택 기능 만들기
- 게시글 작성 UI 개선 혹은 라이브러리등을 사용
게시글 목록에서 조회수, 댓글수 등 더 많은 정보 보여주기
- 조회수 / 댓글수 등 이글의 선호도를 표시
관리자 기능 추가하여 전반적인 사이트 관리에 더 용이하게하기
- 게시글 조회 , 수정 , 삭제


## 개선하고 싶은 점
스프링과 리액트 연동시 데이터를 처리할때 
jwt 토큰을 세션스토리지에 저장하는데 이를 복호화 하거나 캐시에 저장해서 다른 사용자가 읽을 수 없도록 하고싶습니다.
사용자의 권한을 통한 url 접속을 관리하여 관리자로 로그인하지 않은 사용자 url에 접속을 차단
이슈트래킹을 보다 자주 자세히 어떻게 해결했는지 상술하기 
다른 유사이트처럼 보다 깔끔한 사용자 인터페이스 
