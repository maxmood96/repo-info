## `eclipse-temurin:11-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:0f54f3b6cadaa4f7020491cf9fdfead74e4beae7a54c74859852567ff3c6a817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `eclipse-temurin:11-windowsservercore-ltsc2022` - windows version 10.0.20348.5020; amd64

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
