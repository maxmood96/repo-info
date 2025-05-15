## `eclipse-temurin:21-jre-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:fb68c40368c0c741e221180b6853f0eccf0404644b5ae8da43b099aa1480196d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4061; amd64
	-	windows version 10.0.20348.3692; amd64

### `eclipse-temurin:21-jre-windowsservercore` - windows version 10.0.26100.4061; amd64

```console
$ docker pull eclipse-temurin@sha256:782f074fb8a7867d74c5727dd222eca6dd96b45b78b389b1aaae4fb381401bc6
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3514751347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b717e9fdd514af78fedb47b57e0a0aed570226d3ac5ae234f05821c3bffd0933`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Wed, 14 May 2025 20:55:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 May 2025 20:55:04 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 14 May 2025 20:55:21 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_x64_windows_hotspot_21.0.7_6.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_x64_windows_hotspot_21.0.7_6.msi ;     Write-Host ('Verifying sha256 (7c75fbd2c99649580b7869b756effa5b6b30e6808fae1ebc7eeb63921aafd096) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '7c75fbd2c99649580b7869b756effa5b6b30e6808fae1ebc7eeb63921aafd096') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 14 May 2025 20:55:28 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
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
	-	`sha256:96c9cc4e67ae7c5b458befabb4a8ac71724e8ec3198885932d69351bbc30f9ff`  
		Last Modified: Wed, 14 May 2025 20:55:32 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d8314697422fab18054887289753cf52a2e76bb17e724880901444113813be`  
		Last Modified: Wed, 14 May 2025 20:55:32 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0465696844d1dc591e8070f59af733e374da4f4cd5b7f655eb95605f7fa5d99e`  
		Last Modified: Wed, 14 May 2025 20:55:39 GMT  
		Size: 83.6 MB (83602511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87be2a01a5c746ca213f97a3359c1680d697d5b53fe369a45716f6e7a3be3048`  
		Last Modified: Wed, 14 May 2025 20:55:32 GMT  
		Size: 380.5 KB (380453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-windowsservercore` - windows version 10.0.20348.3692; amd64

```console
$ docker pull eclipse-temurin@sha256:f52c6f9257a0b74d9cfdb8445e1e113573b0b185de0b9f64f444f2f1140da90c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2357548574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2504519f5cb849c26e5b85d91d446fc64a2478007fc403690bd8c2b5dafd91f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Wed, 14 May 2025 21:03:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 May 2025 21:03:34 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 14 May 2025 21:03:55 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_x64_windows_hotspot_21.0.7_6.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_x64_windows_hotspot_21.0.7_6.msi ;     Write-Host ('Verifying sha256 (7c75fbd2c99649580b7869b756effa5b6b30e6808fae1ebc7eeb63921aafd096) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '7c75fbd2c99649580b7869b756effa5b6b30e6808fae1ebc7eeb63921aafd096') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 14 May 2025 21:04:02 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b264922a5ac6823df00129805c9fdf374c17ec8e3faf35c999d6abd0c8c754`  
		Last Modified: Wed, 14 May 2025 21:04:04 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c73d54655df05978d87c720a57217d1b4fc19e712439a092bbb4dbdf3cd6c6`  
		Last Modified: Wed, 14 May 2025 21:04:04 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1ede3faa9e237d66a974235e5421816ead67932a843f0f6c9cadb625b2a41e3`  
		Last Modified: Wed, 14 May 2025 21:04:10 GMT  
		Size: 83.6 MB (83574048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b41c86d3a795189f6daf199f5c6ed2d6700fbc84585f729a5fccdb31f14893e4`  
		Last Modified: Wed, 14 May 2025 21:04:04 GMT  
		Size: 343.8 KB (343831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
