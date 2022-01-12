# Github gist calendar

##### 2022-01-08 Sat #####
YYYY:   ██████▍░░░░░░░░░░░░░░ 00.0%
MM:     ██████▍░░░░░░░░░░░░░░ 00.0%
DD:     ██████▍░░░░░░░░░░░░░░ 00.0%
LIFE:   ██████▍░░░░░░░░░░░░░░ 00.0%


https://twitter.com/year_progress
http://progressbarserver.appspot.com/
https://apps.apple.com/us/app/progress-bar/id1441939775

https://twitter.com/countdown2038
https://twitter.com/decade_progress
https://hugovk.github.io/year-progress-bar/
https://www.redgregory.com/notion/2021/1/13/notion-formula-track-progress-for-the-year-month-and-day
https://play.google.com/store/apps/details?id=com.olmur.collection.widget.year&hl=en_US&gl=US
https://changaco.oy.lc/unicode-progress-bars/

## Gist related content
- `../.github/workflows/schedule.yaml` [link](https://github.com/jhojin7/productive-box/blob/master/.github/workflows/schedule.yml)
- turning gist into blogs https://gist.io/
- github gist docs update a gist https://docs.github.com/en/rest/reference/gists#update-a-gist
- py, jp, https://gist.github.com/ytez/cc65072ef6852740d24fc42882fb2806
- https://github.com/softvar/simplegist


## Misc
🌞 Morning     3 commits  █▌░░░░░░░░░░░░░░░░░░░   7.7%
🌆 Daytime    12 commits  ██████▍░░░░░░░░░░░░░░  30.8%
🌃 Evening    12 commits  ██████▍░░░░░░░░░░░░░░  30.8%
🌙 Night      12 commits  ██████▍░░░░░░░░░░░░░░  30.8%

🌏: Seoul, KR
📅: 2022-01-08 Sat
⏰: 23:59

import math
syms = '░▏▎▍▌▋▊▉█';
percent = 30.8
size = 21
#print(len(syms), percent)
frac = math.floor((size*8*percent)/100)
fullBar = math.floor(frac/8)
smallBar = frac % 8
#print(frac, fullBar, smallBar)
output = []
i=0
for i in range(size):
    if i < fullBar:
        output.append(syms[8])
    if i == fullBar:
        output.append(syms[smallBar])
    if i > fullBar:
        output.append(syms[0])
print(''.join(map(str,output)),percent,'%')