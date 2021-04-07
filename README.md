### 1. restful api 정리(UPL,Methods,Message)
- REST(Representaional State Transfer)란?
- 서버나 서비스에 존재하는 모든 자원(이미지,동영상,DB자원)에 고유한 URI를 부여해 활용하는것 =
- 자원을 정의하고 자원에 대한 주소를 지정하는 방법론을 의미한다.

- 자원(Resource): http://service.com/users라는 형태의 URI
- 헹위(Method): GET/POST/DELETE/PUT과 같은 메소드
- 표현(Message): JSON, XML등의 형태를 이용해 표현 

### 2.python flask 프레임워크 설치와 app.py 파일 코딩 설명
- pip install flask flask-restful mysql-connector-python flask 코드 다운받는법
- 코드 예시
- from flask import Flask
- app = Flask(__name__)

- # get localhost:포트번호/

- @app.route('/', methods = ['GET'])
- def hello_world():
-    return 'Hello World'
    

- if __name__=="__main__":
-    app.run()

### 3. python flask 에서, API 개발을 위해 Resource 클래스 개발하는 코드
- class RecipeListResource(Resource) :
-    # get 메소드로 연결시킬 함수  작성.
-    def get(self) :
-        # recipe 테이블에 저장되어 있는 모든 레시피 정보를 가져오는 함수
