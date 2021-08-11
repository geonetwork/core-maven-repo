maven-repo
==========

This maven repository is now empty. Prior contents are relocated to repo.osgeo.org:

```xml
    <repository>
      <snapshots>
        <enabled>false</enabled>
      </snapshots>
      <id>osgeo</id>
      <name>OSGeo repository</name>
      <url>https://repo.osgeo.org/repository/release/</url>
    </repository>
```

Previously:

* GeoNetwork 2.10 included this repository as a submodule for use via local file reference.

  Submodule use by historic revision should continue to work.
  
* GeoNetwork 3.0.x used `https://raw.githubusercontent.com/geonetwork/core-maven-repo/master` URL directly
  
  To build update `~/.m2/settings.xml` to mirror `core-maven-repo`:
  
  ```xml
  <mirrors>
    <mirror>
      <id>core-maven-repo</id>
      <name>GeoNetwork Maven Repository</name>
      <url>https://repo.osgeo.org/repository/geonetwork-releases/</url>
      <mirrorOf>core-maven-repo</mirrorOf> <!-- previously https://raw.githubusercontent.com/geonetwork/core-maven-repo/master -->
    </mirror>
  </mirrors>
  ```

  To read more on using repo.osgeo.org as a mirror see [how to fix a broken build](https://wiki.osgeo.org/wiki/SAC:Repo#How_to_fix_a_broken_build) (OSGeo Wiki).