## `eclipse-temurin:8u345-b01-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:ad0721c4d3dc5c8305ca843a0d0cc2f58ce8f71b5eb61c3712b4c669eb97a54b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1129; amd64

### `eclipse-temurin:8u345-b01-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.1129; amd64

```console
$ docker pull eclipse-temurin@sha256:76ff8568e284379dbe0bbcf8c00f368d525b258785ec425cfc00a2c240966494
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2487977124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575b55eb88a14eefab76016723b8efc5716777e21397dd2100e234e920b55310`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Fri, 07 Oct 2022 22:13:48 GMT
RUN Install update 10.0.20348.1129
# Tue, 11 Oct 2022 20:20:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 15:16:40 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Wed, 12 Oct 2022 15:22:15 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_windows_hotspot_8u345b01.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_windows_hotspot_8u345b01.msi ;     Write-Host ('Verifying sha256 (30253824132f22de22fef11242fc9cd7a183b5e09757bb57ad1d82c03d852a3c) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '30253824132f22de22fef11242fc9cd7a183b5e09757bb57ad1d82c03d852a3c') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Oct 2022 15:22:34 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7ab91661ce2a2a2c14684a2ba0f543a81d7896773f88200b31be0e37c589de38`  
		Size: 979.4 MB (979359717 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:15e15cecc9c7498ee7335091ed603347777bb2f7810e8b701327779faaae1712`  
		Last Modified: Tue, 11 Oct 2022 20:34:44 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d94fd3e6ff12ae44041574106003abbd18a384f23e9c75b39eb032dd7bd3d8a`  
		Last Modified: Wed, 12 Oct 2022 16:01:59 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b9948252ee70be25300320224a54cf7920a26aa3eeccc15392494a563e5418`  
		Last Modified: Wed, 12 Oct 2022 16:03:30 GMT  
		Size: 71.2 MB (71212788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee80059c5956e54e01d2a6ab9f3e1c42c362e357598f119631e7832e94e29fbf`  
		Last Modified: Wed, 12 Oct 2022 16:03:22 GMT  
		Size: 538.2 KB (538184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
