# [9001]_selenium chromedriver 콘솔창 제거

## 01_해당 파일

site-packages\selenium\webdriver\common\service.py 에서

## 02_ 해당 코드를 추가해준다.
```
self.process = subprocess.Popen(cmd, env=self.env,
  close_fds=platform.system() != 'Windows',
  stdout=self.log_file,
  stderr=self.log_file,
  stdin=PIPE,
  creationflags=0x08000000
)
```


