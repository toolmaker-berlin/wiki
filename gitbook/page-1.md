# Page 1

**Kleine schnipset‘s und Beispiele**&#x20;

_Kleine schnipset‘s und Beispiele für Standard Probleme in Python zu verschiedenen Themen._

### Ablaufsteuerung

#### Exit

_Irgendwann will man Python auch mal sauber beenden. Es gibt noch andere Möglichkeiten, aber die haben auch Ecken und Kanten._&#x20;

{% code title="testpy.py" overflow="wrap" lineNumbers="true" %}
```python
import sys
from exitstatus import ExitStatus # $pip install exitstatus 
print("Sauberes Programm-Ende!")
sys.exit(ExitStatus.success)

```
{% endcode %}

{% code lineNumbers="true" %}
```python
import sys, os
os._exit(status=0)
sys.exit(0)

```
{% endcode %}

#### Pool-Funktion&#x20;

```
from multiprocessing import Pool

def ggg(x):
    return x * x

with Pool(10) as p:
    print(p.map(ggg, [1, 2, 3] * 30))

print("ok")

```

#### Breakpoints&#x20;

```
x = 15
breakpoint(cond=x>17,context=7)
print(x)

```

### Systemfunktionen

#### Anzahl CPUs

```
import multiprocessing
print("Anzahl CPUs (ggf. mit Hyperthreading) : ", multiprocessing.cpu_count())


```

#### Datum und Uhrzeit

```
from datetime import datetime
print(f"Date/Time: {datetime.now():%d-%m-%Y %H:%M:%S%z}\n")

```

#### Speicherplatz

```
meminfo = dict((i.split()[0].rstrip(':'),int(i.split()[1])) for i in open('/proc/meminfo').readlines())
mem_kib = meminfo['MemTotal']  
print("RAM ",mem_kib)

import psutil # $pip install psutil (nicht iOS konform)
print(psutil.virtual_memory())

```

#### Python Version&#x20;

\#offen

```
import sys
text=sys.version.split(" ")
text="\nPython: "+text[0]
print(text)
print("-"*(len(text)-1))

```

#### Platform&#x20;

```
import platform
Systemname=platform.system()
print(Systemname)
```

#### Bildschirm CLR

_Es gibt viele Varianten …_

```
print("\033c", end="") # ok replit

from console.utils import cls
cls() # nicht überall implementiert 

# ziemlich universell 
try:
  import sys, subprocess, platform
  subprocess.Popen( "cls" if platform.system() == "Windows" else "clear", shell=True)
except:
  pass

import os 
os.system('clear')

```

### Beispiele&#x20;

#### Zeitmessung

_Hier ein Beispiel wie ich das in meinem Benchmark-Program mit einem Decorator_\
_gelöst habe:_

```
import time

ms_total = 0
ms_einzel = 0

# Zeitmessung mit decorator
def timeit(method):
  def timed(*args, **kw):
    ts = time.time()
    result = method(*args, **kw)
    te = time.time()
    global ms_total, ms_einzel
    ms_einzel = (te - ts) * 1000
    ms_total += ms_einzel
    return result
  return timed

# Floatingpointtest (Simple)
@timeit
def test1():
  x = 0
  for i in range(10_000_00):
    x += i / 1000

test1()
Print(ms_einzel)

```

```
A$=„4711“


```
