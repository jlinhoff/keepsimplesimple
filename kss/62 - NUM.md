---


---

<p>Following the sizeof discussion, the best way to get the number of elements of an array.</p>
<pre><code>.#define NUM(a) (sizeof(a)/sizeof(*(a)))
...
time_t array[ENUM_MAX];
int badNum=ENUM_MAX;
int goodNum=NUM(array);
</code></pre>
<p>Using NUM macro works in all cases where the compiler can calculate the sizes.</p>

