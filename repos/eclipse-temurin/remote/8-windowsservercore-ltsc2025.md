## `eclipse-temurin:8-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:af305248e098cde5b5eadac94bc209b72c232e843da4062b4fa2465938c9f9aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `eclipse-temurin:8-windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull eclipse-temurin@sha256:fd76d0ebeb7541fb809f384f41ed0c628026b7a8f6856a26ea239d372687b3dc
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2693839127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6afc766ceb5ecf15bf1861b42befeed6bded53796bff43fbab0f09c324bd0b50`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Wed, 22 Jan 2025 18:31:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 18:31:31 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Wed, 22 Jan 2025 18:31:52 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_windows_hotspot_8u432b06.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_windows_hotspot_8u432b06.msi ;     Write-Host ('Verifying sha256 (c9280205858928756374d930d4b539c59b1cb470425d2cf300b943c56efe4d86) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'c9280205858928756374d930d4b539c59b1cb470425d2cf300b943c56efe4d86') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 22 Jan 2025 18:32:01 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:422777209949288c76c37146a8ac6154ce803d3bd40a5fcbeebcf1806b6144a6`  
		Last Modified: Wed, 22 Jan 2025 18:32:05 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3a178498765ab7dc3c4e2b4bce0ca20cc1d898689b8dc9e73bbd701ea5b2d1`  
		Last Modified: Wed, 22 Jan 2025 18:32:05 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0161f5444a76f39fdc713f5d20a9714530a003235e1476a069515e1eeaf9bbfd`  
		Last Modified: Wed, 22 Jan 2025 18:32:16 GMT  
		Size: 193.2 MB (193159722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a0d071116326e58bba75a9488bdb8bce150a7fa879adc94e0ea46b04d86e76`  
		Last Modified: Wed, 22 Jan 2025 18:32:06 GMT  
		Size: 399.2 KB (399222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
