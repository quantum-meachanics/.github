## 💻 `프로젝트 소개`
_다양한 짐을 보관할 수 있는 공간을 제공하고 이용하는 중개 사이트_
- 자신이 소유하고 있는 공간 내에서 보관할 수 없는 짐을 맡기고 싶은 사용자와, 남는 공간이 있지만 활용하지 못해 아쉬운 사용자가 모두 모여 공간을 제공하거나 이용할 수 있는 중개 플랫폼

##  ⌨️ `개발 기간`
* 2024.08.27 ~ 2024.10.11

## 🧑‍🤝‍🧑 `멤버구성`
 - 팀장 : 양혜연
 - 팀원 : 위성민
 - 팀원 : 김강현
 - 팀원 : 박하얀

## ⚙️ `개발 환경`
- FRAMEWORK : SPRING, REACT
- FRONTEND : Visual Studio Code
- BACKEND : IntelliJ IDEA, MYSQL, SMTP GMAIL
- LIBRARY : AWS S3, SMTP GAMIL, JPA HIBERNATE
- CONFIGURATION MANAGEMENT : GITHUB, DISCORD
  
## 📂 `패키지구조`
```
백엔드
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

프론트엔드
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


## 🗣️ 후기

- 위성민 : 이번 프로젝트를 통해서 처음으로 스프링과 리액트를 연동시켜보았는데 처음에는 정말 막막한 과정이었지만, 연동에 성공하여 리액트에서 입력하여 보낸 값이 스프링을 통해 데이터베이스에 저장되고 데이터베이스에 저장된 값을 리액트에서 가져와서 사용하는 방식이 너무 재밌었습니다.
          예약을 확인하고, 처리하고, 예약이 끝난 후의 유효성 검사를 통해 리뷰 작성으로 연동되는 기능 등을 구현하지 못해 아쉽고 앞으로의 개선방향이 될 것 같습니다.
