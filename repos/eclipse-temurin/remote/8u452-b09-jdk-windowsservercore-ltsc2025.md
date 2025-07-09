## `eclipse-temurin:8u452-b09-jdk-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:1f70ae92fbad68239836f19d9c0943cfcda10e6a8464f8016227aa724056770e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4652; amd64

### `eclipse-temurin:8u452-b09-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.4652; amd64

```console
$ docker pull eclipse-temurin@sha256:3bfbfc83625c3980ed38c5d0cd991daa3b37e53d03b47ace3ee78f3dc829a535
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3682940135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa5875ae7408dc82dff90f35f20110830621945162ea35327108e764d8e7747a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 05 Jul 2025 18:40:54 GMT
RUN Install update 10.0.26100.4652
# Wed, 09 Jul 2025 18:08:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jul 2025 18:09:01 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Wed, 09 Jul 2025 18:09:24 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_windows_hotspot_8u452b09.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_windows_hotspot_8u452b09.msi ;     Write-Host ('Verifying sha256 (989f085584ca58701eab2d2b2f5576b7594325f0a6f85572b34586774963c46c) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '989f085584ca58701eab2d2b2f5576b7594325f0a6f85572b34586774963c46c') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 09 Jul 2025 18:09:36 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ebc78effce2335b8fe04c34f5f1f3e33e513d5a7831fa81718af6737b3d654`  
		Last Modified: Wed, 09 Jul 2025 19:09:08 GMT  
		Size: 1.3 GB (1275866158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c2756b49a5dfe757a8d93034ce5673878fdafcbffe218f253bc179456b4a28`  
		Last Modified: Wed, 09 Jul 2025 19:08:42 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e7776178422716e95ed1d69c25cfcd7d4f7785c65e2d7218423d1a543522d3`  
		Last Modified: Wed, 09 Jul 2025 19:08:44 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5fbb79c72928b6ba7c3921fee5187946c5300e056e7eae411b6abaff233e32`  
		Last Modified: Wed, 09 Jul 2025 19:09:08 GMT  
		Size: 191.4 MB (191398803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa399bd281e7a0d1ffacd5c7284d696e564a1c8cf0a7f94b492f719b32d8afdd`  
		Last Modified: Wed, 09 Jul 2025 19:09:10 GMT  
		Size: 365.4 KB (365377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
