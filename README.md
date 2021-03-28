# kiwitcms-post-pytest-results-to-kiwi-
Code for the YouTube video: https://youtu.be/zhz0AuaDGuY

## Install pytest using apt
```
sudo apt install -y python3-pytest
```
- (Optional add alias for pytest)
```
vim ~/.bash_aliases
```
- add:
```
alias pytest=pytest-3
```
## The simple test used
- Make a new file with prefix test_ 
  - for example ```test_123.py```
  - add the following
  ```
  import pytest

  def test_method():
    assert "a" == "a"

  def test_failed_method():
    assert "a" == "b"

  ```
## Running the simple test

- now run the test: ```pytest --junit-xml ./report.xml```

## Post to kiwi
- Install the plugin
```pip install kiwitcms-junit.xml-plugin --user```

- Now to post the report run ```tcms-junit.xml-plugin ./report.xml```



References:
- Junit XML plugin https://github.com/kiwitcms/junit.xml-plugin
- Post TAP to Kiwi: https://youtu.be/d7kK5wuBeZU
- Install Kiwi on Ubuntu: https://youtu.be/S7h4OG7aeFA
