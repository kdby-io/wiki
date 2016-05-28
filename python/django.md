# Django

## Login
django.contrib.auth에 내장된 view와 form을 이용.
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

로그인을 성공하면 LOGIN_REDIRECT_URL로 redirect 하는데 기본값은 '../accounts/profile'다.  
setting.py 에서 `LOGIN_REDIRECT_URL = '/'`로 변경 가능.
