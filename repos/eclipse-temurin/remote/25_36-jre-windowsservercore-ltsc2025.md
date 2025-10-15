## `eclipse-temurin:25_36-jre-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:c9c92cda052fea1510c5ef40b44dc7a0da02895cea055fd0b50414c0fe8d89ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6899; amd64

### `eclipse-temurin:25_36-jre-windowsservercore-ltsc2025` - windows version 10.0.26100.6899; amd64

```console
$ docker pull eclipse-temurin@sha256:4824253dde88ba4b7c5109294c9f1775a4f4cb40f11183f41740497649da98e2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3321754593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43efcf2430e6b0c6bd1b2b8cad5b911254799b518186a02ff411311aeeb41d10`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 11 Oct 2025 16:27:11 GMT
RUN Install update 10.0.26100.6899
# Tue, 14 Oct 2025 20:43:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:52:02 GMT
ENV JAVA_VERSION=jdk-25+36
# Tue, 14 Oct 2025 20:52:16 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_x64_windows_hotspot_25_36.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_x64_windows_hotspot_25_36.msi ;     Write-Host ('Verifying sha256 (eeae2fb19dc8d778a324d9b5c879f7afe9732487516807b75584436b01e0d8c3) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'eeae2fb19dc8d778a324d9b5c879f7afe9732487516807b75584436b01e0d8c3') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-25' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 14 Oct 2025 20:52:21 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a050b25516334eac5bca074c4f4b42f39b3cf4be3d40626ee4f574c862e03e8b`  
		Last Modified: Tue, 14 Oct 2025 21:11:35 GMT  
		Size: 1.0 GB (1005173296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66c58e920e9f0915866ea63ab2aabb6407ed4c6b44b84a5318caf2ae3fb8608a`  
		Last Modified: Tue, 14 Oct 2025 20:51:42 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a724de46317003a725ea83e73db8ad923d2a749de1f3ac8b136b32b804bbd488`  
		Last Modified: Tue, 14 Oct 2025 20:52:42 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20c2b03d6eadba709a9d82fb3c166553f6e5e274fb8b1f178f1b2f5bbd3b0b7`  
		Last Modified: Tue, 14 Oct 2025 20:52:51 GMT  
		Size: 100.9 MB (100925532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ab0189b9b652554c4f81e7c8573d7c529b4509986ea4719d51ccb82c05d454`  
		Last Modified: Tue, 14 Oct 2025 20:52:42 GMT  
		Size: 346.0 KB (346006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
