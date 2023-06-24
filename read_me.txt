<분석 코드> 폴더 안에 있는 코드들은 분석을 위해 사용한 코드들입니다.

- <modeling> 폴더 안에 있는 코드는 KoBERT, KLUE BERT, Multilingual_BERT 모델을 사용한 fine-tuning 과정이 담긴 코드들입니다.

- <data> 폴더에는 사용한 데이터들이 들어있습니다.

- 데이터_전처리.ipynb는 데이터들을 통합하여 하나의 데이터셋으로 전처리하는 과정에 대한 코드입니다.

- EDA.ipynb는 통합된 데이터셋에 대한 탐색적 데이터 분석 코드입니다.

- 텍스트_마이닝_클러스터링.ipynb는 데이터셋들을 통합하여 감정별로 새로운 문서를 만들어 해당 문서들간의 K-평균 군집분석을 진행한 코드입니다.






<웹 서비스 코드> 폴더 안에 있는 파일은 웹 서비스 구현을 위한 프로젝트 코드입니다.

-[Project : emotion_diary]에 대한 설명입니다.


Apps :
1. analysis : 누적된 감정일기 분석 기능
	1) stat_model : 머신러닝 시킨 모델, 분석에 필요한 함수, 시각화함수 파일 모아놓은 디렉터리
		① charts.py : 하루 일기 시각화 함수 모듈
		② model_state_dict_final.pt : 머신러닝 시킨 모델
		③ MyBert.py : 사용된 Kobert 모델 형태로 데이터 변환시키는 함수 모듈
		④ predict_func.py : 예측함수 정의 및 데이터 전처리, 데이터프레임 생성 모듈
		⑤ weekly_charts.py : 누적 일기 시각화 함수 모듈
		⑥ weekly_result.py : 누적 일기 데이터 전처리 및 변환 모듈
		⑦ wordcloud_chart.py : 워드클라우드 생성 모듈

	2) static : 시각화 이미지, 컨텐츠 추천 등에 사용되는 이미지 모아놓은 디렉터리
		① images : 시각화 이미지, 컨텐츠 추천 등에 사용되는 이미지 모아놓은 디렉터리
	3) templates : html 파일들 모아놓은 디렉터리 
		① stacked_result.html : 주간 일기 분석 페이지

2. common : 회원가입, 로그인 등 사용자 계정 관리
	1) templates : html 파일들 모아놓은 디렉터리 
		① common_base.html : 로그인, 회원가입 페이지 기본 틀
		② form_erros.html : 발생가능한 에러 정의 및 메세지 제공 정의 페이지
		③ login.html : 로그인 페이지
		④ signup.html : 회원가입 페이지

3. diary : 일기 작성 및 수정, 삭제, 일기 목록, 하루 일기 분석 기능
	1) contents : 컨텐츠 추천에 사용된 함수들 모아놓은 디렉터리
		① book.py : 컨텐츠 추천 - 도서 이미지 저장 및 리스트 추출 모듈
		② book_recommend.py : 도서 추천 모듈
		③ movie.py : 컨텐츠 추천 - 영화 이미지 저장 및 리스트 추출 모듈
		④ movie_recommend.py : 영화 추천 모듈
		⑤ music_recommend.py : 음악 추천 모듈
	2) media : 사용자가 head_image에 올린 사진 저장하는 디렉터리
	3) static : 음악, 이미지, 부트스트랩, CSS 파일 등 저장해놓은 디렉터리		
		① bgm : BGM 오디오 파일 저장 디렉터리
		② diary(bootstrat, css, images) : 부트스트랩, css, 로고 이미지 저장해놓은 디렉터리
		③ emoticon : 이모티콘 이미지 저장 디렉터리
	4) templates : html 파일들 모아놓은 디렉터리 
		① base.html : html 기본 틀
		② confirmation.html : 일기 작성 후 확인 페이지
		③ diary_delete.html : 일기 삭제 페이지
		④ diary_detail : 오늘의 일기 분석 페이지
		⑤ diary_form.html : 일기 작성 페이지
		⑥ diary_list : 일기 목록 페이지
		⑦ footer.html : Footer 페이지
		⑧ mainavbar.html : 메인 화면 네비게이션 바 html
		⑨ navbar.html : 네비게이션 바 html

4. emotion_diary : config 역할

5. single_pages : 메인 홈 화면, 자기소개 페이지 관리 기능
	1) static : 사용중인 부트스트랩, css 파일 등 저장해놓은 디렉터리
	2) templates : html 파일들 모아놓은 디렉터리  
		① about_me.html : 자기소개 페이지
		② form_errors.html : 발생가능한 에러 정의 및 메세지 제공 정의 페이지
		③ info.html : 자기소개 수정 페이지
		④ landing.html : 메인 홈 페이지


# 앱 별 공통으로 사용되는 파일 정의
	1) forms.py : 장고에서 제공하는 form 정의 파일
	2) models.py : DB에 사용되는 모델 정의 파일
	3) urls.py : 각 페이지 별 사용되는 url 정의 파일
	4) views.py : 각 페이지 별 사용되는 함수 정의 파일


+) 그 외
- images : 사용자가 about me 에 올린 사진 저장 디렉터리	
- static : 사용중인 부트스트랩, css 파일 등 저장해놓은 디렉터리
- NanumBarunGothic.ttf : 사용된 글꼴
- stop_w.txt : 불용어 제거 시 사용된 단어 목록