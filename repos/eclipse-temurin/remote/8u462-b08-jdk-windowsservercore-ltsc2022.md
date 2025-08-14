## `eclipse-temurin:8u462-b08-jdk-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:5a25c35b51aa8fec3c93c9f3efa68e98542cf3d9710cfea01a600c49ab6f009d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `eclipse-temurin:8u462-b08-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull eclipse-temurin@sha256:3cd80d47fbbdd5f7953263d43263b3dd8e8bbf39505a71e3b6b6cb0158c5a665
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2473306391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb5719a48e03b2e072e41a6d8c79098eb8b73494425d3229af0d69e9013a231d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:26:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:26:00 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Tue, 12 Aug 2025 20:26:18 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_windows_hotspot_8u462b08.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_windows_hotspot_8u462b08.msi ;     Write-Host ('Verifying sha256 (6abb1058eb80b3ae13f63cd7aef302724aebaf0a68924fee6a503ff4a0a39901) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '6abb1058eb80b3ae13f63cd7aef302724aebaf0a68924fee6a503ff4a0a39901') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 12 Aug 2025 20:26:25 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58a3fd212e50f830be3301951f17d0adc53b328829844a9b1cd344b4bda275b4`  
		Last Modified: Tue, 12 Aug 2025 20:28:07 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e277124d6393426f769e392a89c7d232ebad0cce1cc318a0a609a72f2a165b4`  
		Last Modified: Tue, 12 Aug 2025 20:28:08 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a1f26c01f70740d32d9e20e2db1e22436d0974c5014510c7954225091f92a8`  
		Last Modified: Tue, 12 Aug 2025 20:45:23 GMT  
		Size: 191.3 MB (191263645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17bd25301e3bc6186dad82670d572b1631e1ed77d6d2b3eb58431a4bd5491f3d`  
		Last Modified: Tue, 12 Aug 2025 20:28:11 GMT  
		Size: 348.2 KB (348227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
