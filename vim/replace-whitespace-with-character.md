# Replace whitespaces with visible character

Helpful when identation errors for incosistent tabs and spaces keep popping up in python or any other usecase. 


`:set listchars=eol:$,tab:>·,trail:~,extends:>,precedes:<,space:*`
`:set list`

Code sample:

```python
try:$
****with*open(FILE,*'r')*as*openfile:$
********try:$
************beacons*=*json.load(openfile)$
********except:$
************with*open(FILE,*'w')*as*outfile:$
****************outfile.write(json.dumps(beacons,*indent*=*4))$
except*FileNotFoundError:$
****with*open(FILE,*'w')*as*outfile:$
********outfile.write(json.dumps(beacons,*indent*=*4))$
```
