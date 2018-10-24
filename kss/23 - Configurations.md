---


---

<h2 id="multiple-configurations">Multiple Configurations</h2>
<p>Most projects will be built in multiple ways. For example, it may be built for regression testing that’s run from the command line by the build-server to validate a commit. Here are some ideas on configs:</p>
<ul>
<li>debug, release config</li>
<li>on the device, simulated</li>
<li>Linux, Windows, Cygwin, Mac, iOS, Android</li>
</ul>
<h2 id="defines">#defines</h2>
<p>Using #define to compile the same file multiples ways quickly hurts simplicity.</p>
<h2 id="files-and-interfaces">Files and Interfaces</h2>
<p>Define an common interface that works across the different configurations.<br>
Isolate the configuration-specific code into their own files and build for the current configuration.</p>
<p>Common interface for all configurations.</p>
<pre><code>// i2c.h
int I2CReadByte(uint8_t dev,uint8_t reg);
</code></pre>
<p>The ESP8266 bit-banging implemention.</p>
<pre><code>// i2c_esp8266.c
int I2CReadByte(uint8_t dev,uint8_t reg)
{
  // ESP8266 implemention
}
</code></pre>
<p>The Windows implimentation.</p>
<pre><code>// i2c_win.c
int I2CReadByte(uint8_t dev,uint8_t reg)
{
  // Windows implemention
}
</code></pre>
<p>A software simulation implementation.</p>
<pre><code>// i2c_sim.c
int I2CReadByte(uint8_t dev,uint8_t reg)
{
  // Software simulation implemention
}
</code></pre>

