## `eclipse-temurin:17-jre-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:de682e20729d600d69267c8c7ba35164ab64571d4229deb05b55e43fd258de59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `eclipse-temurin:17-jre-windowsservercore` - windows version 10.0.26100.32230; amd64

```console
$ docker pull eclipse-temurin@sha256:aac7f3db87b302c21c070c5587c7ac9775df577af0a8b45ae6334d041e2717f4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1571339201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1881eb94799154968d210b895c6b77746dd0724ca53abef5f2ab2fa95aaf4b5e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Thu, 05 Feb 2026 22:16:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Feb 2026 22:16:50 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Thu, 05 Feb 2026 22:17:28 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_windows_hotspot_17.0.18_8.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_windows_hotspot_17.0.18_8.msi ;     Write-Host ('Verifying sha256 (fa15e3d32633795979395d4f42446b0fc41c8dcf4b4995d063ae4352d882ca26) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'fa15e3d32633795979395d4f42446b0fc41c8dcf4b4995d063ae4352d882ca26') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 05 Feb 2026 22:17:35 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff2762ed88d87c597ae136ce85956fea17f048b03309f8de01958f9bb52ef056`  
		Last Modified: Thu, 05 Feb 2026 22:17:39 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd681a16744c401d1649e49b2258c26675bd4259e68364f0baee3403b9e4389`  
		Last Modified: Thu, 05 Feb 2026 22:17:39 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7352a94e703209e0e4a6afa39618db2cd8344c6e247dde474fa5756915f177`  
		Last Modified: Thu, 05 Feb 2026 22:17:46 GMT  
		Size: 75.2 MB (75162788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a45fa8061726e5046b0f0bb035a84499d0e0b1098a52a4a3cee7fa9320aa8be`  
		Last Modified: Thu, 05 Feb 2026 22:17:39 GMT  
		Size: 413.5 KB (413519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jre-windowsservercore` - windows version 10.0.20348.4648; amd64

```console
$ docker pull eclipse-temurin@sha256:ded1c3547ce043a8e6cec66cd23bf4d26a02fdffacff9b58ca57166e68aa343c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1911282413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9778d1b345e3fa50ab5927ab6ba46958d6caa1bf7d65a79f99533c03dc9db88`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Thu, 05 Feb 2026 22:21:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Feb 2026 22:21:01 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Thu, 05 Feb 2026 22:21:42 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_windows_hotspot_17.0.18_8.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_windows_hotspot_17.0.18_8.msi ;     Write-Host ('Verifying sha256 (fa15e3d32633795979395d4f42446b0fc41c8dcf4b4995d063ae4352d882ca26) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'fa15e3d32633795979395d4f42446b0fc41c8dcf4b4995d063ae4352d882ca26') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 05 Feb 2026 22:21:48 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85715903d4fd4648b9c487ca4b752d150d2b37892ab30baf6bb7ac4ef8bfa1d2`  
		Last Modified: Thu, 05 Feb 2026 22:21:53 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744b55ed50abb5decdc640723edb73cd7943a6a84524bd52ce862602d28b66e5`  
		Last Modified: Thu, 05 Feb 2026 22:21:53 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108bc699b95f5ce4609d99eeb84546fc9a60cdfb265534088938a7fe8d62457a`  
		Last Modified: Thu, 05 Feb 2026 22:22:00 GMT  
		Size: 75.3 MB (75253153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:940c8600eb7955a8bb0fe5678a4daf7c1c60980047613ca12e65f83f371d01d1`  
		Last Modified: Thu, 05 Feb 2026 22:21:53 GMT  
		Size: 367.5 KB (367454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
