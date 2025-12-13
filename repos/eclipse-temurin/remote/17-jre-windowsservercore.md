## `eclipse-temurin:17-jre-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:d6dbd8e047d4aa198d0d6c6e49cdaadef3c309df9bdfb463633876eb67a64049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7462; amd64
	-	windows version 10.0.20348.4529; amd64

### `eclipse-temurin:17-jre-windowsservercore` - windows version 10.0.26100.7462; amd64

```console
$ docker pull eclipse-temurin@sha256:1ba84db312871654649ca2d9c2aab07d4f9dc5b826f79618826aba77ac3e6891
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3328580462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae038e068b234c3aa79e6a9df31f12c4e3713baa6592198cda3293774cd649de`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Dec 2025 21:49:56 GMT
RUN Install update 10.0.26100.7462
# Tue, 09 Dec 2025 20:37:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 20:37:37 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Tue, 09 Dec 2025 20:37:57 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_windows_hotspot_17.0.17_10.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_windows_hotspot_17.0.17_10.msi ;     Write-Host ('Verifying sha256 (23eea3080b9545915b5af64807fd310ee7227688a179b33859530912cca4c1e6) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '23eea3080b9545915b5af64807fd310ee7227688a179b33859530912cca4c1e6') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 09 Dec 2025 20:38:03 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
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
	-	`sha256:fda927c6cef6816dc1c8fd7866a5d520bfd29aa30ffd60afde0abadfe383bdb5`  
		Last Modified: Tue, 09 Dec 2025 20:46:22 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e731ff0ac83685a12732f1557ace4d524d902f0e4eefcf7bdf8176ffcb97d0b`  
		Last Modified: Tue, 09 Dec 2025 20:46:22 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874eaa3ca7087ecf9fc7947483eefd09f43b0b91fa04c74fc41fc239b2a32a91`  
		Last Modified: Tue, 09 Dec 2025 20:46:32 GMT  
		Size: 75.1 MB (75100562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743ab7a2ea2bec0482ce80e15f61a02bac63ba42d0ce3a6ac7cd657ae3d43f38`  
		Last Modified: Tue, 09 Dec 2025 20:46:23 GMT  
		Size: 356.9 KB (356897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jre-windowsservercore` - windows version 10.0.20348.4529; amd64

```console
$ docker pull eclipse-temurin@sha256:c4f50ebf6a06f29a87ca460a4f2cb4d15db5856a4f19828f680d9a2b879f30bb
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1855460975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef7f586d7aac49aa14ef34c85d32452d4938ab92d2d603c227ef380b5baa943`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Tue, 09 Dec 2025 20:32:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 20:40:50 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Tue, 09 Dec 2025 20:41:05 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_windows_hotspot_17.0.17_10.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_windows_hotspot_17.0.17_10.msi ;     Write-Host ('Verifying sha256 (23eea3080b9545915b5af64807fd310ee7227688a179b33859530912cca4c1e6) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '23eea3080b9545915b5af64807fd310ee7227688a179b33859530912cca4c1e6') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 09 Dec 2025 20:41:10 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
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
	-	`sha256:4337b0b452250939272a24a7d25392c5f6351fbf9da067a0d397cefbb4266c7a`  
		Last Modified: Tue, 09 Dec 2025 20:40:35 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a90b6ca61b240a43699990f50873ca5a5ab92712d6678486ad99b6c1dcc208`  
		Last Modified: Tue, 09 Dec 2025 20:41:29 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50d43c4764f9b9d5ba11b8b46b4590a1314833b1cc2bff11f4439b44b3faabd3`  
		Last Modified: Tue, 09 Dec 2025 20:41:44 GMT  
		Size: 75.2 MB (75227105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13165c1ce3b51e470d69975aa88948b5fd27e34e93bdcb909c98cce7472780e`  
		Last Modified: Tue, 09 Dec 2025 20:41:29 GMT  
		Size: 351.9 KB (351945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
