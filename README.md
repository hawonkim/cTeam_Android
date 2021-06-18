# cTeam : Android
### 작업 방침

- 저희는 소수의 액티비티와 다수의 프래그먼트를 이용해 작업할 예정이오니, 프래그먼트에다가 쓴다는 가정하에 만들면 좋습니다.





## 하지 말아야 할 것들

### 1.설정 파일 건드리기

- 설정 파일은 어플리케이션 자체에 큰 영향을 주기 때문에 저도 무슨 일이 일어날지 알 수 없습니다. 가급적 건드리지 말도록 하고, 필요한 경우 저에게 물어봐주세요.

### 2.한글 경로 사용

- 안드로이드 스튜디오가 하지말랍니다.

### 3.master 브랜치에 작업하기

- 만약 push까지 해버린 상태라면 저장소를 지우고 다시 만들어야 합니다.

### 4.변수 등 이름 겹치기

- 브랜치 병합 과정(Pull Request)에서 가장 위험한 것 중 하나입니다. 절대 겹치면 안됩니다 절대.

### 5.비어있는 커밋 메시지

- 실제 현장에서 협업하는데 커밋 메시지가 비어있으면 진짜로 욕먹습니다. 되게 귀찮은 짓이지만 꼭 해주도록 합시다. 형식은 아래의 링크를 참고해주세요

[https://blog.weirdx.io/post/33832](https://blog.weirdx.io/post/33832) 이 링크의 예시는 영어니까 한글로 따라하면 됩니다.

---

## Naming Rule

> 아래의 룰을 지키지 않으면 브랜치 병합 과정이 힘들어집니다.

> 정말 간단한거지만, 대부분의 문제는 간단한 것에서 비롯됩니다.

---

### 변수, ID명

> 말 그대로 변수와, 레이아웃에 들어가는 ID 이름

이 둘은 카멜 케이스라는 규칙이 적용됩니다. 카멜케이스란, 'camelCase' 이와 같이 소문자로 시작해서 단어가 바뀔때 앞부분만 대문자로 작성하는 규칙을 말합니다.

변수와 ID의 이름은 역할에 초점을 둔 '명사'로 짓습니다.

- 예) loginBtn, registerBtn

---

### 메서드명

변수와 똑같이 카멜 케이스 룰이 적용됩니다. 단, 역할에 초점을 둔 '동사'로 짓습니다.

- 예) doClose(), getConnection()

---

### 클래스명

클래스 명은 파스칼 케이스가 적용됩니다. 파스칼 케이스는 단어가 바뀔때마다 대문자를 사용하는 방식입니다. 'PascalCase' 이렇게요.

클래스 이름은 여러가지 국룰이 있기 때문에 그에 맞춰서 지을 예정입니다.

- 예) ArticleController, UserService

---

### 패키지명

패키지명은 전부 소문자를 이용합니다.

패키지 이름 역시 국룰이 있기 때문에 그에 맞춰서 지을 예정입니다. 그런데 문제가 하나 있습니다. 깃은 어떠한 패키지 안에 아무런 파일도 존재하지 않으면 해당 패키지는 저장소에 올리지 않습니다. 그렇기 때문에 패키지를 만들 일이 생기면 안에다가 test.txt 파일이라도 하나 넣어줍시다.

- 예) .controller, .service, .mapper

---

### 파일 이름

> 사진 파일 등 drawble에 집어넣는 것들

기본적으로 안드로이드 개발은 '사진'을 위한 폴더를 따로 만들지 않습니다. drawble 폴더 하나를 사용하는 것이 원칙입니다. 그러니 drawble 폴더에 다른 폴더를 만드는 일은 하지 말도록 합시다. 그렇다면 어떻게 해야하는가. 간단합니다. 그냥 이름만 다르게 해서 넣어두세요.

> user_login_btn_naver.PNG

위와같은 것을 스네이크 케이스라고 합니다. 중간 중간 단어가 바뀌는 부분은  _ 언더바로 구분해주는 방식으로, 데이터베이스나 파일 이름, final 상수 이외에는 잘 쓰이지 않습니다. 어찌되었던 파일 이름에는 snake_case를 적용합니다.

파일 이름은 '사용할 유저_기능_타입_기타.PNG' 의 형식으로 작성해주시면 됩니다. 현재 res 폴더에는 drawble, layout, mipmap, values 밖에 없지만 더 세세하게 분류할 계획입니다. 분류 기준은

[https://developer.android.com/guide/topics/resources/providing-resources](https://developer.android.com/guide/topics/resources/providing-resources)

위 링크를 참고해주세요.

---

### 레이아웃, 기타

레이아웃 파일은 스네이크 케이스(snake_case)를 적용합니다. 

여러번 파일을 만들어봤던 것처럼 MainActivity의 xml 레이아웃은 activity_main와 같은 이름으로 지어주도록 합시다.
