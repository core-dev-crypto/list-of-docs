mkdir UnitTest
cd UnitTest/
curl https://api.nuget.org/downloads/nuget.exe -o nuget.exe
mono nuget.exe update
mono nuget.exe -self update
mono nuget.exe update -self

nano nuget.config

<configuration>
  <activePackageSource>
    <add key="All" value="(Aggregate source)" />
  </activePackageSource>
  <packageSources>
    <add key="nuget.org" value="https://api.nuget.org/v3/index.json" />
    <add key="nuget v2" value="https://www.nuget.org/api/v2" />
  </packageSources>
</configuration>

mono nuget.exe install NUnit
mono nuget.exe install NUnit.Runners