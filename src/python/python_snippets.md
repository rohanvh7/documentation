
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