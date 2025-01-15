## `eclipse-temurin:8u432-b06-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:d98ee60598d13be2cde3d7d5cdb6830c7c5f73c7576ef324dcdfeee90251b2e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `eclipse-temurin:8u432-b06-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull eclipse-temurin@sha256:5ed72e9920a4ec360f6d715a3636262b7b4ef4932af9e013a4bdc4e9d3711ed4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2336017319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618a1f426b759bc401bc6e40a0221b3db4208f8d3df1c70fce9e28bf4cd84474`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Tue, 14 Jan 2025 23:35:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:35:30 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Tue, 14 Jan 2025 23:35:46 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_x64_windows_hotspot_8u432b06.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_x64_windows_hotspot_8u432b06.msi ;     Write-Host ('Verifying sha256 (34801770278c26045517fc1851396d7bf66c7c32fa6f9965b968d55adbebda4b) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '34801770278c26045517fc1851396d7bf66c7c32fa6f9965b968d55adbebda4b') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 14 Jan 2025 23:35:52 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
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
	-	`sha256:3044ed2130554bdf30eb5f376fe3fee0c48ccc6ae746ed966946287bd3616ea3`  
		Last Modified: Tue, 14 Jan 2025 23:35:54 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3fe08508f2d5db2dde1ac333e781e222d57844c537a34cfefb50af056cfaa2`  
		Last Modified: Tue, 14 Jan 2025 23:35:54 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa9a5b3db67b59ad8a88891efa5461230fef5f8a89878238255a49c0b28dec4`  
		Last Modified: Tue, 14 Jan 2025 23:35:59 GMT  
		Size: 73.3 MB (73281752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a976d441b63f99f9599ab64cfc17c09eb0769864ebc5295a1f1096d0dd13d1`  
		Last Modified: Tue, 14 Jan 2025 23:35:55 GMT  
		Size: 347.7 KB (347738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
