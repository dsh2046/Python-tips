# Python-tips

## 1. datetime, timezone
tz = pytz.timezone('America/Toronto')
dt = datetime.datetime(2019, 6, 1, 12, 0, 0)

local = tz.localize(dt.replace(tzinfo=None), is_dst=None)
non_local = dt.replace(tzinfo=tz)
print(local)
print(non_local)

#### Use ```tz.localize(dt.replace(tzinfo=None), is_dst=None)``` instead of ```dt.replace(tzinfo=tz)```
