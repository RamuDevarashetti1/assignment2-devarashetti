# Ramu Devarashetti
###### McDonald's

Around McD we have **Wallmart** Store and to the other side we have **PizzaHut**. It is a nice place to visit for food.

***
### Path to McDonald's from the Neraest Airport
The Nearest Airport to McD is Kansas City (MCI) Airport. 
1. Get on I-29 N from NW 120th St (3 min, 1.2 mi)
2. Follow I-29 N to US-71 N in Jefferson Township. Take exit 56A from I-29 N (38 min, 43.5 mi)
3. Follow US-71 N to your destination in Maryville
4. On your Left side you will find the McD

### Recommended Items from McD
* Crispy Chicken Sandwich
* McChicken®
* Filet-O-Fish®
* World Famous Fries®
***
[About Ramu](AboutMe.md)
***
### Sports I Recommend
Sports are defined as physical or mental exertion by individuals and are committed to maintaining physical or mental fitness. There are many types of exercise that can be practiced as a healthy habit, such as Baseball, Tennis, Football, Cricket, and these sports have many benefits on the human body.

#### Table Below Showing the Details About the Each Sport
|Name of the Sport| Location    | Amount Needed for Equipment|
| ---             | ---         |  ---                       |
|Cricket          |Hyderabad    |  $100                      |
|Tennis           |Gachibowli   |  $75                       |
|Baseball         |Maryville    |  $200                      |
|Football         |Kansas City  |  $250                      |

***
#### Quotes I Like
> Everything is hard before it is easy. *Johann Wolfgang von Goethe*

> Don't let your happiness depend on something you may lose. *PC.S. Lewis*

***
### Intro to Sqrt (or Square Root) Decomposition Data Structure
> Sqrt (or Square Root) Decomposition Technique is one of the most common query optimization technique used by competitive programmers. This technique helps us to reduce Time Complexity by a factor of sqrt(n). The key concept of this technique is to decompose given array into small chunks specifically of size sqrt(n).

Here is the link to the Algorithm Intro <https://www.geeksforgeeks.org/sqrt-square-root-decomposition-technique-set-1-introduction/>

```
// input data
int n;
vector<int> a (n);

// preprocessing
int len = (int) sqrt (n + .0) + 1; // size of the block and the number of blocks
vector<int> b (len);
for (int i=0; i<n; ++i)
    b[i / len] += a[i];

// answering the queries
for (;;) {
    int l, r;
  // read input data for the next query
    int sum = 0;
    for (int i=l; i<=r; )
        if (i % len == 0 && i + len - 1 <= r) {
            // if the whole block starting at i belongs to [l, r]
            sum += b[i / len];
            i += len;
        }
        else {
            sum += a[i];
            ++i;
        }
}
```

Here is the link to the Code <https://cp-algorithms.com/data_structures/sqrt_decomposition.html>
