## `eclipse-temurin:23-jdk-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:361e99afc516c96570c74ee1166e002d66618829a0c3d43c38f58d3b0bb635c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `eclipse-temurin:23-jdk-windowsservercore` - windows version 10.0.26100.2894; amd64

```console
$ docker pull eclipse-temurin@sha256:b1e5888845c567c79c11c6675cb2a595c28734a7e0261192bdea667b3ea3f153
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2897548995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:830a7575f07fb15f5007aea5b805a3add448f01fb6d2f5e56f0a651994445621`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Fri, 31 Jan 2025 01:35:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Jan 2025 01:35:25 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Fri, 31 Jan 2025 01:35:51 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_x64_windows_hotspot_23.0.2_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_x64_windows_hotspot_23.0.2_7.msi ;     Write-Host ('Verifying sha256 (e4ef33439c2dc725387fce4d57ed63794785c0d3ab55726bdc9861c0387dc3a0) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'e4ef33439c2dc725387fce4d57ed63794785c0d3ab55726bdc9861c0387dc3a0') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-23' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 31 Jan 2025 01:36:00 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Fri, 31 Jan 2025 01:36:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:904315b835de2fef53078d13a5e428ef8d0e64c60f898cad5809720320d83460`  
		Last Modified: Fri, 31 Jan 2025 01:36:04 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525e636202b5f5dc61c0277f5ca2a58f9e233c3607f138a2750953e5db5188b8`  
		Last Modified: Fri, 31 Jan 2025 01:36:04 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b757498d0d3c5f45cc87d9ed4ffff9d1cddf7a339b8ca14360979251d634ad08`  
		Last Modified: Fri, 31 Jan 2025 01:36:27 GMT  
		Size: 396.9 MB (396873598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4f56b7d0f503b6c1aefa3a6d7462c8ef52293107dcbfbddf2e5607a39de68f`  
		Last Modified: Fri, 31 Jan 2025 01:36:04 GMT  
		Size: 393.8 KB (393837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6594bc5fdc4b5e6f778ea923758cf0becd5e5a8df40a74ebfc1ff36dfa5e5eeb`  
		Last Modified: Fri, 31 Jan 2025 01:36:04 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:23-jdk-windowsservercore` - windows version 10.0.20348.3091; amd64

```console
$ docker pull eclipse-temurin@sha256:90f642c409323221e27c26dbb16095a5d4aac41445f07c20bef63140d909861a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2659546478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:744bee0bce3076b2018c347b8d2b32c116ee0b067542416946bd76d611ab3e70`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Fri, 31 Jan 2025 01:30:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Jan 2025 01:30:41 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Fri, 31 Jan 2025 01:32:02 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_x64_windows_hotspot_23.0.2_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_x64_windows_hotspot_23.0.2_7.msi ;     Write-Host ('Verifying sha256 (e4ef33439c2dc725387fce4d57ed63794785c0d3ab55726bdc9861c0387dc3a0) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'e4ef33439c2dc725387fce4d57ed63794785c0d3ab55726bdc9861c0387dc3a0') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-23' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 31 Jan 2025 01:32:09 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Fri, 31 Jan 2025 01:32:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ba044f8e1d2e73b7ddeb6cc219df761f829fe28a7259cba1b24705c1b5584a`  
		Last Modified: Fri, 31 Jan 2025 01:32:13 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e326bf19a52a12609fe39b0b50156b386b5da5980e8ed6e368692f6da964ad5d`  
		Last Modified: Fri, 31 Jan 2025 01:32:13 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eea627498f4165359553c4150ab92b87514975eeddad9fa4217dba09cb1f7d0`  
		Last Modified: Fri, 31 Jan 2025 01:32:28 GMT  
		Size: 396.8 MB (396830506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf5432de68e55d4d574316bf07ce0914426edca56fdcd71a191251dc3afa67f8`  
		Last Modified: Fri, 31 Jan 2025 01:32:14 GMT  
		Size: 326.8 KB (326838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:641a711ce284af47ac320c31e6bf7457574970aafcdb59773821c672b01b1d7b`  
		Last Modified: Fri, 31 Jan 2025 01:32:16 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:23-jdk-windowsservercore` - windows version 10.0.17763.6775; amd64

```console
$ docker pull eclipse-temurin@sha256:95d9f550c35c9e36b9590d322d563736b56360d989d30d8791e4fdc58a3d0f66
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2523395974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f32ac21995f8ea2dded83d19d30dbe037f5fcb7c1e120aa4914b0aefc1650d25`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Fri, 31 Jan 2025 01:30:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Jan 2025 01:30:40 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Fri, 31 Jan 2025 01:32:49 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_x64_windows_hotspot_23.0.2_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_x64_windows_hotspot_23.0.2_7.msi ;     Write-Host ('Verifying sha256 (e4ef33439c2dc725387fce4d57ed63794785c0d3ab55726bdc9861c0387dc3a0) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'e4ef33439c2dc725387fce4d57ed63794785c0d3ab55726bdc9861c0387dc3a0') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-23' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 31 Jan 2025 01:33:00 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Fri, 31 Jan 2025 01:33:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1a883cb00c69d0bdb519d430ade95100a427618db0faba1aa3f4f3db345fff`  
		Last Modified: Fri, 31 Jan 2025 01:33:03 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195248e9049375b50543b3e7aab0eab614002615ae8dcaf2a2f550a91e680b6b`  
		Last Modified: Fri, 31 Jan 2025 01:33:03 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6da4a065c4484ac514c389dc25b97cfc8d4935d97349030ed7d5fc2e9df79c`  
		Last Modified: Fri, 31 Jan 2025 01:33:20 GMT  
		Size: 396.9 MB (396850270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce263a9a4faf3e0a138a0b2f42290f6fd488a5f51c3d99e433908652e0dcffef`  
		Last Modified: Fri, 31 Jan 2025 01:33:04 GMT  
		Size: 4.3 MB (4329578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81bb601002c74f8a1064097ac53c0bd778b8fb45643fb74b11c8514ea1e2d942`  
		Last Modified: Fri, 31 Jan 2025 01:33:03 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
