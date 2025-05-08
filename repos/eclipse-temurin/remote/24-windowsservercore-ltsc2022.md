## `eclipse-temurin:24-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:0941f88dd9c75f74d1f2ea436aa445638b7c841312e7d3a4578c993f497c4373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `eclipse-temurin:24-windowsservercore-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull eclipse-temurin@sha256:dcd71b8c77d656834cf6e163eba19b9fb6ce80db07d3641fefe1033deae699c6
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2526525944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:686d027c535c79cf3f27c87391460099bd7ebf7322f6b09e2e50cf7ac3113a43`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Wed, 23 Apr 2025 16:44:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 23 Apr 2025 16:44:41 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Wed, 23 Apr 2025 16:45:08 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_x64_windows_hotspot_24.0.1_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_x64_windows_hotspot_24.0.1_9.msi ;     Write-Host ('Verifying sha256 (c820fd88f666dbb56109095a7a82ce82ebc0aedb0a0d6d1dd9f75fe2b7ac0eb0) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'c820fd88f666dbb56109095a7a82ce82ebc0aedb0a0d6d1dd9f75fe2b7ac0eb0') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-24' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 23 Apr 2025 16:45:16 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 23 Apr 2025 16:45:17 GMT
CMD ["jshell"]
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
	-	`sha256:8494466c77edaa4544745898543b95d17f61e5d17b3739058f2960732dd94330`  
		Last Modified: Wed, 23 Apr 2025 16:45:19 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59207c72e966163d82e7bbae69f8d8926013b422f699e0597ad3302bd826d021`  
		Last Modified: Wed, 23 Apr 2025 16:45:19 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901d8122a255c363dc2ac9979b3cbfcc46966eb942a55a12fd9b2394c3a5766e`  
		Last Modified: Wed, 23 Apr 2025 16:45:34 GMT  
		Size: 252.6 MB (252563274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc531822529dcc1a28b681765cb156feb4bc7cb092dbd22444ec3dba879c5eab`  
		Last Modified: Wed, 23 Apr 2025 16:45:20 GMT  
		Size: 376.2 KB (376195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b47c9d9041b06d235042747eb73f3fd98e33f9affac5e957db8535c7ab060b8`  
		Last Modified: Wed, 23 Apr 2025 16:45:19 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
