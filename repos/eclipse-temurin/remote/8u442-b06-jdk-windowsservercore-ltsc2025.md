## `eclipse-temurin:8u442-b06-jdk-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:f3e266d24411ca043bbe60e06760bc16f163f557d6eaf0b64ca4c26a9abd56eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `eclipse-temurin:8u442-b06-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.3476; amd64

```console
$ docker pull eclipse-temurin@sha256:f53035d4396499981355442dd9f4ba429118a38323d3a3f5efb5ab395cecf495
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3100425450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51a25db565e67cf1d9118c196ebdaa60ec43a4e8eaa8dbea586b99cb727ed70a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Wed, 12 Mar 2025 18:50:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:50:18 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Wed, 12 Mar 2025 18:50:38 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_windows_hotspot_8u442b06.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_windows_hotspot_8u442b06.msi ;     Write-Host ('Verifying sha256 (fac13d03d3d193509d82ef964060c21f2b20bc0ca3419ecc5cb3ef71283f2f94) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'fac13d03d3d193509d82ef964060c21f2b20bc0ca3419ecc5cb3ef71283f2f94') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Mar 2025 18:50:46 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ad5c40dc134601fbac5d42a3f3aa38fd0823e572a07a6b9436cf846c63c20f`  
		Last Modified: Wed, 12 Mar 2025 18:50:50 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d59fdd879f3b00ab32edc413bfd7fbe98ed519241c939af1b4b0480ccb135851`  
		Last Modified: Wed, 12 Mar 2025 18:50:50 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:514610c3e51e811929ab4292bc1d0fa23b01e47ea2634c4083616d93466e7fdb`  
		Last Modified: Wed, 12 Mar 2025 18:51:00 GMT  
		Size: 191.4 MB (191393933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:229bb6e7518c3efd0736b97dd0e527141c4fcc358104bfe0b6d5d33115df6d7b`  
		Last Modified: Wed, 12 Mar 2025 18:50:50 GMT  
		Size: 381.2 KB (381213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
