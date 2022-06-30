
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
plt.scatter(gdp_cap, life_exp, s = np_pop, c = [])
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


### customizations
```
plt.scatter(x = gdp_cap, y = life_exp, s = np.array(pop) * 2, c = col, alpha = 0.8)

# Previous customizations
plt.xscale('log') 
plt.xlabel('GDP per Capita [in USD]')
plt.ylabel('Life Expectancy [in years]')
plt.title('World Development in 2007')
plt.xticks([1000,10000,100000], ['1k','10k','100k'])

# Additional customizations
plt.text(1550, 71, 'India')
plt.text(5700, 80, 'China')

# Add grid() call
plt.grid(True)
```
