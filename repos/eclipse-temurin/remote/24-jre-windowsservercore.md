## `eclipse-temurin:24-jre-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:d4446750605e13589d3a55ed1b89b538cae03b41a080305e837f1424313611fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `eclipse-temurin:24-jre-windowsservercore` - windows version 10.0.26100.6584; amd64

```console
$ docker pull eclipse-temurin@sha256:c6580b350b0b5dc17600b316865de3db019b44250c423a8ecc5056a8a1eab179
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3671063754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881bb8435c25922d24e65f19259b785cd37dc90bc746250be06f05886bd0055f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 10 Sep 2025 21:47:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:57:11 GMT
ENV JAVA_VERSION=jdk-24.0.2+12
# Wed, 10 Sep 2025 21:57:31 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_x64_windows_hotspot_24.0.2_12.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_x64_windows_hotspot_24.0.2_12.msi ;     Write-Host ('Verifying sha256 (701c4d93bec1fd007985518d4e9ca6ba334cb99b0db7c8773c1c8dd1faa24628) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '701c4d93bec1fd007985518d4e9ca6ba334cb99b0db7c8773c1c8dd1faa24628') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-24' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 10 Sep 2025 21:57:37 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bee5668bf3ba1627541264428f67a2ab55326377dac447bebf1d4c10460b655`  
		Last Modified: Wed, 10 Sep 2025 21:57:04 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7356fb2b6418c7a3d2cea72865c701a28528b741359b3f0736ef3c703267375e`  
		Last Modified: Wed, 10 Sep 2025 21:57:59 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c79c84297071889298d10c06280606fab989ad388fc4cf554fa10c19135517d`  
		Last Modified: Wed, 10 Sep 2025 21:58:08 GMT  
		Size: 99.3 MB (99274024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00ecda2d66892a67a1a5c334cd7f5f0c244da23e0043e3e7eba2821d77c69cb6`  
		Last Modified: Wed, 10 Sep 2025 21:57:59 GMT  
		Size: 347.4 KB (347410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:24-jre-windowsservercore` - windows version 10.0.20348.4171; amd64

```console
$ docker pull eclipse-temurin@sha256:80b008993d12aac0ed9dafb92f0e0f1a778984ded1c798d858e62eff2d973b71
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2381768744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e69322ecc04aef464b9db4bf7b1441919671c68be34ef470122904f77faf862`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 10 Sep 2025 21:53:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:53:59 GMT
ENV JAVA_VERSION=jdk-24.0.2+12
# Wed, 10 Sep 2025 21:54:23 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_x64_windows_hotspot_24.0.2_12.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_x64_windows_hotspot_24.0.2_12.msi ;     Write-Host ('Verifying sha256 (701c4d93bec1fd007985518d4e9ca6ba334cb99b0db7c8773c1c8dd1faa24628) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '701c4d93bec1fd007985518d4e9ca6ba334cb99b0db7c8773c1c8dd1faa24628') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-24' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 10 Sep 2025 21:54:28 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4099e040dab5364d73cd9952f3875b25d8740bc20dceb8e13860f7abbec96c`  
		Last Modified: Wed, 10 Sep 2025 21:54:50 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb65686a0c85133b46bfad2bf062655c6da4eb1f2e3c6e97edb5f7a7a12cc7d`  
		Last Modified: Wed, 10 Sep 2025 21:54:50 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0a3475db5cc5226545a432dcdf7be80c4a38fc50a9bb991fb01a7a383f1170`  
		Last Modified: Wed, 10 Sep 2025 21:54:57 GMT  
		Size: 99.3 MB (99269706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a2c3a258cdd8a8bd124acba829140a861faa2951fc227e61541fc2974853ec`  
		Last Modified: Wed, 10 Sep 2025 21:54:50 GMT  
		Size: 351.5 KB (351466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
