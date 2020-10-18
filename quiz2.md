```python
import sys

pres_map = {}

# mapper output: president valence
for line in sys.stdin:
    line = line.strip()
    pres, val = line.split("\t", 1)
    if pres not in pres_map:
        pres_map[pres] = int(val)
    else:
        pres_map[pres] += int(val)

for pres, val in pres_map.items():
    print(pres + "\t" + str(val))
```
