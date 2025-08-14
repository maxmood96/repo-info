## `eclipse-temurin:24-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:7355c0653231a80dfc99d33576bc4b3810621213ad6fb2199a245372fbe6da78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `eclipse-temurin:24-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull eclipse-temurin@sha256:4d2c32ffe8bc1bbf4b1b1b8ec4f0a14d0acea4719f112c8aa83791e419d86c12
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2534524754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a7b04023ee5958bd49635705dc0a9e692267b1efccdb742d37b65349069218`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:26:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:26:57 GMT
ENV JAVA_VERSION=jdk-24.0.2+12
# Tue, 12 Aug 2025 20:27:19 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_x64_windows_hotspot_24.0.2_12.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_x64_windows_hotspot_24.0.2_12.msi ;     Write-Host ('Verifying sha256 (be608fa0c8a0b106b2051fbef941e8021d53d799d22172719b8f8b1eef4b361c) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'be608fa0c8a0b106b2051fbef941e8021d53d799d22172719b8f8b1eef4b361c') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-24' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 12 Aug 2025 20:27:28 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 12 Aug 2025 20:27:29 GMT
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
	-	`sha256:77ba991321401941592a8475cb419469264968b7d319c48a3f2e07fae3f33607`  
		Last Modified: Tue, 12 Aug 2025 20:29:02 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f2f126a592dd299e2a3b0de8c6a53c62fbfc308e1ebcdae4706a737910d890`  
		Last Modified: Tue, 12 Aug 2025 20:29:03 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cfca669bc809848bb51055d8c5eb961d7383aaa661b96935150ae0cd5aa6031`  
		Last Modified: Tue, 12 Aug 2025 20:45:41 GMT  
		Size: 252.5 MB (252482445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83cef8a961c4634a14f58226f7cbf5c39989b5725dd2f25794dde741da715b64`  
		Last Modified: Tue, 12 Aug 2025 20:45:14 GMT  
		Size: 346.5 KB (346489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff74d287bfca478a6e860f207e6dd06b132852ddd7237547212aeba61d24a1b5`  
		Last Modified: Tue, 12 Aug 2025 20:29:06 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
