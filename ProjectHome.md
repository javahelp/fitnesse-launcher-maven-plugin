<img src='http://maven.apache.org/images/maven-logo-2.gif' align='right' />
<img src='http://fitnesse.org/files/images/FitNesseLogoMedium.jpg' align='right' height='93' />
### Maven Plugin which directly launches ###
## `FitNesse` integration test server ##

#### The intention is to _make it easy_ to run `FitNesse` based integration tests. ####

Features:
  1. A `FitNesse` classpath variable (`${maven.classpath}`) is automatically configured with maven dependencies which are not necessarily the same as the overall project dependencies.
  1. Maven properties are automatically made available as `FitNesse` variables.
  1. Automatically downloads and unpacks `FitNesse`, and keeps working directories (by default found under target/fitnesse) separate from project `FitNesse` wiki pages (by default located under src/test/fitnesse)
  1. Can be used to run `FitNesse` as a wiki test server or as part of automated integration tests

  * [Intro (Why do we need yet another Maven plugin for FitNesse?)](http://fitnesse-launcher-maven-plugin.googlecode.com/svn/maven/site/fitnesse-launcher-maven-plugin/index.html)
  * [Usage (pom.xml configuration)](http://fitnesse-launcher-maven-plugin.googlecode.com/svn/maven/site/fitnesse-launcher-maven-plugin/usage.html)
  * [Maven Project Info](http://fitnesse-launcher-maven-plugin.googlecode.com/svn/maven/site/fitnesse-launcher-maven-plugin/project-info.html)
  * [Maven Project Reports](http://fitnesse-launcher-maven-plugin.googlecode.com/svn/maven/site/fitnesse-launcher-maven-plugin/project-reports.html)


---


  * ### The latest release version is 1.4.2 ###
    * #### All releases are in [Maven Central](http://search.maven.org/#search%7Cgav%7C1%7Cg%3A%22uk.co.javahelp.fitnesse%22%20AND%20a%3A%22fitnesse-launcher-maven-plugin%22) ####

  * ### The latest snapshot version is 1.5.0-SNAPSHOT ###
    * #### Snapshots are in [http://oss.sonatype.org/content/repositories/snapshots/](http://oss.sonatype.org/content/repositories/snapshots/uk/co/javahelp/fitnesse/) ####

  * ### Example Projects Sources ###
    * #### Available via [Downloads WIKI page](Downloads.md) ####

| This version of | Uses these versions of | | And has these |
|:----------------|:-----------------------|:|:--------------|
| **`FitNesse` Launcher**<br> Maven Plugin<table><thead><th> <b>Maven Components</b> </th><th> <b><code>FitNesse</code></b> </th><th> <b>Features and Bug Fixes</b> </th></thead><tbody>
<tr><td> 1.5.0-SNAPSHOT  </td><td> 3.2.2<br>(17 Jun 2014) </td><td> 20130530<br><a href='https://code.google.com/p/fitnesse-launcher-maven-plugin/issues/detail?id=#35'>Issue #35</a> </td><td> Maven Site Reports (<a href='https://code.google.com/p/fitnesse-launcher-maven-plugin/issues/detail?id=#4'>Issue #4</a>, <a href='https://code.google.com/p/fitnesse-launcher-maven-plugin/issues/detail?id=#5'>Issue #5</a>) <br> Log <code>FitNesse</code> Exceptions to Maven Console (<a href='https://code.google.com/p/fitnesse-launcher-maven-plugin/issues/detail?id=#36'>Issue #36</a>) </td></tr>
<tr><td> 1.4.3-SNAPSHOT  </td><td> 3.1.1<br>(17 Sep 2013) </td><td> 20140418<br>(18 Apr 2014) </td><td> <code>FitNesse</code> version upgrade </td></tr>
<tr><td> 1.4.2<br>(10 Aug 2014) </td><td> 3.1.1<br>(17 Sep 2013) </td><td> 20140201<br>(01 Feb 2014) </td><td> <code>FitNesse</code> version upgrade<br>Use of DBFit in SQL Example Project restored in this release </td></tr>
<tr><td> 1.4.1<br>(21 Jul 2014) </td><td> 3.1.1<br>(17 Sep 2013) </td><td> 20131110<br>(10 Nov 2013) </td><td> <code>FitNesse</code> version upgrade (<a href='https://code.google.com/p/fitnesse-launcher-maven-plugin/issues/detail?id=#28'>Issue #28</a>)<br>Use of DBFit in SQL Example Project broken in this release <a href='https://github.com/dbfit/dbfit/issues/173'>https://github.com/dbfit/dbfit/issues/173</a> </td></tr>
<tr><td> 1.4.0<br>(7 Jul 2014) </td><td> 3.1.1<br>(17 Sep 2013) </td><td> 20130530<br>(1 Jun 2013) </td><td> <a href='MavenCompatibility.md'>Maven Compatibility</a>: Usable with any Maven 3.x (<a href='https://code.google.com/p/fitnesse-launcher-maven-plugin/issues/detail?id=#21'>Issue #21</a>, <a href='https://code.google.com/p/fitnesse-launcher-maven-plugin/issues/detail?id=#26'>Issue #26</a>)<br>Better control of Test Suites to run, including new <code>&lt;launches&gt;</code> config (<a href='https://code.google.com/p/fitnesse-launcher-maven-plugin/issues/detail?id=#12'>Issue #12</a>, <a href='https://code.google.com/p/fitnesse-launcher-maven-plugin/issues/detail?id=#17'>Issue #17</a>, <a href='https://code.google.com/p/fitnesse-launcher-maven-plugin/issues/detail?id=#18'>Issue #18</a>)<br>Better control over <code>FitNesse</code> working dir setup (<a href='https://code.google.com/p/fitnesse-launcher-maven-plugin/issues/detail?id=#13'>Issue #13</a>, <a href='https://code.google.com/p/fitnesse-launcher-maven-plugin/issues/detail?id=#16'>Issue #16</a>, <a href='https://code.google.com/p/fitnesse-launcher-maven-plugin/issues/detail?id=#22'>Issue #22</a>, <a href='https://code.google.com/p/fitnesse-launcher-maven-plugin/issues/detail?id=#23'>Issue #23</a>, <a href='https://code.google.com/p/fitnesse-launcher-maven-plugin/issues/detail?id=#29'>Issue #29</a>)<br>Better classpath/dependency handling (<a href='https://code.google.com/p/fitnesse-launcher-maven-plugin/issues/detail?id=#27'>Issue #27</a>, <a href='https://code.google.com/p/fitnesse-launcher-maven-plugin/issues/detail?id=#30'>Issue #30</a>)</td></tr>
<tr><td> 1.3.0<br>(9 Jul 2013) </td><td> 3.0.5<br>(19 Feb 2013) </td><td> 20121220<br>(20 Dec 2012) </td><td> <a href='MavenCompatibility.md'>Maven Compatibility</a>: Use only with Maven 3.0.x<br><code>&lt;useProjectDependencies&gt;</code> config (<a href='https://code.google.com/p/fitnesse-launcher-maven-plugin/issues/detail?id=#7'>Issue #7</a>)<br>Also <a href='https://code.google.com/p/fitnesse-launcher-maven-plugin/issues/detail?id=#9'>Issue #9</a>, <a href='https://code.google.com/p/fitnesse-launcher-maven-plugin/issues/detail?id=#10'>Issue #10</a>, <a href='https://code.google.com/p/fitnesse-launcher-maven-plugin/issues/detail?id=#11'>Issue #11</a>, </td></tr>
<tr><td> 1.2.2<br>(23 Jun 2013) </td><td> 3.0.4<br>(17 Jan 2012) </td><td> 20121220<br>(20 Dec 2012) </td><td> Removed implicit reliance on <code>${fitnesse.working}</code> <br> and other properties (<a href='https://code.google.com/p/fitnesse-launcher-maven-plugin/issues/detail?id=#8'>Issue #8</a>) </td></tr>
<tr><td> 1.2.1<br>(8 Jan 2013) </td><td> 3.0.4<br>(17 Jan 2012) </td><td> 20121220<br>(20 Dec 2012) </td><td> Can be run standalone (<a href='https://code.google.com/p/fitnesse-launcher-maven-plugin/issues/detail?id=#6'>Issue #6</a>) </td></tr>
<tr><td> 1.2.0<br>(31 Dec 2012) </td><td> 3.0.4<br>(17 Jan 2012) </td><td> 20121220<br>(20 Dec 2012) </td><td> <code>FitNesse</code> version upgrade </td></tr>
<tr><td> 1.1.0<br>(23 Dec 2012) </td><td> 3.0.4<br>(17 Jan 2012) </td><td> 20111025<br>(14 Nov 2011) </td><td> set-up & tear-down goals<br>Own project on classpath (<a href='https://code.google.com/p/fitnesse-launcher-maven-plugin/issues/detail?id=#2'>Issue #2</a>) </td></tr>
<tr><td> 1.0.0<br>(5 Jun 2012) </td><td> 3.0.4<br>(17 Jan 2012) </td><td> 20111025<br>(14 Nov 2011) </td><td> Initial basic implementation </td></tr></tbody></table>


<blockquote><i><b>"... I compared a couple of the Maven plugins out there and this was matched my workflow perfectly. The plugin comes with a couple of different example Maven projects that helped me get started. I was really pleased to see my first <code>FitNesse</code> tests running 15 minutes after I found the plugin. ... Overall, this is a great project that does exactly what I need it to do."</b></i> <a href='https://www.ohloh.net/p/fitnesse-launcher-maven-plugin/reviews/summary'>Project Reviews on Ohloh</a></blockquote>

<br>
<br>
<hr />

<table><thead><th> <img src='http://fitnesse-launcher-maven-plugin.googlecode.com/svn/maven/site/fitnesse-launcher-maven-plugin/statscm/locandchurn.png' /> </th></thead><tbody></tbody></table>

<hr />

<table>
<tr><td><wiki:gadget url="http://www.ohloh.net/p/602496/widgets/project_search_code.xml" height="170" width="400" border="0"/><br>
</td><td>
<wiki:gadget url="http://www.ohloh.net/p/602496/widgets/project_factoids.xml" width="400" height="170" border="0" /><br>
</td></tr>
<tr><td>
<wiki:gadget url="http://www.ohloh.net/p/602496/widgets/project_languages.xml" height="220" width="400" border="0"/><br>
</td><td>
<wiki:gadget url="http://www.ohloh.net/p/602496/widgets/project_cocomo.xml" height="220" width="400" border="0"/><br>
</td></tr>
</table>