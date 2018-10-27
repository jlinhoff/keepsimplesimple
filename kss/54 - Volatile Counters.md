---


---

<p>Volatile signals the compiler to not optimize access to the variable.</p>
<p>Use volatile for counters shared between code with different contexts.</p>
<p>Counters provide a safe and minimal way to communicate between an interrupt and foreground code. For example: when an interrupt occurs, increment the counter, clear the interrupt and return. In the main loop, check for the counter’s change and process the interrupt.</p>

