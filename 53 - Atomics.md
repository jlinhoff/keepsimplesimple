---


---

<p>Atomic operations run from start to finish in isolation, without the possibility of corruption from an outside operation.</p>
<p>Any atomic can be used to build any other atomic, and build a lock-free system.</p>
<p>Atomics are read-modify-write operations, and must be guaranteed at the hardware level. Typically:</p>
<ul>
<li>atomic increment</li>
<li>atomic test and set</li>
<li>atomic compare and swap</li>
</ul>
<p>If the processor doesn’t provide atomic instructions, it probably means the</p>
<p>Systems without atomic instructions require disabling interrupts to guarantee the operation is atomic. Look closely at the atomic’s read-modify-write and identify any outside system or operation that might interfere.</p>
<p>Be careful, atomics by themselves, do not guarantee order of execution.</p>
<p>Take into account:</p>
<ul>
<li>interrupts, signals</li>
<li>multiple threads</li>
<li>multiple processors</li>
</ul>

