# mybBlog
1.简介
语言：python3、HTML、CSS、JavaScript
web框架：django2.0
前端框架：bootstrap、jQuery、HIGHCHARTS
数据库：MySQL
2.如何使用
1、一键安装库
项目文件夹都有一个requirments.txt文件。该文件是记录所使用库的信息。可利用该文件直接一键安装所有库。
启动虚拟环境之后（若有使用虚拟环境的的话），进入requirments.txt所在的目录，执行命令：
pip install -r requirements.txt
2、将项目克隆到本地
git clone git@github.com:xuxu12345/mybBlog.git
3、然后进入项目目录
cd SimplePersonalBlog
4、修改/mysite/settings文件中的DATABASE参数
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql', # 可以修改成其它数据库
        'NAME': 'mysite', # 数据库名称
        'USER': 'xuxu', # 用户名
        'PASSWORD': 'xuxu123456', # 密码
        'HOST': 'localhost', # host地址，本地数据库不用改，远程数据库的话改成数据库的IP地址
        'PORT': 3306, # 端口，一般不用改
    		}
}
5、初始化数据库
python manage.py migrate
6、再新建个管理员用户
python manage.py createsuperuser
然后依次输入用户名（可跳过，默认admin）、邮箱地址（可跳过）、密码即可。 
7、来创建缓存表
python manage.py createcachetable 
8、最后启动本地服务器
python manage.py runserver
9、在浏览器输入地址localhost:8000即可访问博客，输入地址localhost:8000/admin即可进入后台。
10、admin后台用户名是xuxu，密码是xuxu123456。
