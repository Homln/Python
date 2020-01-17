### Adding libraries
```
pip install pylint autopep8
pip install jupyter
```

### Solve problems

```
Если не стал хаходим на сайт https://www.lfd.uci.edu/~gohlke/pythonlibs/#pywinpty
 находим билиатеку на которой заткнулись pywinpty. Находим 
Collecting pywinpty>=0.5; os_name == "nt"
  Using cached https://files.pythonhosted.org/packages/5d/97/8e43c2152a638cdb83d45644eb125c752abe67249f94bb3e3e29b0709685/pywinpty-0.5.7.tar.gz
    ERROR: Command errored out with exit status 1:



https://stackoverflow.com/questions/58422817/jupyter-notebook-with-python-3-8-notimplementederror

C:\Users\Администратор\AppData\Local\Programs\Python\Python38-32\Lib\site-packages\tornado\platform\asyncio.py
Добавить 

import sys
if sys.platform == 'win32':
    asyncio.set_event_loop_policy(asyncio.WindowsSelectorEventLoopPolicy())
```

