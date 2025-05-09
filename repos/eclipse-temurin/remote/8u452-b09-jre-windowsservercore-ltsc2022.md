## `eclipse-temurin:8u452-b09-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:e618058268e58b867eb936df04d2ed49c8922e602995e5faa79f2de60615edfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `eclipse-temurin:8u452-b09-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull eclipse-temurin@sha256:2254350528bc550e662bb031875647f052009ab7b77e941848fd64ba0aa051e2
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346730246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376300388aeb3c0968c02a34eac1aaf812824bc97e12c49dd2aa169bab823b07`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Mon, 28 Apr 2025 20:18:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 28 Apr 2025 20:18:34 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Mon, 28 Apr 2025 20:18:57 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_x64_windows_hotspot_8u452b09.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_x64_windows_hotspot_8u452b09.msi ;     Write-Host ('Verifying sha256 (aa75823c6dee1d65b53da6b1e9bd7de8a521e01f7e95dea2b5f104be0ee58242) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'aa75823c6dee1d65b53da6b1e9bd7de8a521e01f7e95dea2b5f104be0ee58242') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Mon, 28 Apr 2025 20:19:04 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b6ee194dfee460cc53e0f761b7ff976c08380d6cd1e70cc50ff92cfa99d176`  
		Last Modified: Fri, 18 Apr 2025 03:14:44 GMT  
		Size: 811.4 MB (811390127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d05ca465a51249d55e11e8eb7418d4806f32384fde62aa317aa39052136275`  
		Last Modified: Mon, 28 Apr 2025 20:19:06 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60ac88fecea6e1d0dcd75338bc6f5f15a67e184726ade2c9359aed40b31ac029`  
		Last Modified: Mon, 28 Apr 2025 20:19:06 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd8de2f820be8ccfcd4860e20e01cfde20b457fdf60c8e3354d2b3dbb3f19e5`  
		Last Modified: Mon, 28 Apr 2025 20:19:10 GMT  
		Size: 72.8 MB (72772480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acb8c771a151bec2fe2cbc8d0830c01ab0fe590d26277e21acdf37ac2e3195c1`  
		Last Modified: Mon, 28 Apr 2025 20:19:06 GMT  
		Size: 372.7 KB (372663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
