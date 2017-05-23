# Board_for_design

### MVP 구조와 인터페이스를 통해 만드는 게시판
### 인터페이스를 통한 설계의 좋은 예
### MVP 구조와 활용 이해의 좋은 예 
- M : 게시판에 필요한 속성값(데이터)와 이 값들을 영구 저장소에 저장하고(write) 불러오는(read) 일까지 처리
- V : 모든 화면에 관련 사항은 이곳에 정의한다. System.out.println의 모든 메소드는 이 곳에 정의한다.
- P : 프로그램을 실행시킬 때 필요한 메소드 정의, 모델의 값들을 처리하고 뷰에 넘겨주거나 뷰에서 입력된 값을 처리해서 저장하는 모든 일은 이곳에서 담당한다. start, end, 세부 사항, 입력, 삭제, 목록 보기에 관한 메소드를 이곳에 정의한다.
###
- 1.목록 : M->P->V
- 2.새글 : V->P->M
- 3.상세보기 : V->P->M->P->V
- 4.삭제 : V->P->M
- 5.종료 : V->P

### 영구 저장소 이용과 불러오기 이해의 좋은 예
- 1.부분 저장(객체 하나하나를 파라미터로 전달)
- 2.전체 저장(임시 저장소(컬렉션)에 저장 후 배열 전체를 파라미터로 전달)
- 3.전체 읽어오기(전체 객체를 읽어온 후 임시 저장소로 로딩해주기)
- 4.부분 읽어오기(개체 하나하나 읽어오기)
