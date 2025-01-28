# Command Script
Use `!` or `%` to use any terminal command-line
`%` are called magic commands
Auto magic don't need the `!` or `%`
```
!pip install <library>
!apt-get install <library>
%cat
%ls
%mkdir
```

# Accessing Files
```python
from google.colab import drive
drive.mount('/content/drive')
```

```python
from google.colab import files
upload = files.upload()
```