## `eclipse-temurin:8u372-b07-jdk-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:022317223dd61d7a7d0b09b61bf842821e939812b6fe853bbe42dc90d6132966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4645; amd64

### `eclipse-temurin:8u372-b07-jdk-windowsservercore-1809` - windows version 10.0.17763.4645; amd64

```console
$ docker pull eclipse-temurin@sha256:dec2366c7197a673c7a423ceedb370328a08e4d54943cb82a45a61782d59bfed
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2131115428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86617c8ec49aaf04814e6b044e3d1f85f4a9b635f3c5e7ea8c6d1f48e3a3cef`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jul 2023 08:17:39 GMT
RUN Install update 10.0.17763.4645
# Thu, 13 Jul 2023 20:32:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Jul 2023 21:34:03 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 13 Jul 2023 21:35:26 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_windows_hotspot_8u372b07.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_windows_hotspot_8u372b07.msi ;     Write-Host ('Verifying sha256 (e75a4e4a70d0fb5c0f1ca4855cb2a7f3c9ccb3d5dea5af0f45d4608a563c45b8) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'e75a4e4a70d0fb5c0f1ca4855cb2a7f3c9ccb3d5dea5af0f45d4608a563c45b8') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 13 Jul 2023 21:36:23 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36dba1ee29cd36713c8785a5de7dd2a487244d734ed4c5e7b0a6890bffb806e`  
		Last Modified: Tue, 11 Jul 2023 18:27:38 GMT  
		Size: 289.1 MB (289068746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e991bb72ebb8bf12a5cb5fcb2075d938e3508db6634bdfe6a5bb73e4c612051`  
		Last Modified: Thu, 13 Jul 2023 21:08:51 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8730ed1a3e68aa1e2a0000134c988fdca6aa2c088ff4b4aa222e896db496f041`  
		Last Modified: Thu, 13 Jul 2023 22:18:36 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e45a7c29a38b2df71caa412556c8f87ac8c7b8ea7947bf13a68c9c560d6360f`  
		Last Modified: Thu, 13 Jul 2023 22:18:52 GMT  
		Size: 191.2 MB (191220416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309ad8a066de9f7a241905ace880d39d10981d39a51d442470c11dfb855f564e`  
		Last Modified: Thu, 13 Jul 2023 22:18:37 GMT  
		Size: 203.1 KB (203145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
