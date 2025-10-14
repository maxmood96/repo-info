## `eclipse-temurin:25-jdk-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:30d5d31fa2a92dd629c82fa4ed3393d13c176b0affd6bed4e03831a7485abf28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4294; amd64

### `eclipse-temurin:25-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.4294; amd64

```console
$ docker pull eclipse-temurin@sha256:0b8601d4601783992856ffd5fd83ecbd2ba1c68574f4f47f5771d8b02ead3009
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1742877827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7123c46c745aeda779070f62e4b4c4841b967e71bc9ef94e6f34c81c3cd0f3db`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 14 Oct 2025 20:41:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:47:45 GMT
ENV JAVA_VERSION=jdk-25+36
# Tue, 14 Oct 2025 20:48:05 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_x64_windows_hotspot_25_36.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_x64_windows_hotspot_25_36.msi ;     Write-Host ('Verifying sha256 (d899afd9c8160b8de9dcf2cced8da33702e00104068eac50e33dd1cbf1df5248) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'd899afd9c8160b8de9dcf2cced8da33702e00104068eac50e33dd1cbf1df5248') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-25' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 14 Oct 2025 20:48:11 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 14 Oct 2025 20:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d69910297fad50ffc461b607623e7deea128c2f2ed652341ab8682223c1249b`  
		Last Modified: Tue, 14 Oct 2025 20:45:19 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f79780ea06a2d75011cefe6297cb93cc3a5c2bed70a3f86413dfa8ea0b97cc`  
		Last Modified: Tue, 14 Oct 2025 20:48:38 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af010825ba113a2eb6739a55bf37efd6cdf00b97639bced93a4dd62ee193109`  
		Last Modified: Tue, 14 Oct 2025 21:14:53 GMT  
		Size: 253.5 MB (253502665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f8db394c58510f8ae6eac903c735644f9a8cb0d8db5d657ada783399409fa4`  
		Last Modified: Tue, 14 Oct 2025 20:48:38 GMT  
		Size: 352.2 KB (352156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c3c299f1ceb3df23e702c21a0c524a4b25a8f5617247f9e6ce4a148f702a09`  
		Last Modified: Tue, 14 Oct 2025 20:48:38 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
