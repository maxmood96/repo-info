## `eclipse-temurin:11-jdk-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:983c23c51774864122f82aec28b9717921870c540bdbeaf27e9d6fd9b1c66283
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `eclipse-temurin:11-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull eclipse-temurin@sha256:00a17bc4e8f928f28acb279c291ea368afb5079158d44207a50cd1bb71572db6
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2651359414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68405177e57d7c371e3b92bd58e498fe4c431de83c779b5d375fb58221f08a44`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:27:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:27:06 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Tue, 12 Aug 2025 20:27:32 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_x64_windows_hotspot_11.0.28_6.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_x64_windows_hotspot_11.0.28_6.msi ;     Write-Host ('Verifying sha256 (5063082c0f8a35e2d033ae1ca64eea7ab02222cf04ec97b8318426443f9e1cb0) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '5063082c0f8a35e2d033ae1ca64eea7ab02222cf04ec97b8318426443f9e1cb0') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 12 Aug 2025 20:27:43 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 12 Aug 2025 20:27:44 GMT
CMD ["jshell"]
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
	-	`sha256:86a625d2baa8762d633b3cc166260802de4413804b0ee8d7419de4b203bdead1`  
		Last Modified: Tue, 12 Aug 2025 20:45:07 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af0b9740169f711a6767f4c407c9513723e2469c2b160973019af5a18d371dd2`  
		Last Modified: Tue, 12 Aug 2025 20:45:06 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a281488511cf6050660bc47be22619323b28ab823958f42817d08a2bb495b70`  
		Last Modified: Tue, 12 Aug 2025 20:45:18 GMT  
		Size: 369.3 MB (369306601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d06a8c536e9ceb980cd108902433c93c89f2a069c0e7026e9f1d68222b5ea5`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 357.0 KB (356961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd2c3b588072f7c5e2d3450aa98f8ec20b34880b413bdca6cfd259291e46a76`  
		Last Modified: Tue, 12 Aug 2025 20:45:09 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
