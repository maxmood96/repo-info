## `eclipse-temurin:22-jdk-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:632eca4fa606612c95999a470b71bca3d1fafa1fc7613cad04c6f23a17f41067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `eclipse-temurin:22-jdk-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull eclipse-temurin@sha256:f30c9e381e2f031f204a7448b7ce13961aa9f76a5fce07ad446bb5b920821737
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2509192130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ee85b80d1b1eee64dd1669be54fab14de6f14db1dc8111580c1f50ba8a6b9c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 28 Mar 2024 01:20:56 GMT
ENV JAVA_VERSION=jdk-22+36
# Thu, 28 Mar 2024 01:23:12 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jdk_x64_windows_hotspot_22_36.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jdk_x64_windows_hotspot_22_36.msi ;     Write-Host ('Verifying sha256 (a825f7098a99a6e6a6dca621ba58a60ec285eee19a27e641870ff7cdfd223a85) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'a825f7098a99a6e6a6dca621ba58a60ec285eee19a27e641870ff7cdfd223a85') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-22' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 28 Mar 2024 01:24:36 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Thu, 28 Mar 2024 01:24:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f7c360fd7d6281bb6b494ebac22f9165235afc440fb43948425a566792f6`  
		Last Modified: Wed, 13 Mar 2024 01:29:39 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a685c5969554d9ebfd3d37a78edff8b239bcbc0f0189340fb9bbff062442ae`  
		Last Modified: Thu, 28 Mar 2024 01:38:07 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad6c0750a708c896e63d22d68ca3257ab3a611a504b1a6519d3429de66d0e13`  
		Last Modified: Thu, 28 Mar 2024 01:38:35 GMT  
		Size: 380.0 MB (380042389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61bf69b5a209ef54e62e058a583615b32e1f0ff209cbfa6d5b5fc835f31157ad`  
		Last Modified: Thu, 28 Mar 2024 01:38:09 GMT  
		Size: 4.0 MB (4045534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db64a5cd2e15da125199533ae5fa4e91c0e0bea261ddc10af0a7f5a1f49eab1`  
		Last Modified: Thu, 28 Mar 2024 01:38:08 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
