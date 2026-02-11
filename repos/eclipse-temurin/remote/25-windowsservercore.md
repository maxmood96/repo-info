## `eclipse-temurin:25-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:fa3218bf90fe7d80a3f03d369dd21ebce9e7112d3b2f8e10402a0c121e96cd39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32370; amd64
	-	windows version 10.0.20348.4773; amd64

### `eclipse-temurin:25-windowsservercore` - windows version 10.0.26100.32370; amd64

```console
$ docker pull eclipse-temurin@sha256:94a05bc8efea663ed5336948a4eebb7c6043fd1ad8e8d4ddf3e5c7a537f89a17
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2218798305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c89b15d4dcb916110017a3427f88b85076d8da3459bede106fe28eeb4cd36223`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Feb 2026 22:21:49 GMT
RUN Install update 10.0.26100.32370
# Tue, 10 Feb 2026 22:53:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Feb 2026 22:57:17 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Tue, 10 Feb 2026 22:57:41 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_windows_hotspot_25.0.2_10.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_windows_hotspot_25.0.2_10.msi ;     Write-Host ('Verifying sha256 (c433b59ab42630634657ae273940183c2f95a115dd5bf6846a70dcd0a42b9c0d) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'c433b59ab42630634657ae273940183c2f95a115dd5bf6846a70dcd0a42b9c0d') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-25' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 10 Feb 2026 22:57:46 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 10 Feb 2026 22:57:47 GMT
CMD ["jshell"]
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
	-	`sha256:9bf306b44c48d9a4165a5c7f64bfb2245a1e5c25879026de401ef775731bc70c`  
		Last Modified: Tue, 10 Feb 2026 22:57:51 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb313162e43337565abf2ae34639a27ee8e42587903915e4fcd10abfd925fbed`  
		Last Modified: Tue, 10 Feb 2026 22:58:07 GMT  
		Size: 253.7 MB (253671239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de2114acefef8aa3479456a44f1a610443fecd09d1c13a6928b888ba4242611`  
		Last Modified: Tue, 10 Feb 2026 22:57:51 GMT  
		Size: 363.3 KB (363273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32830ff4aa893f2d54fb8a19e5dd80cc342b5e6595b62ecb56d99f4132719043`  
		Last Modified: Tue, 10 Feb 2026 22:57:51 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:25-windowsservercore` - windows version 10.0.20348.4773; amd64

```console
$ docker pull eclipse-temurin@sha256:0c4ba5091d4ff69f361e75d5fc8052852c9dcda42cd665bca4da3cc4bd621107
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2116665794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2035f104d422c6cd2010b4d4d6bb02527e128bffdba68323acd3eeba03c79e92`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Tue, 10 Feb 2026 22:52:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Feb 2026 23:02:35 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Tue, 10 Feb 2026 23:03:02 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_windows_hotspot_25.0.2_10.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_windows_hotspot_25.0.2_10.msi ;     Write-Host ('Verifying sha256 (c433b59ab42630634657ae273940183c2f95a115dd5bf6846a70dcd0a42b9c0d) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'c433b59ab42630634657ae273940183c2f95a115dd5bf6846a70dcd0a42b9c0d') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-25' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 10 Feb 2026 23:03:09 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 10 Feb 2026 23:03:10 GMT
CMD ["jshell"]
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
	-	`sha256:d5a1a68b70a6037a04683b570a391289e218225652d139b4c315a66941376ca1`  
		Last Modified: Tue, 10 Feb 2026 22:54:47 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b85fa88e6db5bf3c5ec8edf269d55dbb442e0ac58434c2c6d5394a00d9574bdd`  
		Last Modified: Tue, 10 Feb 2026 23:03:13 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e304d5dcbb8c964b75411f482c6a4caac987dbdb211ebdbb54d65ac231d460`  
		Last Modified: Tue, 10 Feb 2026 23:03:29 GMT  
		Size: 253.7 MB (253656016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b805805d42f3819ef2f195b3e00abf99ad7cea806079c970ded9b4fdd0b1b6e3`  
		Last Modified: Tue, 10 Feb 2026 23:03:14 GMT  
		Size: 348.7 KB (348677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c79086e308f322854e72bc45060c1fcf7a448ad523aa6aba1ea75e04cdc37997`  
		Last Modified: Tue, 10 Feb 2026 23:03:14 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
