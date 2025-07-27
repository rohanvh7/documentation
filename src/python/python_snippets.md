
```python
#Github : twitter/communitynotes 

from contextlib import contextmanager

@contextmanager
def time_block(label):
  start = time.time()
  try:
    yield
  finally:
    end = time.time()
    logger.info(f"{label} elapsed time: {end - start:.2f} secs ({((end - start) / 60.0):.2f} mins)")    
```

```python
# Infinite Loop with iter:  
#https://stackoverflow.com/questions/34253996/are-infinite-for-loops-possible-in-python
for _ in iter(int, 1):
    pass

from itertools import count

for i in count(0):
    pass
```

```python
TIL: Exception.add_note
# https://daniel.feldroy.com/posts/til-2025-05-exception-add_note

try:
    1/0
except ZeroDivisionError as e:
    e.add_note("This is a note about the error")
    e.add_note("This is another note")
    e.add_note("All notes must be strings")
    raise
```
