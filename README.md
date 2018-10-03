# Nodejs-Firebase_Example_Project
Nodejs + Firebase Example Project


# Firebase 환경 설정
1. Firebase Console에서 Project 생성
2. 프로젝트 설정으로 이동, 서비스 계정 탭 클릭
3. 서비스 계정 생성 후 '새 비공개 키 생성' 및 파일 다운로드
4. 다운로드 파일을 Nodejs 프로젝트에 넣기

# Nodejs 서버
1. 클라이언트용 'firebase' package install. / 서버용 'firebase-admin' package install.
2. 'firebase' 패키지 초기설정
  - 다운로드된 파일 연결 및 실시간 데이터베이스 연결

# Firebase-db
1. 실시간 데이터베이스 예시 구조
```
{
  "public_resource" : {
    "TestNode" : {
      "Test1" : {
        "NickName" : "4525",
        "writeDate" : "2018-09-30 01:00:22"
      },
      "Test2" : {
        "NickName" : "4525",
        "writeDate" : "2018-09-30 00:00:00"
      },
      "Test3" : {
        "NickName" : 4325
      },
      "Test4" : {
        "NickName" : 4255
      },
      "Test5" : {
        "NickName" : 4857
      }
    }
  }
}
```
2. Restful
  - get Method
    - localhost:3000/ : Test1 NickName을 출력
    - localhost:3000/save : save query 값을 저장 및 update [세부사항 코드확인할 것.]
       - ex) `http://localhost:3000/save?save=4525`

3. Firebase Method
  - set : 하위 노드 덮어쓰기
  - update : 하위 노드 추가
  - on : 이벤트 연결
    - child_add : ref 하위 노드 추가
    - child_change : ref 하위 노드 수정
    - child_remove : ref 하위 노두 삭제
  - once : 1회성 이벤트 연결
 
 
## REF : Firebase Doc - chapter. 관리자
시작하기 : <https://firebase.google.com/docs/database/admin/start?hl=ko>
데이터 구조화 : <https://firebase.google.com/docs/database/admin/structure-data?hl=ko>
데이터 저장 : <https://firebase.google.com/docs/database/admin/save-data?hl=ko>
데이터 검색 : <https://firebase.google.com/docs/database/admin/retrieve-data?hl=ko>
