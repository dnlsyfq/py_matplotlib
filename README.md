
# pylot interface
```
import matplotlib.pyplot as plt
fig, ax = plt.subplots()

ax.plot(x,y)
ax.plot(a,b, marker='o',linestyle='--',color='r') // linestyle='None'
ax.set_xlabel('')
ax.set_ylabel('')
ax.set_title('')
plt.show()
```

# Matplotlib
```
plt.show() //displays a plot;
plt.clf() //cleans it up again so you can start afresh.
plt.plot() // Line chart , shows continuous change, often used to measure change over time
plt.scatter() // Scatter plot ,  uses position to show the relationship, or correlation, between two numeric values
plt.bar() // Bar chart, uses bar height to compare a measure between categorical variables
plt.pie() // Pie chart, shows us the breakdown of a whole into its parts
plt.hist() // Histogram, shows how one kind of data is distributed
plt.barh()


Add a legend	plt.legend()
Add axis labels	plt.ylabel(), plt.xlabel()
Adjust axes	plt.xscale(), plt.yticks()
Print graph	plt.show()
```

### import
```
import matplotlib.pyplot as plt
from matplotlib import pyplot as plt
```

### remove scientific notation
```
plt.ticklabel_format(axis='y', style='plain') // 'sci', 'scientific', and 'plain'.
```

### line chart
```
plt.plot(arr,arr)
plt.plot(x,y,color='',linewidth='',linestyle='')
```

### scatter plot
```
plt.scatter(arr,arr)
plt.scatter(gdp_cap, life_exp, s = np_pop, c = [])

# Import numpy as np
import numpy as np

# Store pop as a numpy array: np_pop
np_pop = np.array(pop)

# Double np_pop
np_pop = np_pop * 2

# Update: set s argument to np_pop
plt.scatter(gdp_cap, life_exp, s = np_pop)

# Previous customizations
plt.xscale('log') 
plt.xlabel('GDP per Capita [in USD]')
plt.ylabel('Life Expectancy [in years]')
plt.title('World Development in 2007')
plt.xticks([1000, 10000, 100000],['1k', '10k', '100k'])

# Display the plot
plt.show()
```

### bar plot
```
plt.bar(x,y,color=<as much as x>)
```

* stacked column chart
```
grades = ['Freshman','Sophomore','Junior','Senior']
in_state=[40,31,15,14]
out_of_state=[60,40,33,18]

plt.bar(grades, in_state, color='r')
plt.bar(grades, out_of_state, bottom=in_state, color='b')
plt.show()
```

* stacked bar chart
```
grades = ['Freshman','Sophomore','Junior','Senior']
in_state=[40,31,15,14]
out_of_state=[60,40,33,18]

plt.barh(grades, in_state, color='r')
plt.barh(grades, out_of_state, left=in_state, color='b')

plt.xlabel("Class")
plt.ylabel("Number of students")
plt.title("Total number of student per class")

plt.show()
```

**pie**
```
df.plot.pie(autopct='%.1f%%')
```

### histogram
```
plt.hist(arr,bins=intlabel='')
plt.hist(agecon, bins=20, histtype='step')
```

### Reduce Scale
```
plt.scatter(x,y)
plt.xscale('log')
```

### axis labels
```
plt.xlabel('')
plt.ylabel('',
  family='monospace', // [ 'serif' | 'sans-serif' | 'cursive' | 'fantasy' | 'monospace' ]
  style='italic', // [ 'normal' | 'italic' | 'oblique' ]
  weight='' //'normal' | 'bold' | 'heavy' | 'light' | 'ultrabold' | 'ultralight']
)
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
plt.title('World Development in 2007',size='large', weight='bold') // [ 'xx-small' | 'x-small' | 'small' | 'medium' | 'large' | 'x-large' | 'xx-large' ]
plt.xticks([1000,10000,100000], ['1k','10k','100k'])

# Additional customizations
plt.text(1550, 71, 'India')
plt.text(5700, 80, 'China')

# Add grid() call
plt.grid(True)

plt.tick_params(axis='x', direction='out', color='red', labelsize='large', labelcolor='purple', labelrotation=30)
plt.legend(bbox_to_anchor = (1, 0.5))

plt.savefig('my_lineplot.png') //  dpi and bbox_inches
// bbox_inches = 'tight'
// bounding box or bbox.
plt.savefig('my_lineplot.png', dpi=128, bbox_inches='tight')
```

### Plot on same figure 
```

```

### Matplotlib
```
import matplotlib.pyplot as plt

plt.scatter(x,y) // to assess if there's a correlation between two variables 
plt.plot(x,y) // time scale along the horizontal axis


# Put the x-axis on a logarithmic scale
plt.xscale('log') // A correlation will become clear when you display the GDP per capita on a logarithmic scale.

plt.show()
```

* histogram
```
* show distribution
* bins
* bins width

plt.hist(x,bins=10) // 10 default


Too few bins will oversimplify reality and won't show you the details. Too many bins will overcomplicate reality and won't show the bigger picture.
```

* customization
```

plt.plot(x,y)
plt.xlabel(str)
plt.ylabel(str)
plt.title(str)

plt.yticks(
  [0,2,4,6,8,10], // bins the y values within range
  ['0B','2B','4B','6B','8B','10B'] // new Y label 
)


# Definition of tick_val and tick_lab
tick_val = [1000, 10000, 100000]
tick_lab = ['1k', '10k', '100k']

# Adapt the ticks on the x-axis
plt.xticks(tick_val,tick_lab)
```

```
# Specify c and alpha inside plt.scatter()
plt.scatter(
x = gdp_cap // list 
, y = life_exp // list
, s = np.array(pop) * 2, //list
c= col, //list
alpha = 0.8)

# Previous customizations
plt.xscale('log') 
plt.xlabel('GDP per Capita [in USD]')
plt.ylabel('Life Expectancy [in years]')
plt.title('World Development in 2007')
plt.xticks([1000,10000,100000], ['1k','10k','100k'])

# Show the plot
plt.show()

```

```
# Scatter plot
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

# Show the plot
plt.show()

```
