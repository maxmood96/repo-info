## `eclipse-temurin:24-jre-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:8ea5af35a199a7b85d384e5b16fab3c58aade2b241eadfc80202c7444c283858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4061; amd64

### `eclipse-temurin:24-jre-windowsservercore-ltsc2025` - windows version 10.0.26100.4061; amd64

```console
$ docker pull eclipse-temurin@sha256:42959fff8c993c4d7111b19c09966571c9aa69fe9ef72f909c4cf6788d111e8a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3530527193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b022ddaaa510170d44d923c00eaa80281c09d9314104f073fc4ea69c5a81ed0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Wed, 14 May 2025 20:55:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 May 2025 20:55:51 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Wed, 14 May 2025 20:56:10 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jre_x64_windows_hotspot_24.0.1_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jre_x64_windows_hotspot_24.0.1_9.msi ;     Write-Host ('Verifying sha256 (4562ea92299178db9966b7eb7abf9f8bb5269595f6627cede8fc77caf62a2789) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '4562ea92299178db9966b7eb7abf9f8bb5269595f6627cede8fc77caf62a2789') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-24' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 14 May 2025 20:56:18 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Thu, 15 May 2025 19:25:03 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59a8c05d13f36f76f74a2caeabdd06e72c0d912c9ef135f3f8443511586078a`  
		Last Modified: Wed, 14 May 2025 20:56:21 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f2e69095560dc0f0e1122dec1c3e6d09a12115136d5fb82f967269f0034b35`  
		Last Modified: Wed, 14 May 2025 20:56:21 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b1f23363229d097ec1e7e8dc258d890e0174d0edf6e346fea4e95cfdad1a9a3`  
		Last Modified: Wed, 14 May 2025 20:56:30 GMT  
		Size: 99.4 MB (99386276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0f9c29c734ed68020cf2bcb8ee7a707e423432243106df6f921bf8e99b32b2`  
		Last Modified: Wed, 14 May 2025 20:56:21 GMT  
		Size: 372.5 KB (372538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
