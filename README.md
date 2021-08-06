maven-repo
==========

This maven repository should not be used directly, it is cached at repo.osgeo.org:

```xml
    <repository>
      <snapshots>
        <enabled>false</enabled>
      </snapshots>
      <id>osgeo</id>
      <name>OSGeo repository</name>
      <url>https://repo.osgeo.org/repository/geonetwork-cache/</url>
    </repository>
```

This maven respository is not intended for direct use, it was setup for GeoNetwork 2.10 and use as a submodule via a local file reference.

If you find an older codebase such as GeoNetwork 3.0.x please update you `~/.m2/settings.xml` to mirror `core-maven-repo`:
```xml
<mirrors>
  <mirror>
    <id>core-maven-repo</id>
    <name>GeoNetwork Maven Repository</name>
    <url>https://repo.osgeo.org/repository/geonetwork-cache/</url>
    <mirrorOf>core-maven-repo</mirrorOf> <!-- previously https://raw.githubusercontent.com/geonetwork/core-maven-repo/master -->
  </mirror>
</mirrors>
```

For more information using repo.osgeo.org see [how to fix a broken build](https://wiki.osgeo.org/wiki/SAC:Repo#How_to_fix_a_broken_build) (OSGeo Wiki).

## Maintenance

Generate archetype catalog using:

```
mvn archetype:crawl -Dcatalog=archetype-catalog.xml -Drepository=.
```


