# Regex

## Sample code
```python
import re
template = r'0x004b value: (\w{2}) (\w{2}) ([0-z]{2})'
regex = re.compile(template)
for line in lines[30:33]:
    matched = regex.search(line) 
    x = matched.group(1)
    y = matched.group(2)
    z = matched.group(3)
    # x = int(x,16)
    # y = int(y,16)
    z0 = int(z[0],16)
    z1 = int(z[1],16)
    print(line,x,y,z0, z1,z)

```
## Output
```
Notification handle = 0x004b value: 41 0c 4a 41 0c 4 10 4a 
Notification handle = 0x004b value: 39 0c 44 39 0c 4 4 44 
Notification handle = 0x004b value: 37 0c 37 37 0c 3 7 37
```

## Other regex
- ISO8601 datetime format
`(\d{4})-(\d{2})-(\d{2})T(\w{2}):(\d{2}):(\d{2})Z`

## Resources
- Regex testing https://regexr.com/
- Py Regex http://pythonstudy.xyz/python/article/401-%EC%A0%95%EA%B7%9C-%ED%91%9C%ED%98%84%EC%8B%9D-Regex