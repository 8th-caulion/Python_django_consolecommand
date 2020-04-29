# LIKELION_8TH 1ST CONSOLE COMMAND

## APP만들기까지

1. 폴더를 하나 생성한다.
```bash
$ mkdir <폴더명>
```

2. 폴더로 이동한다. -> 왜냐면 이 폴더안에서 작업을 해야되니까!
```bash
$ cd <폴더명>
```

3. 가상환경설정
```bash
$ python -m venv <가상환경이름(보통은 myvenv로 사용!)>
``` 

4. 가상환경을 켜준다
  - Windows
```bash
$ source <가상환경이름>/Scripts/activate
```
  - Mac
```bash
$ source <가상환경이름>/bin/activate
```

5. 장고를 설치한다.
```bash
$ pip install django
```

6. 프로젝트를 생성한다.
```bash
$ django-admin startproject <프로젝트 명>
``` 

7. 프로젝트로 이동한다.
```bash
$ cd <프로젝트 명>
```

8. 앱을 생성한다. 
```bash
$ python manage.py startapp <앱 명>
```


## 장고서버켜기
- 이때 주의할 점은 manage.py가 있는 폴더에서 실행이 되야된다는거!!!
```bash
$ python manage.py runserver
```

## 알면 편리한 그리고 알아야되는 명령어들과 단축키
- 상위폴더로 이동
```bash
$ cd ..
```
- 하위 디렉토리 출력
```bash
$ ls
```

- 단축키(제가 자주쓰는 것들이라 안쓰셔도 되요!!)
    - Ctrl + K + F : 줄정리
    - Ctrl + K + C : 전체주석
    - Ctrl + K + U : 주석해제
    - Ctrl + `     : 터미널켜기
    - Ctrl + C : 터미널에서 서버끄기 및... 흠... 무언가를 실행할때 종료

