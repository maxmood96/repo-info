## `eclipse-temurin:8u452-b09-jre-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:ab2e87b58928e81aed40c7594ef457947a75f2d08d7b0e5e74bf8e49a0aa896e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4061; amd64

### `eclipse-temurin:8u452-b09-jre-windowsservercore-ltsc2025` - windows version 10.0.26100.4061; amd64

```console
$ docker pull eclipse-temurin@sha256:7ff698a2504dcf699c794b21e6dddc39a1ea12396a91bfe0c503bb278ee31e4e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3503899425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b1f1c42852b133a1f643af6cc1596eead2a87abaa1464c824b083ad9e005d31`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Wed, 14 May 2025 20:55:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 May 2025 20:55:07 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Wed, 14 May 2025 20:55:20 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_x64_windows_hotspot_8u452b09.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_x64_windows_hotspot_8u452b09.msi ;     Write-Host ('Verifying sha256 (aa75823c6dee1d65b53da6b1e9bd7de8a521e01f7e95dea2b5f104be0ee58242) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'aa75823c6dee1d65b53da6b1e9bd7de8a521e01f7e95dea2b5f104be0ee58242') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 14 May 2025 20:55:26 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
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
	-	`sha256:457e9b7b16e4e136399745842a42b8a4d3e9c1c7daf5d809d5b145b1b794bdfc`  
		Last Modified: Fri, 16 May 2025 19:05:18 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dae735ea0f4f63fa5334fb4610bc62ca55e34cc1ba1dd035fcabf8084ed6441`  
		Last Modified: Fri, 16 May 2025 19:05:19 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5285a3da0cd9b215994280e6cbcff4ad856df09423dbcd5d25015acdc84e8ba4`  
		Last Modified: Fri, 16 May 2025 19:05:43 GMT  
		Size: 72.8 MB (72766030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f29655aa83714fbbc18c6b8504fbffac1060755f9bbde89d369ab1e782d2cd`  
		Last Modified: Fri, 16 May 2025 19:05:15 GMT  
		Size: 365.1 KB (365087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
