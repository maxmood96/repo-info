## `openjdk:8-jre-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:a1632b5db2e1770afdf7d78dce249d892696fd8a0b7f062dca4a03ea7616c5b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64

### `openjdk:8-jre-windowsservercore-1809` - windows version 10.0.17763.1518; amd64

```console
$ docker pull openjdk@sha256:9d369d03d0aef3a9e9345f92d3677b7425aa120491bb889cfb1fe7ba45c13e6f
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2425450499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73699cf8bbab30f71a4ae5444db0c97ee830dc06590c328151d8429c9c6876d5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 01 Oct 2020 02:26:38 GMT
RUN Install update 1809-amd64
# Wed, 14 Oct 2020 12:27:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 18:14:23 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 14 Oct 2020 18:15:00 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Wed, 14 Oct 2020 18:15:01 GMT
ENV JAVA_VERSION=8u265
# Wed, 14 Oct 2020 18:21:00 GMT
ENV JAVA_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_windows_8u265b01.zip
# Wed, 14 Oct 2020 18:21:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  java -version'; java -version; 		Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:406ffb8432a757e84f7594e85c676620dec6955e0475ac271aa4dd5c0531190d`  
		Size: 655.8 MB (655757265 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5e61fff845eda39f31bdf5d797254fdf656ee79d8c294c1713007864bc4c2535`  
		Last Modified: Wed, 14 Oct 2020 12:50:32 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423e6d8e8bc166e44e75a7429a9d4337b7f187f5087a11a1ffa628b9d5c9fa3f`  
		Last Modified: Wed, 14 Oct 2020 18:50:47 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955986b14a9eba01fe3b415706ff08c9b8d356c2c46b6100a3bc762273d0ecb7`  
		Last Modified: Wed, 14 Oct 2020 18:50:50 GMT  
		Size: 9.2 MB (9229481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7870b534496b92d96b751a60834211c34c8df847220e6e439f9e153ae5d7c8eb`  
		Last Modified: Wed, 14 Oct 2020 18:50:48 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2015db906b3b1a644dabfbe1c3e0f8e294e2de9e9261935afdf5edc5fcbf1165`  
		Last Modified: Wed, 14 Oct 2020 18:54:14 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fca04f462eb5a313719f99f279b1ca571b91453820718ef768d164924ab70c0`  
		Last Modified: Wed, 14 Oct 2020 18:54:21 GMT  
		Size: 42.1 MB (42126338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
