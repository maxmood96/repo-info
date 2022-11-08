## `eclipse-temurin:19-jdk-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:9b1643a1f034db8d26f72906ed0ca8ea0029628ef15153686d2d45c0dfc3138e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1249; amd64
	-	windows version 10.0.17763.3650; amd64

### `eclipse-temurin:19-jdk-windowsservercore` - windows version 10.0.20348.1249; amd64

```console
$ docker pull eclipse-temurin@sha256:623bf1540023b7f34ea31b97f6358e5a311add84a7e1f5d729040afb0a3e93d7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2849233604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a90b6372d0af8ccb1ea13c565d6985b55ef6b2f026df6ea693ed5290faaefbd`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Sat, 05 Nov 2022 07:49:25 GMT
RUN Install update 10.0.20348.1249
# Tue, 08 Nov 2022 18:28:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 08 Nov 2022 19:12:11 GMT
ENV JAVA_VERSION=jdk-19.0.1+10
# Tue, 08 Nov 2022 19:13:41 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jdk_x64_windows_hotspot_19.0.1_10.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jdk_x64_windows_hotspot_19.0.1_10.msi ;     Write-Host ('Verifying sha256 (d4e742c37e645f4b1fa40734df75949ae0ecd5cd946f8dac241d58924a63e787) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'd4e742c37e645f4b1fa40734df75949ae0ecd5cd946f8dac241d58924a63e787') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-19' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 08 Nov 2022 19:14:55 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 08 Nov 2022 19:14:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a4aee932fccc1ec8135f290aca03a7c93dcc2536fc84723813ef9b95f6fd13ea`  
		Last Modified: Wed, 18 May 2022 07:59:24 GMT  
		Size: 1.5 GB (1473997635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e276673195ed11807395b0da51ac20ef31c925ce955c29ad1bab54f14617c25b`  
		Last Modified: Tue, 08 Nov 2022 19:41:53 GMT  
		Size: 1.0 GB (1007770983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3becc14271944025e3fa6c2ef2689bdfbf09bfc54ec339115d3082df315898e4`  
		Last Modified: Tue, 08 Nov 2022 19:38:57 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:475fd7723281328e1b6805eca57c06af8c864c1bfc567d6e528f0dd9627a02f0`  
		Last Modified: Tue, 08 Nov 2022 19:54:07 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce94597b11d8425ed95936c5baa5550aca10c5e95ae565ae067245c1d882ab3`  
		Last Modified: Tue, 08 Nov 2022 19:54:41 GMT  
		Size: 366.9 MB (366901621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bba63ccbfc3706dd60fae1c4e19eadeefdf4b3adbfc120b1fd5976127462a6a`  
		Last Modified: Tue, 08 Nov 2022 19:54:07 GMT  
		Size: 559.1 KB (559125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e109d33259fc100bdec6f7a8ba102eb662addfccc78dccf68c6a183a3ab4df1`  
		Last Modified: Tue, 08 Nov 2022 19:54:07 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:19-jdk-windowsservercore` - windows version 10.0.17763.3650; amd64

```console
$ docker pull eclipse-temurin@sha256:3132aece663d8fc7f7ddf3a8944125f3ca81a5f44cd454b5e681bf70903d3196
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3149243013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121993198ed50209a1cfdd1dd6562b8a1ee0a2cfd0e7359aa1d467e6af08fc63`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 05 Nov 2022 18:29:26 GMT
RUN Install update 10.0.17763.3650
# Tue, 08 Nov 2022 18:31:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 08 Nov 2022 19:15:10 GMT
ENV JAVA_VERSION=jdk-19.0.1+10
# Tue, 08 Nov 2022 19:17:47 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jdk_x64_windows_hotspot_19.0.1_10.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jdk_x64_windows_hotspot_19.0.1_10.msi ;     Write-Host ('Verifying sha256 (d4e742c37e645f4b1fa40734df75949ae0ecd5cd946f8dac241d58924a63e787) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'd4e742c37e645f4b1fa40734df75949ae0ecd5cd946f8dac241d58924a63e787') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-19' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 08 Nov 2022 19:19:40 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 08 Nov 2022 19:19:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26cc6e4f9eb1ae415a5ead6f884cac597bbd57efa6cd042c878d5b54c9d2091`  
		Last Modified: Tue, 08 Nov 2022 19:44:35 GMT  
		Size: 854.3 MB (854317461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f182832ad6ad5ea3d4b7320fd7bfea56fb9cf8413be904e52db6ed14c8d9e36f`  
		Last Modified: Tue, 08 Nov 2022 19:42:07 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e985ddaf32ace65d0eff12e6fb243efc3c2b42ed4459033b28e53418912e17`  
		Last Modified: Tue, 08 Nov 2022 19:54:55 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b68408c21523feb15a7391eedd7fb543afe1b03e0fe771fad4274ee5e0249f`  
		Last Modified: Tue, 08 Nov 2022 19:55:28 GMT  
		Size: 366.7 MB (366692809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1811741f71339a0ee857a05d26b32bc47086995ff5d2fef23813580ac8cc890e`  
		Last Modified: Tue, 08 Nov 2022 19:54:56 GMT  
		Size: 4.0 MB (3959082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6091502121b9e2613866c0c7ad187824aa83c76469bfbe837feb06919a2dcaf7`  
		Last Modified: Tue, 08 Nov 2022 19:54:55 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
