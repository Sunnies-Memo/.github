# 📝 **칸반 보드 애플리케이션 README**

---

## 📚 **프로젝트 개요**

**칸반 보드 애플리케이션**은 **React**, **TypeScript**, **Spring Boot**, 그리고 **NestJS**를 기반으로 한 프로젝트입니다. 이 애플리케이션은 작업을 시각적으로 관리할 수 있는 직관적인 인터페이스를 제공하며, 사용자는 보드 및 작업을 생성, 수정, 삭제, 드래그 앤 드롭으로 재배치할 수 있습니다.

---

## 🚀 **기술 스택**

### **Frontend**  
- **React 18.3.1**  
- **TypeScript**  
- **Recoil** (상태 관리)  
- **TanStack React Query** (서버 상태 관리)  
- **Styled-Components** (스타일링)  
- **React Beautiful DnD** (드래그 앤 드롭)  
- **React Hook Form** (폼 관리)  
- **Framer Motion** (애니메이션)  

### **Backend (Spring Boot)**  
- **Java 17**  
- **Spring Boot 3.3.3**  
- **Spring Security**  
- **JPA**  
- **JWT**  
- **AWS SDK**  

### **Backend (NestJS)**  
- **NestJS**  
- **TypeORM**  
- **Passport JWT**  
- **Multer**  
- **AWS S3**  
- **class-validator**  

### **Infrastructure**  
- **EC2 (Ubuntu 24.04 LTS)**  
- **MySQL**  
- **AWS S3**  
- **CloudFront**  
- **Nginx Reverse Proxy**  

---

## 🌟 **주요 기능**

### **공통 기능**  
- JWT 기반 인증 (로그인/회원가입/로그아웃/토큰 갱신)  
- 보드 및 카드 관리 (CRUD)  
- 드래그 앤 드롭 기능으로 작업 재배치  
- 이미지 업로드 (AWS S3)  

### **Frontend 기능**  
- 사용자 프로필 관리 (이미지 업로드, 비밀번호 변경)  
- 드래그 앤 드롭 기반의 작업 이동 및 보드 재배치  
- 반응형 UI 디자인  
- 유지보수 모드 지원  

### **Backend 기능 (Spring Boot / NestJS)**  
- 사용자 인증 및 권한 관리  
- 보드 및 카드 CRUD API 제공  
- JWT 기반 보안 처리  
- S3를 통한 이미지 업로드 및 관리  

---

## 🛠️ **상태 관리 전략**

### **React Query**  
- 데이터 캐싱 및 낙관적 업데이트  
- 자동 재시도 및 에러 핸들링  
- **StaleTime**: 15분 설정  

### **Recoil**  
- **userState**: 사용자 정보 상태  
- **orderedBoardList**: 보드 순서 상태  
- **boardAtomFamily**: 개별 보드 상태  
- **cardListSelector**: 카드 목록 상태  

---

## 🔄 **드래그 앤 드롭 구현**

- **React Beautiful DnD**를 사용하여 드래그 앤 드롭 기능 구현  
- 보드 간 카드 이동  
- 보드 순서 변경  
- 드롭 영역을 통한 카드 삭제  

---

## 🔒 **보안**

### **Frontend**  
- 비밀번호 정책: 최소 7자, 문자/숫자/특수문자 포함  
- 토큰 자동 갱신 및 인증 상태 유지  

### **Backend**  
- 비밀번호 암호화 (BCrypt)  
- JWT Access Token (15분) / Refresh Token (7일)  
- API 요청 시 JWT 인증 필수  

---

## 🗂️ **프로젝트 구조**

### **Frontend**
```
src/
├── pages/
│   ├── Login.tsx
│   ├── Join.tsx
│   ├── Todos.tsx
│   ├── MyPage.tsx
│   ├── Maintenance.tsx
├── components/
│   ├── Board.tsx
│   ├── DraggableCard.tsx
│   ├── BoardForm.tsx
│   ├── ImageDropzone.tsx
│   ├── Navigation.tsx
│   ├── TrashBin.tsx
├── recoil/
└── hooks/
```

### **Backend (Spring Boot)**
```
src/main/java/
├── auth/
│   ├── controller/
│   ├── dto/
│   ├── entity/
│   ├── repository/
│   ├── service/
├── boards/
├── user/
├── config/
└── global/
```

### **Backend (NestJS)**
```
src/
├── auth/
│   ├── dto/
│   ├── entities/
│   ├── service/
├── boards/
├── user/
├── s3/
└── global/
```

---

## 📊 **배포 아키텍처**

### **Spring Boot Backend**
- **EC2 (Ubuntu 24.04 LTS)**: Spring Boot 및 MySQL 배포
- **S3**: 정적 파일 및 이미지 파일 저장
- **CloudFront**: 정적 콘텐츠 캐싱
- **Nginx**: 리버스 프록시 설정

### **NestJS Backend**
- **EC2 (Ubuntu 24.04 LTS)**: NestJS 및 MySQL 배포
- **S3**: 정적 파일 및 이미지 파일 저장
- **CloudFront**: 정적 콘텐츠 캐싱
- **Nginx**: 리버스 프록시 설정

---

## 📎 **링크**

- [배포 링크](https://d362dj0rdk52ph.cloudfront.net/)  
- [GitHub 리포지토리](https://github.com/orgs/Sunnies-Memo/repositories)  

---
