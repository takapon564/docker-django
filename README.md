# docker-django

## 概要  
  * webとDB用のコンテナを使って開発を行うための方法です。


## 作業用のディレクトリを作成する。  
* `$ mkdir app`  
`$ cd mkdir`  
* `$ git clone https://github.com/takapon564/docker-django.git`  
* `$ docker-compose run web  django-admin.py startproject examplepj .f`
> これでコンテナビルドが完了しました。。  
カレントディレクトリを確認し、プロジェクトが作成されていることを確認してください。  
## DBの接続情報を追記する。
* `$ vim examplepj/settings.py`  
* DATABASEの設定を書き換える。  
```
 DATABASES = {
 77     'default': {
 78         'ENGINE': 'django.db.backends.postgresql',
 79         'NAME': 'postgres',
 80         'USER': 'postgres',
 81         'HOST': 'db',
 82         'PORT': '5432',
 83     }
 84 }
```

