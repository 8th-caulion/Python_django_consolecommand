# LIKELION_8TH 4TH 과제를 위한 추가 개념정리!!

## 만약 COMMENT기능을 넣고 싶다면???!!
Django에서 관계를 표현하는 모델 필드에 대해서 알아야 합니다!!

 - 어떤 필드가 있을까??
    - ForeginKey
    - OneToOneField
    - ManyToManyField

#### ForeginKey
- 1:N 관계를 의미합니다!! 예를들어서 댓글과 게시글과의 관계처럼요! 한 게시글에 여러댓글들이 달리겠죠? 하나의 게시글에 여러개의 댓글이 달리는 것과 같은 관계를 ForeginKey라고 합니다!!

- 사용법  
```
class comment(models.Model):
    post = models.ForeignKey(Class명, on_delete=models.CASCADE)
```
두개의 인자를 받습니다!! 하나는 어떠한 Model class를 받을 것인지!! 다른 인자는 삭제시 어떤 옵션을 줄것인지 이렇게 두개를 받습니다!! 저 예시에는 CASCADE를 썼기 때문에 게시글이 삭제될 경우 관련된 모든 comment들을 다 삭제하게 됩니다!!! 즉 N쪽의 데이터들을 다 지우라는 말이에요!!
    
#### OneToOneField
- 1:1 관계를 말합니다!! 보통은 User Model 커스튬을 해서 profile Model을 연결할 때!! 사용해요!!

- 사용법  
```
class profile(models.Model):
    user = models.OneToOneField(Class명, on_delete=models.CASCADE)
```

#### ManyToManyField
- N:N 관계입니다!!! 다대다 관계에요!! 보통은 인스타그램처럼 게시글, tag을 달 때 이 관계로 사용이 됩니다!! 한 게시글에 태그가 여러개 달리고 태그를 눌렀을 경우 연관된 게시글들이 보이는 것처럼요!!
