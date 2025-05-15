## `eclipse-temurin:8-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:ba748582a9b292bae4ff92b04db784062dda0d22f270c0d5a047182754f0841c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `eclipse-temurin:8-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull eclipse-temurin@sha256:1263e324a3d9667d8eb16a1d30ecf1a6a880925a9158e09949531069d06b417b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2465380799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c5a85d519db47f8a4d2ba32aa0a41daaa4265530b85a7d0286b3f7e2bf448d8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Wed, 14 May 2025 21:04:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 May 2025 21:04:41 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Wed, 14 May 2025 21:05:07 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_windows_hotspot_8u452b09.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_windows_hotspot_8u452b09.msi ;     Write-Host ('Verifying sha256 (989f085584ca58701eab2d2b2f5576b7594325f0a6f85572b34586774963c46c) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '989f085584ca58701eab2d2b2f5576b7594325f0a6f85572b34586774963c46c') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 14 May 2025 21:05:13 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Tue, 13 May 2025 18:47:51 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a33d7ac1c3d6cdcca1eed6d793d7e1e564a79c79ccb3539cfe3f95c9c69ce366`  
		Last Modified: Wed, 14 May 2025 21:05:16 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed30e4e277b86afdde47d83244b28d2c627d5f6743995d92586a9f1e1ec4054a`  
		Last Modified: Wed, 14 May 2025 21:05:16 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96683b55539ef8a12c2a1ea2b5e0296d7371ce181633ede1731d3769dd8bc07f`  
		Last Modified: Wed, 14 May 2025 21:05:25 GMT  
		Size: 191.4 MB (191384860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b4455486037db6ff245686f30f1bcba5304e5e3a3adebd59f0bb73115f5d3b4`  
		Last Modified: Wed, 14 May 2025 21:05:16 GMT  
		Size: 365.3 KB (365259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
