## `eclipse-temurin:17-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:46eaceaa1ce987fef0f4340dc6126b7db3528195c95fc866f03920dcd85018bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `eclipse-temurin:17-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull eclipse-temurin@sha256:33e4270f24ddbf07540fb6e7b639e3b4dfc768c70a6f28dbc074918b7d0976f3
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2349075245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:084acee2bf212be3dcc497cad4f7459737c29a263238416a57275359376eb998`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Wed, 23 Apr 2025 16:35:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 23 Apr 2025 16:35:44 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 23 Apr 2025 16:36:00 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_windows_hotspot_17.0.15_6.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_windows_hotspot_17.0.15_6.msi ;     Write-Host ('Verifying sha256 (d89bf8a260d26ed7603ec1e79b43c1297cafd9d6b184a68646c54409285d6c2f) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'd89bf8a260d26ed7603ec1e79b43c1297cafd9d6b184a68646c54409285d6c2f') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 23 Apr 2025 16:36:07 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b6ee194dfee460cc53e0f761b7ff976c08380d6cd1e70cc50ff92cfa99d176`  
		Last Modified: Thu, 08 May 2025 17:22:47 GMT  
		Size: 811.4 MB (811390127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d093b203a30b319af099e77e3dc8455f363b402a4110470fe48e72df8e29ed`  
		Last Modified: Fri, 09 May 2025 06:44:46 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b724aaa97672205dab5becb8eed387901974fff8da75fc36d6cfcdc4440cf68`  
		Last Modified: Fri, 09 May 2025 06:44:46 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8a6ac56635577b2229b9a99e00684934440a2551ff862416d234168c37ba80`  
		Last Modified: Wed, 23 Apr 2025 16:36:17 GMT  
		Size: 75.1 MB (75120628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149651f34792ef89c2f1f1dd3626784157937531af149abd3f64c438e4be1947`  
		Last Modified: Fri, 09 May 2025 06:44:46 GMT  
		Size: 369.5 KB (369500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
