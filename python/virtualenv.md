
# Virtualenvwrapper

## Virtualenvwrapper 설치
    $ pip3 install virtualenv virtualenvwrapper

`~/.profile` 혹은 `~/.bashrc`에 아래 코드를 추가해준다.
```
export VIRTUALENVWRAPPER_PYTHON=/usr/bin/python3.5
export WORK_ON_HOME=$HOME/.virtualenvs
export PROJECT_HOME=$HOME/Dropbox/code
source /usr/local/bin/virtualenvwrapper.sh
```
`$ source ~/.bashrc`로 리로드.

## virtualenv 생성
    $ mkvitualenv <env_name>

## virtualenv 진입
    $ workon <env_name>

## 프로젝트와 함께 virtualenv 생성
    $ mkproject <prj_name>
가상환경을 만들고 PROJECT_HOME에 프로젝트 폴더를 생성하면서 바인딩한다.


## Autoenv
디렉토리를 옮겨갈 때마다 `.env` 파일을 찾고 내용을 실행시켜준다.

    $ git clone git://github.com/kennethreitz/autoenv.git ~/.autoenv
    $ echo 'source ~/.autoenv/activate.sh' >> ~/.bashrc
    $ source ~/.bashrc

프로젝트 폴더에 `.env`를 만들고 `workon <ENV_NAME>` 삽입.
