## `eclipse-temurin:11-jre-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:b61c7545198106767935abc1e8ab4992e9159b14cefafcc5f2a977082293baca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32370; amd64
	-	windows version 10.0.20348.4773; amd64

### `eclipse-temurin:11-jre-windowsservercore` - windows version 10.0.26100.32370; amd64

```console
$ docker pull eclipse-temurin@sha256:3696d7d6e7e4a9c5fa5c4092b6d2c6da8d1424bf676c50c4db3a829ed6e1aa5e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2040220338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e3ed48049b06420b2213d573580309fe5963807653cfc8fc9bb439f20fc6198`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Feb 2026 22:21:49 GMT
RUN Install update 10.0.26100.32370
# Tue, 10 Feb 2026 22:53:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Feb 2026 22:53:30 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Tue, 10 Feb 2026 22:53:46 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_x64_windows_hotspot_11.0.30_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_x64_windows_hotspot_11.0.30_7.msi ;     Write-Host ('Verifying sha256 (44067cdd34231df505c9fad10e788ae9eb6ba0acec7923a7fdb26841f3f855b7) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '44067cdd34231df505c9fad10e788ae9eb6ba0acec7923a7fdb26841f3f855b7') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 10 Feb 2026 22:53:51 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456534216d0c12d9314cda831989d54bb3f542d7d43d9772ba40654db6dbd7bc`  
		Last Modified: Tue, 10 Feb 2026 18:52:01 GMT  
		Size: 441.7 MB (441700471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a5e7fbb08adcb3734489a8b4babdef763ffff52d029c414bc9a2dd8caee23d`  
		Last Modified: Tue, 10 Feb 2026 22:53:55 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444dbb82e04c5817b1c88a5b563bab2ce9cc97d2b8fc3cc0794b17806e4df62f`  
		Last Modified: Tue, 10 Feb 2026 22:53:55 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5b85b56a8da4540327adbfa24998d860fdf8d475f787d114c3d34617c058e3`  
		Last Modified: Tue, 10 Feb 2026 22:54:03 GMT  
		Size: 75.1 MB (75105909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e13496b5734782c3afc5e8a0a59385f203894597df1951aa6113ca36bfbf3f`  
		Last Modified: Tue, 10 Feb 2026 22:53:56 GMT  
		Size: 352.0 KB (351962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-windowsservercore` - windows version 10.0.20348.4773; amd64

```console
$ docker pull eclipse-temurin@sha256:f0491751362f1bc9bbf62c3aa24883f4ae347109472796dec5f5feee76f3ea9c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1938128382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdb0bd2d55feea3fe65bdcdde0b4cd05872421b6c83143b0846a63a1905f78dd`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Tue, 10 Feb 2026 22:51:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Feb 2026 23:00:54 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Tue, 10 Feb 2026 23:01:07 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_x64_windows_hotspot_11.0.30_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_x64_windows_hotspot_11.0.30_7.msi ;     Write-Host ('Verifying sha256 (44067cdd34231df505c9fad10e788ae9eb6ba0acec7923a7fdb26841f3f855b7) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '44067cdd34231df505c9fad10e788ae9eb6ba0acec7923a7fdb26841f3f855b7') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 10 Feb 2026 23:01:13 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf582aa59c8f589f6cc77378809eabf79b679ef8c09e8e900a5ce77bf0b77e38`  
		Last Modified: Tue, 10 Feb 2026 22:55:10 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2373705ede3c57c19ad0cf0b1d800479b7c1060e45efb8bccd77e63519e99169`  
		Last Modified: Tue, 10 Feb 2026 23:01:17 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3880d462c87ff03a16e6b6aaeb09f9d4d1684a0ef88f03ecccc63e070f9a983`  
		Last Modified: Tue, 10 Feb 2026 23:01:24 GMT  
		Size: 75.1 MB (75119610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0c4c7b09f4e32b5519405539b3882aa18062bd82a45f2cd848fb1588485904`  
		Last Modified: Tue, 10 Feb 2026 23:01:17 GMT  
		Size: 348.9 KB (348941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
