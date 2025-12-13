## `eclipse-temurin:11-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:545aa5e27771da94d559098b43822cff5746745cfacc3a0d27adbf277269c9b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7462; amd64
	-	windows version 10.0.20348.4529; amd64

### `eclipse-temurin:11-windowsservercore` - windows version 10.0.26100.7462; amd64

```console
$ docker pull eclipse-temurin@sha256:c710cdbd23a1e8f54a1ab8631662cb31886a51c13c8661cb5e3d742e2db29bb3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3622917887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde96c386d39578a1efe8c8e54ecf2c01b84099c09cc95e19eda7e1954da388a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Dec 2025 21:49:56 GMT
RUN Install update 10.0.26100.7462
# Tue, 09 Dec 2025 20:36:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 20:36:03 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Tue, 09 Dec 2025 20:36:36 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_windows_hotspot_11.0.29_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_windows_hotspot_11.0.29_7.msi ;     Write-Host ('Verifying sha256 (219e88a862ccdde521c42d8ebc001cc711279cdef79157b568ec2ae16b3abde0) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '219e88a862ccdde521c42d8ebc001cc711279cdef79157b568ec2ae16b3abde0') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 09 Dec 2025 20:36:43 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 09 Dec 2025 20:36:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Mon, 08 Dec 2025 10:02:12 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890b21ccebaeedf053c6c32fb4fe8d98ab2c60496b12e6b730ac67df9096fc5b`  
		Last Modified: Tue, 09 Dec 2025 19:44:14 GMT  
		Size: 1.0 GB (1037813290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc4dc9da92e440fd16269231217a19ad7ee04e301094f4689f5eddb0f2bde81`  
		Last Modified: Tue, 09 Dec 2025 20:46:24 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa20b997df915cfb38e94d9707c9ada4a6ad6f07f2c4b82f00da3ab6ac59a5fc`  
		Last Modified: Tue, 09 Dec 2025 20:46:24 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b390207f9dc910d653fa9a4d37d1a6147b164672e1cdbf8c67098be2e7fa8e7`  
		Last Modified: Tue, 09 Dec 2025 20:46:56 GMT  
		Size: 369.4 MB (369441097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6083bd6deb3eb1dbcdcb7818b73a2a709c6946844c47cf308bed94c0a09b99ee`  
		Last Modified: Tue, 09 Dec 2025 20:46:24 GMT  
		Size: 352.5 KB (352462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb5f6a94bed522c2c7ee314eea202fddcbab2496eccc6ae465ac0448f850460`  
		Last Modified: Tue, 09 Dec 2025 20:46:24 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-windowsservercore` - windows version 10.0.20348.4529; amd64

```console
$ docker pull eclipse-temurin@sha256:6f984b050dbdac4d4794ba456518af4140119ab6ec3eeb05abb7c1a9e5e840c2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2149815271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b51b72529098692a4cfe1de9f55fc6838c6c49b0d6fa26f717994efc14d017ff`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Tue, 09 Dec 2025 20:40:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 20:40:26 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Tue, 09 Dec 2025 20:41:17 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_windows_hotspot_11.0.29_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_windows_hotspot_11.0.29_7.msi ;     Write-Host ('Verifying sha256 (219e88a862ccdde521c42d8ebc001cc711279cdef79157b568ec2ae16b3abde0) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '219e88a862ccdde521c42d8ebc001cc711279cdef79157b568ec2ae16b3abde0') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 09 Dec 2025 20:41:26 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 09 Dec 2025 20:41:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:323d6571ea86abd0158f636013b118b7f30b9fdb6aa70348177419fb48c2c825`  
		Last Modified: Tue, 09 Dec 2025 20:41:56 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9503a1bccb896eedd3c101fa00c7ba8b55af8d7ac721ca41a22c9e45030d1035`  
		Last Modified: Tue, 09 Dec 2025 20:41:56 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d113aa7bd46f2ac9043b67da48121211323d1952aedab2880f84ce208b3c877`  
		Last Modified: Tue, 09 Dec 2025 20:42:05 GMT  
		Size: 369.6 MB (369578571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:796a774aba8d46fca32891181b413ec8c11f1e2b0aeec23dad60b51de9571078`  
		Last Modified: Tue, 09 Dec 2025 20:41:56 GMT  
		Size: 353.5 KB (353506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a615e9e472b2d9fe9d46aab8dba7db171354d7dec707af481e922ef2161f07e3`  
		Last Modified: Tue, 09 Dec 2025 20:41:56 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
