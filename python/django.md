# Django

## Login
django.contrib.auth에 내장된 view를 쓰려면
```python
# urls.py
from django.contrib.auth import views as auth_views

urlpatterns = [
	url(r'^login/$', auth_views.login, {
			'template_name': 'login.html',	# login()에 넘길 파라미터
		}, name='login'),
	url(r'^logout/$', auth_views.logout, {
			'next_page': 'login',	# logout()에 넘길 파라미터
		}, name='logout'),
]
```

view는 직접 만들고, django.contrib.auth에서 form만 쓰려면
```py
# views.py
from django.contrib.auth.forms import AuthenticationForm

form = AuthenticationForm(data=request.POST)
```
AuthenticationForm의 첫번째 파라미터는 request다. 그래서 그냥 AuthenticationForm(request.POST)라서 하면 form.is_valid()가 False가 된다.

로그인을 성공하면 LOGIN_REDIRECT_URL로 redirect 하는데 기본값은 '../accounts/profile'다.  
setting.py 에서 `LOGIN_REDIRECT_URL = '/'`로 변경 가능.

마찬가지로 login_required인 view에 접근시 로그인되어 있지 않으면 'LOGIN_URL'로 redirect된다. 기본값은 '../accounts/login'.

## Form에서 파일 받기
request된 데이터가 있을경우 Form에 request.POST와 함께 request.FILES로 파라미터로 넘겨준다.
```py
# views.py
form = Form(request.POST, request.FILES)
```
그리고 템플릿에서 `<form>`에 아래와 같이 `enctype="multipart/form-data"`를 넣는다.
```html
<form enctype="multipart/form-data" ...>
```

## Form에 내용 불러오기
```py
form = Form(instance=something)
```
