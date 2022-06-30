
# Matplotlib
plt.show() displays a plot; plt.clf() cleans it up again so you can start afresh.

### import
```
import matplotlib.pyplot as plt
from matplotlib import pyplot as plt
```

### line chart
```
plt.plot(arr,arr)
```

### scatter plot
```
plt.scatter(arr,arr)
```

### histogram
```
plt.hist(arr,bins=int)
```

### Reduce Scale
```
plt.scatter(x,y)
plt.xscale('log')
```

### axis labels
```
plt.xlabel('')
plt.ylabel('')
plt.title('')
```

### ticks
```
plt.yticks([0,2,4,6,8,10],['0B','2B','4B','6B','8B','10B'])
```
