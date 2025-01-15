## `eclipse-temurin:11-jre-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:1d4320313195b64993ac4637fd8ee0d612eac4e7c30edee8388c94773e06ed9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `eclipse-temurin:11-jre-windowsservercore` - windows version 10.0.20348.3091; amd64

```console
$ docker pull eclipse-temurin@sha256:1549c045a778424f0dd478f429328b3608374ff8792142ab9546d18cdcfd5825
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2338508415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c30eb29ec7ef4eccef21fe0b2dd7e962d2af8d714035cce271f762f7858a08`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Tue, 14 Jan 2025 23:32:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:32:59 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Tue, 14 Jan 2025 23:33:19 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_windows_hotspot_11.0.25_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_windows_hotspot_11.0.25_9.msi ;     Write-Host ('Verifying sha256 (577f448ffe2737633bdc2a02e5c53ecccaf3317274b7013b6eb25e9de1934a79) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '577f448ffe2737633bdc2a02e5c53ecccaf3317274b7013b6eb25e9de1934a79') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 14 Jan 2025 23:33:25 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed9432e286d0acf65ed1957aed13eb2bec5064ef929464ea203bb7bffad9649`  
		Last Modified: Tue, 14 Jan 2025 23:33:29 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43d4c3e9aabc571d0a4e46174185a9bbb096b2ee75c2f900a884b68a7dc22d8`  
		Last Modified: Tue, 14 Jan 2025 23:33:29 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e65c4b3922b4077a7e8af171d4bb389e187dfce99e2e4d023e531da3a9d194c5`  
		Last Modified: Tue, 14 Jan 2025 23:33:35 GMT  
		Size: 75.8 MB (75771100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8c9c1692ca8cdd757f487ce02cfc014779c304965938353da59e3ee85e4f7f`  
		Last Modified: Tue, 14 Jan 2025 23:33:30 GMT  
		Size: 349.5 KB (349489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-windowsservercore` - windows version 10.0.17763.6775; amd64

```console
$ docker pull eclipse-temurin@sha256:6248a1c1ec3bcd07f510d6316889bffff05bfbb775f8f120d8296f4e96a0d648
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2198351554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0776d5563e2333f05166b3a4f54946ddc3e38f4ee8dbeb80ea4718e584b95317`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Tue, 14 Jan 2025 23:35:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:35:53 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Tue, 14 Jan 2025 23:36:28 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_windows_hotspot_11.0.25_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_windows_hotspot_11.0.25_9.msi ;     Write-Host ('Verifying sha256 (577f448ffe2737633bdc2a02e5c53ecccaf3317274b7013b6eb25e9de1934a79) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '577f448ffe2737633bdc2a02e5c53ecccaf3317274b7013b6eb25e9de1934a79') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 14 Jan 2025 23:36:36 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:631ef876bc4286894a3f1998e23b52b6d0f386cc8d382733a35641112d6c16c0`  
		Last Modified: Tue, 14 Jan 2025 23:36:40 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c622d33af031751b1b6bdc100e3b3590dc81d3eabba6af4784f1123994d90a4`  
		Last Modified: Tue, 14 Jan 2025 23:36:40 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9ef067d65ef3b84dc34274dc13dc4eb4f59824793e3af9e26db4164af30f439`  
		Last Modified: Tue, 14 Jan 2025 23:36:46 GMT  
		Size: 75.8 MB (75787968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d864e8cfb10e9822512a737ade3267caeec4b47eba3305a8d6f3fce85282bd`  
		Last Modified: Tue, 14 Jan 2025 23:36:40 GMT  
		Size: 348.7 KB (348723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
