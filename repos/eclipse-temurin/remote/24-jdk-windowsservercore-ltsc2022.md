## `eclipse-temurin:24-jdk-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:a7735415c40f7ff86e0229793f57f282fa29d56901368474b088cbc98bc9bce2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `eclipse-temurin:24-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull eclipse-temurin@sha256:2bbae1f9264d057bedd2ba5dd4288db404da26105869b7875abf4bbbc9f0a65c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2522869417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a2bc19428211827bd503a96e43cc42639d63c5e748656d7da787a4e3cf1fdb5`
-	Default Command: `["jshell"]`
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
# Tue, 25 Mar 2025 22:12:07 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_x64_windows_hotspot_24_36.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_x64_windows_hotspot_24_36.msi ;     Write-Host ('Verifying sha256 (168a9d9ead2f75de44f6d49ac35a58879066c1215375824ada6e6dc4a9ad0b95) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '168a9d9ead2f75de44f6d49ac35a58879066c1215375824ada6e6dc4a9ad0b95') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-24' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 25 Mar 2025 22:12:15 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 25 Mar 2025 22:12:15 GMT
CMD ["jshell"]
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
	-	`sha256:822c4ef9e7d7b4e42106ffb946b1db45f41ec635401a8e64d8eaeac238c321ac`  
		Last Modified: Tue, 25 Mar 2025 22:12:17 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a0cc1f6c841087c17f8f24cc083835f69b68d2236e9f9822046101f0492173`  
		Last Modified: Tue, 25 Mar 2025 22:12:18 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2592a0351936d6f085a5e676170c99c4e7614259348cbdf3b98fdf9e7948fb`  
		Last Modified: Tue, 25 Mar 2025 22:12:30 GMT  
		Size: 252.6 MB (252552008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a586d8252ad803d704aa318d43d0793967fd4c4ad9732120d6fe7cb17dcd955`  
		Last Modified: Tue, 25 Mar 2025 22:12:18 GMT  
		Size: 372.3 KB (372335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29bb14c0626119291182e8f7c1ac6360f9ca0f9b4deb7662008457294ae29b76`  
		Last Modified: Tue, 25 Mar 2025 22:12:17 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
