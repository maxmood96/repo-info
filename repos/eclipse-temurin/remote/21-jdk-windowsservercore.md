## `eclipse-temurin:21-jdk-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:6fea791282a69bef93bbe6645c6368aa5eee45ca63b04886ea7a101b6e22d1be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `eclipse-temurin:21-jdk-windowsservercore` - windows version 10.0.26100.32230; amd64

```console
$ docker pull eclipse-temurin@sha256:5e27dc2d2b43d122bd47324b06fa420adab3f69dcea6bd5486b126c6d4608d14
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1876833904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff81cd15cc676e642853f95d903e6cbb625df2b60309943bcbb36c22f1f06a8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Thu, 05 Feb 2026 22:17:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Feb 2026 22:17:02 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Thu, 05 Feb 2026 22:17:57 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_windows_hotspot_21.0.10_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_windows_hotspot_21.0.10_7.msi ;     Write-Host ('Verifying sha256 (6be8643444ec20758a34ddb1231e998ac77e72f661a0d5525a8ac3e078bcbcb0) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '6be8643444ec20758a34ddb1231e998ac77e72f661a0d5525a8ac3e078bcbcb0') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 05 Feb 2026 22:18:04 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Thu, 05 Feb 2026 22:18:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4bd51021594de608b9c2ba92f1c09460e19eceb50da801338bb4b595b24bf85`  
		Last Modified: Thu, 05 Feb 2026 22:18:09 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67a42270a134965def014a16d0f3ab2585a1f687bc5c01a2437c561f63d91d9e`  
		Last Modified: Thu, 05 Feb 2026 22:18:09 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0abd8d136eea0557bb4dd335b32e26802356cb5cd2e5c6544e644f1a7ab86174`  
		Last Modified: Thu, 05 Feb 2026 22:18:29 GMT  
		Size: 380.7 MB (380688744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a58bc174a90232ac5583ebdbda6625f8841891c8d0fc14dbb9c7476abdcd2e`  
		Last Modified: Thu, 05 Feb 2026 22:18:09 GMT  
		Size: 380.9 KB (380914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c00efa4a82dc46e2f608f263e2ba529982724ee4297f572927b6e5368ec0e9`  
		Last Modified: Thu, 05 Feb 2026 22:18:08 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jdk-windowsservercore` - windows version 10.0.20348.4648; amd64

```console
$ docker pull eclipse-temurin@sha256:87cf36afd4eaf0b60efbedc1777262a02f475b15593fad550300e5baaf04f7df
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2216831054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8be0a4030a725746296baf6d58a68abab5d3bf598639aa34681c90a1ada73b0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Thu, 05 Feb 2026 22:21:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Feb 2026 22:21:01 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Thu, 05 Feb 2026 22:22:34 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_windows_hotspot_21.0.10_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_windows_hotspot_21.0.10_7.msi ;     Write-Host ('Verifying sha256 (6be8643444ec20758a34ddb1231e998ac77e72f661a0d5525a8ac3e078bcbcb0) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '6be8643444ec20758a34ddb1231e998ac77e72f661a0d5525a8ac3e078bcbcb0') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 05 Feb 2026 22:22:47 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Thu, 05 Feb 2026 22:22:47 GMT
CMD ["jshell"]
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
	-	`sha256:f1a59fc8c7e415f2ed068d8d7c3e4506e5c984eee3a51653989c8ef50ccc06c6`  
		Last Modified: Thu, 05 Feb 2026 22:22:51 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60610f549c099b2c34c157f9c4865a165b38b9738e5a277d5002f869aa018be`  
		Last Modified: Thu, 05 Feb 2026 22:22:51 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e0912ae7a1c4f333ff93a28e77f06a4c0e2188b8e40ac01812606c73afb490`  
		Last Modified: Thu, 05 Feb 2026 22:23:12 GMT  
		Size: 380.8 MB (380800954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540948c656ee369262c60c85f3831f72dbacb280e503388b90ce1ff9a6e32e53`  
		Last Modified: Thu, 05 Feb 2026 22:22:52 GMT  
		Size: 367.0 KB (366976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb50f28f2a7243765a13c415877c4f29e83a3fcd53c0ce43336eb73fed76db0`  
		Last Modified: Thu, 05 Feb 2026 22:22:51 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
