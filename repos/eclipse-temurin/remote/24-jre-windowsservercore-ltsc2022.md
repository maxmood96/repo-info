## `eclipse-temurin:24-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:56997106880ab7618a6478f094f1b28733a8aabdfb03a60f2119171281cbfc61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `eclipse-temurin:24-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull eclipse-temurin@sha256:427c7ca7bfca4b67fd9b7745c2839e0ad383e08cc77f933c1eea5a3cb090884a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2369642758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6015c7a1cd29e05868765049c9580794ed6564d603fc6b2156702000de2837d5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Tue, 25 Mar 2025 22:11:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 25 Mar 2025 22:11:38 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 22:12:03 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_x64_windows_hotspot_24_36.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_x64_windows_hotspot_24_36.msi ;     Write-Host ('Verifying sha256 (3c49e1699ef7b3a1e6e3afb276c0d8d2dca70d91365850ccfddce66e99dd4bd4) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '3c49e1699ef7b3a1e6e3afb276c0d8d2dca70d91365850ccfddce66e99dd4bd4') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-24' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 25 Mar 2025 22:12:09 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edbcba2d4cd0fff8bb459b22ffa7a95babc1ac9ec8a1dd3a110d12765e6ed77c`  
		Last Modified: Tue, 25 Mar 2025 22:12:11 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:960b5e79f2bf58693874bb01805550e1851d0ab8d4e83250b14e856c49c78315`  
		Last Modified: Tue, 25 Mar 2025 22:12:11 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94ecdb07dec1aecb38c16545ee512e8c2952f85d407446814a6e35d6ded89f2c`  
		Last Modified: Tue, 25 Mar 2025 22:12:19 GMT  
		Size: 99.3 MB (99337367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d105b018730c5aca7edc8fa76733f8b756bb834b7f508ee5365659a680ea6eae`  
		Last Modified: Tue, 25 Mar 2025 22:12:11 GMT  
		Size: 361.6 KB (361616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
