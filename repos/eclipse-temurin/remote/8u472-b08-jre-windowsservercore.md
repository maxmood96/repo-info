## `eclipse-temurin:8u472-b08-jre-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:37af7503bdbacf7983c0930e6396f55c93f8f9e2a4cc3a8788567e3ba66b0371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7462; amd64
	-	windows version 10.0.20348.4529; amd64

### `eclipse-temurin:8u472-b08-jre-windowsservercore` - windows version 10.0.26100.7462; amd64

```console
$ docker pull eclipse-temurin@sha256:da5bd5a507ad38c4a216200c453abab0a30d728c0557bdd28ef3b9d76f7b246f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3326167154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:070f01d4710ddec100663a3ae4e7d23947e61c452e54136797f7143a33453502`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Dec 2025 21:49:56 GMT
RUN Install update 10.0.26100.7462
# Tue, 09 Dec 2025 20:35:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 20:35:54 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Tue, 09 Dec 2025 20:36:23 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_windows_hotspot_8u472b08.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_windows_hotspot_8u472b08.msi ;     Write-Host ('Verifying sha256 (2099c63f97bab0dea8c70fb2f32a7a8a2ad8e53167f0523f42c8f62d03bcc66a) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '2099c63f97bab0dea8c70fb2f32a7a8a2ad8e53167f0523f42c8f62d03bcc66a') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 09 Dec 2025 20:36:28 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
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
	-	`sha256:662b1308053cacb291cd58b29a82f4ad20d6a19f07b45fabb48f69751e7dd073`  
		Last Modified: Tue, 09 Dec 2025 20:46:21 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd6e7e5f654c56f00a7d0197e22b89f7cceb511cbc1e68b97cdca3ef9594a28`  
		Last Modified: Tue, 09 Dec 2025 20:46:21 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dddf86b13405ca559e64516e58a45a7231a3e5401a974df727ff888e251931a`  
		Last Modified: Tue, 09 Dec 2025 20:46:31 GMT  
		Size: 72.7 MB (72674111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b29305fad2240a99702c3ce2f5beefccf689005603c7533e5b8478adc434359`  
		Last Modified: Tue, 09 Dec 2025 20:46:22 GMT  
		Size: 370.0 KB (370020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u472-b08-jre-windowsservercore` - windows version 10.0.20348.4529; amd64

```console
$ docker pull eclipse-temurin@sha256:fb2f70505d29f26d110c2158decd89f322fd23086be4e9773ce32572ff662a64
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1853010760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e1b1a192914ccc231cf18f57a4f97567f8c83d5014d6b7b7ce56cf6bb06e42c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Tue, 09 Dec 2025 20:40:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 20:40:19 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Tue, 09 Dec 2025 20:40:39 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_windows_hotspot_8u472b08.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_windows_hotspot_8u472b08.msi ;     Write-Host ('Verifying sha256 (2099c63f97bab0dea8c70fb2f32a7a8a2ad8e53167f0523f42c8f62d03bcc66a) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '2099c63f97bab0dea8c70fb2f32a7a8a2ad8e53167f0523f42c8f62d03bcc66a') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 09 Dec 2025 20:40:46 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
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
	-	`sha256:8168617ee10fc15e3adb5c56ebdabfa52e263ba4a71565a1bb5e5a80bf05dad0`  
		Last Modified: Tue, 09 Dec 2025 20:41:03 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20b882a031007f2dd09c85bad23b41a04ffe45e8472e835bf04b414f52dd77a`  
		Last Modified: Tue, 09 Dec 2025 20:41:03 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9fc6ea395bfe7452c9396d85f64535f50a20b45a87d13ba857612f7e559977`  
		Last Modified: Tue, 09 Dec 2025 20:41:16 GMT  
		Size: 72.8 MB (72778226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87bf64851f2d451311ecf9fd365a7d223f5198f1e816f4080fa6116d2e78dc9e`  
		Last Modified: Tue, 09 Dec 2025 20:41:03 GMT  
		Size: 350.6 KB (350627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
