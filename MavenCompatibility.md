# `FitNesse` Launcher Plugin Compatibility<br>With Different Versions Of Maven</h1>

This matrix was deduced through simple trial and error.

| |Plugin Source Uses Maven Components| |
|:|:----------------------------------|:|
|Build The Plugin With| **3.0.5 (Plugin Version 1.3.x)**  | **3.1.1 (Plugin Version 1.4.x)** |
|Maven 3.0.5|OK                                 |OK|
|Maven 3.1.1|OK                                 |OK|
|Run The Plugin With<br>(Build A Project With)<table><thead><th>-                                  </th><th>-</th></thead><tbody>
<tr><td>Maven 3.0.5</td><td>OK                                 </td><td>OK</td></tr>
<tr><td>Maven 3.1.1</td><td> <b>NO</b>                         </td><td>OK</td></tr></tbody></table>


<h1>Major Changes<br>Maven 3.0.x --> 3.1.x</h1>

<ul><li>The use of JSR330 in the core for extensions and in Maven plugins. You can read more about it in the Maven and JSR330 document.<br>
<ul><li>If you want to use JSR-330, you must understand that your code won't be compatible with Maven 2 or 3.0.x but only with Maven 3.1.0+: even if JSR-330 is available in core since Maven 3.0-beta-3, it was made available to plugins and extensions only in Maven 3.1.0 (see MNG-5343 for more details).<br>
</li><li><b><code>FitNesse</code> Launcher continues to use Plexus.</b></li></ul></li></ul>

<ul><li>The use of SLF4J in the core for logging. You can read more about it in the Maven and SLF4J document.<br>
<ul><li>Maven 2.x and 3.0.x use Plexus logging API with basic Maven implementation writing to stdout.<br>
</li><li>The standard Maven distribution, from Maven 3.1.0 onward, uses the SLF4J API for logging combined with the SLF4J Simple implementation. Future versions may use a more advanced implementation, but we chose to start simple.<br>
</li><li><b><code>FitNesse</code> Launcher is unaffected.</b></li></ul></li></ul>

<ul><li>The switch in the core from Sonatype Aether to Eclipse Aether.<br>
<ul><li>The significant change in Eclipse Aether with respect to API changes and package relocation will likely cause issues with plugins that directly depend on Aether.<br>
</li><li><b><code>FitNesse</code> Launcher does depend directly upon Aether.</b>
</li><li>In practical terms, package changes in source code amount to:<br>
<ul><li><code>org.sonatype.aether</code> (3.0.x)<br>
</li><li><code>org.eclipse.aether</code>  (3.1.x)</li></ul></li></ul></li></ul>


<h2>See <a href='http://maven.apache.org/release-notes-3.x.html#Major_Changes'>Release Notes - Maven 3.x</a></h2>