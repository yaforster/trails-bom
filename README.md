# Trails BOM

The Trails BOM provides dependency version alignment for the Trails SDK and adapters. Import under the Maven `dependencyManagement` section.

```xml
<dependencyManagement>
    <dependencies>
        <dependency>
            <groupId>io.github.yaforster</groupId>
            <artifactId>trails-bom</artifactId>
            <version>0.0.1</version>
            <type>pom</type>
            <scope>import</scope>
        </dependency>
    </dependencies>
</dependencyManagement>
```
For a different Trails release, use the corresponding BOM version so the SDK and official adapters remain aligned. Minor version differences across the stack may or may not cause issues.

## Build from source

From this repository, verify the BOM POM with the Maven wrapper:

```powershell
.\mvnw.cmd clean verify
```

The BOM project sources and release information are available in the [trails-bom repository](https://github.com/yaforster/trails-bom).
