# Trails BOM

The BOM manages optional `io.github.yaforster:trails-mcp`. Add it explicitly to a wrapper and enable its read-only
MCP endpoint through `trails.mcp` configuration. Named MCP keys are independent of user authentication.

The BOM also manages `io.github.yaforster:trails-auth-none`. Select it instead of `trails-auth-oidc-jwt` for
credential-free, unrestricted access with one shared profile. Including both fails SDK composition validation.

The Trails BOM provides dependency version alignment for the Trails SDK and adapters. Import under the Maven `dependencyManagement` section.

This includes `trails-printer-pdf`, the standard zero-configuration implementation of the required printing port.
Dependency management aligns its version; consumers still add the adapter as an explicit dependency.

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
