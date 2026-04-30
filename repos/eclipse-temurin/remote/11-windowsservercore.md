## `eclipse-temurin:11-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:d094157cec262b192c4a9581e157d7254296002334d78644b1dcc8b582abbbfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32690; amd64
	-	windows version 10.0.20348.5020; amd64

### `eclipse-temurin:11-windowsservercore` - windows version 10.0.26100.32690; amd64

```console
$ docker pull eclipse-temurin@sha256:aad45d3ba974e98b36391d9367e0d2b81d038e75ebc81870bb7d774175d6647e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2500312809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e83a3489f953c0a7aea1e45bf848b96a41d9123fcafd2e35b14a14237a200cd`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Wed, 29 Apr 2026 22:46:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 Apr 2026 22:46:44 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 29 Apr 2026 22:48:20 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_windows_hotspot_11.0.31_11.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_windows_hotspot_11.0.31_11.msi ;     Write-Host ('Verifying sha256 (432d897f39766288a5747ec5f4927136ce89b743df2ab436cf7d230fbbcd596a) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '432d897f39766288a5747ec5f4927136ce89b743df2ab436cf7d230fbbcd596a') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 29 Apr 2026 22:48:26 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 29 Apr 2026 22:48:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3642e4b8bb65ad3768f9f74a0dc48bb2e3294779b5d51573a234bfbe4f65324e`  
		Last Modified: Tue, 14 Apr 2026 18:48:19 GMT  
		Size: 606.9 MB (606926634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a14b1ab823928f463b4116f5097425013fadfeafe8e1197e48a6fc31d0b442f`  
		Last Modified: Wed, 29 Apr 2026 22:48:31 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c58ee3f9682c5208560950643c27df8146f711f6a0d2052c02808cb8d06d226d`  
		Last Modified: Wed, 29 Apr 2026 22:48:31 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c904db6727b6c02b68dbc30195f3026da3c345ffd75bd930eff9a5e83a6b9af`  
		Last Modified: Wed, 29 Apr 2026 22:48:48 GMT  
		Size: 370.0 MB (369962589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb27a1e6937a7df008ed69d95755b0d984d4927e5aff423d2b78637b4f6c9d8`  
		Last Modified: Wed, 29 Apr 2026 22:48:31 GMT  
		Size: 360.3 KB (360265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2abbabe87ef1751ae74b3b4484e54d483a368abec211a213d4e29fbad1cf141f`  
		Last Modified: Wed, 29 Apr 2026 22:48:31 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-windowsservercore` - windows version 10.0.20348.5020; amd64

```console
$ docker pull eclipse-temurin@sha256:5f9a3b526f926110c5d55a7689f3bc006f3214e472ef9b02969b3ed2a06555ed
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2440483292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4147f28e2fcb854db43ba2f7e2527a732e673deaa3e68ef16ce3b34320123c25`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Wed, 29 Apr 2026 22:49:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 Apr 2026 22:49:59 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 29 Apr 2026 22:51:35 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_windows_hotspot_11.0.31_11.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_windows_hotspot_11.0.31_11.msi ;     Write-Host ('Verifying sha256 (432d897f39766288a5747ec5f4927136ce89b743df2ab436cf7d230fbbcd596a) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '432d897f39766288a5747ec5f4927136ce89b743df2ab436cf7d230fbbcd596a') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 29 Apr 2026 22:51:44 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 29 Apr 2026 22:51:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881adac9baa303e4738660f9fd178c83fa652492d7841586a9540b0b9e48a059`  
		Last Modified: Wed, 29 Apr 2026 22:51:48 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:893b1435f2a41e52c0b48b7092d8e05efae8a7f09d9133aea2ed7a9f6f67f770`  
		Last Modified: Wed, 29 Apr 2026 22:51:48 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b182741e17613c9958d8899d596198ee4813c5c6425d2236ec01f08b5ef4ce68`  
		Last Modified: Wed, 29 Apr 2026 22:52:08 GMT  
		Size: 369.9 MB (369935878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2634d120f8e8d4bbeb30fb4447076e2819fde4d8d5dd12dd5b48ee0e540b0171`  
		Last Modified: Wed, 29 Apr 2026 22:51:49 GMT  
		Size: 332.3 KB (332259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4bf31a0fc957684e5f4e41bb4458476d159465d97d40b0503560d2474a6854`  
		Last Modified: Wed, 29 Apr 2026 22:51:48 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
