## `eclipse-temurin:17-jre-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:356586d89a3b2dc1e72bf7beb92cf34fd3887d30afa903a09ec9cc3cc5712461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `eclipse-temurin:17-jre-windowsservercore-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull eclipse-temurin@sha256:62dd59fc1e6666a81db43219fda37b3fcc677a8166a6db3bf16d93c8f7ee0e07
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3551696661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea2a6bd35800b02688b8ffbd28e6907cd494f78e6e912e8bb16a1780985e9a63`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Tue, 10 Jun 2025 21:28:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Jun 2025 21:28:06 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Tue, 10 Jun 2025 21:28:21 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_windows_hotspot_17.0.15_6.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_windows_hotspot_17.0.15_6.msi ;     Write-Host ('Verifying sha256 (d89bf8a260d26ed7603ec1e79b43c1297cafd9d6b184a68646c54409285d6c2f) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'd89bf8a260d26ed7603ec1e79b43c1297cafd9d6b184a68646c54409285d6c2f') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 10 Jun 2025 21:28:29 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b61d8f1bb5129502a06cea04657715aa68d500a1dc0ddcf37003afcd263c28`  
		Last Modified: Tue, 10 Jun 2025 22:09:36 GMT  
		Size: 1.3 GB (1260866861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ad40039f2cf4be8280a29afaa64003c34f12e29179c07e0e83ba195f90002a`  
		Last Modified: Tue, 10 Jun 2025 21:32:02 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24cb42fc41327988188c746a4780167d190d4d726fdc4b76f7d222fa2d6a62e7`  
		Last Modified: Tue, 10 Jun 2025 21:32:02 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bbb28b49256f0cb49fb5be345642fb71549f37515449b09f05092f915a32889`  
		Last Modified: Tue, 10 Jun 2025 21:32:07 GMT  
		Size: 75.1 MB (75136534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493fd8697821e85b69a336e80401104cdfba4643d7eb6667dbc60575ec32a424`  
		Last Modified: Tue, 10 Jun 2025 21:32:02 GMT  
		Size: 383.4 KB (383401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
