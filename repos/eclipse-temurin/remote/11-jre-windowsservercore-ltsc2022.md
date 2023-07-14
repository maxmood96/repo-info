## `eclipse-temurin:11-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:74f9575ee52cb6a92c1f951fa3a85f002111f6a345a032e39a58be9150447811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1850; amd64

### `eclipse-temurin:11-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.1850; amd64

```console
$ docker pull eclipse-temurin@sha256:d9f236393289e6d8aba585abc2af9bfdc10f5433ab2dc86cd7b51a5f05cab0d5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1812054122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da4ab1f7491dfa5f392c53700f0f2e28bae751249934a7848696a78e3a11eafc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 07 Jul 2023 21:29:32 GMT
RUN Install update 10.0.20348.1850
# Thu, 13 Jul 2023 20:29:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Jul 2023 21:41:30 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 13 Jul 2023 21:47:39 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_windows_hotspot_11.0.19_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_windows_hotspot_11.0.19_7.msi ;     Write-Host ('Verifying sha256 (4556ea75ccc16f762f661675bd8a22e64b52890fa2fb330729316e120791ac09) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '4556ea75ccc16f762f661675bd8a22e64b52890fa2fb330729316e120791ac09') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 13 Jul 2023 21:48:00 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c84a7416e1317a892f4786a89c62493b21df55e0e06b82a4bb007cc79df0f949`  
		Last Modified: Tue, 11 Jul 2023 18:03:32 GMT  
		Size: 348.8 MB (348766456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3e3828ab9c4326158b6161915d8bad87619b3107529ab32863eb31b684d127`  
		Last Modified: Thu, 13 Jul 2023 21:07:36 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4648a316236fcfcff722fa263897ee9e2b5f34722cbe6ee77324ffa0bb242a9`  
		Last Modified: Thu, 13 Jul 2023 22:20:16 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84333aeee848ad1b07c9b9cc1330e8a4bfdd7c8110c66b5f2d9a99e5d1ed4e8f`  
		Last Modified: Thu, 13 Jul 2023 22:22:15 GMT  
		Size: 74.4 MB (74408593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abfccc93d4c28770c4d16a957b1105420caf2f1614f327087f809bc60dc67685`  
		Last Modified: Thu, 13 Jul 2023 22:22:06 GMT  
		Size: 277.5 KB (277453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
