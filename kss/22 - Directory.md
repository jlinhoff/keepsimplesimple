---


---

<p>Organize your directory structure to mirror the breakdown of your project. Projects consist of multiple programs that share header files. Share only what’s necessary to minimize dependencies and maximize future flexibility.</p>
<h2 id="levels-of-sharing">Levels Of Sharing</h2>
<p>At the top level:</p>
<ul>
<li>world-wide
<ul>
<li>e.g. stdtypes.h, stdlib</li>
</ul>
</li>
<li>external-libraries
<ul>
<li>SQLite, cURL</li>
</ul>
</li>
<li>company-wide</li>
<li>project-wide</li>
<li>platform-based</li>
</ul>
<h2 id="shallow">Shallow</h2>
<p>Directory scope is from broad to narrow. Keep the directory depth down. Think about a directory as a package or library.</p>

