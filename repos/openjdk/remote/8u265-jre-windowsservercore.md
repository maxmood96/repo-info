## `openjdk:8u265-jre-windowsservercore`

```console
$ docker pull openjdk@sha256:8f92ec7323479578254c585fb650bddec16efcd5bebdff391a4480f120b69105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64
	-	windows version 10.0.14393.3986; amd64

### `openjdk:8u265-jre-windowsservercore` - windows version 10.0.17763.1518; amd64

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

### `openjdk:8u265-jre-windowsservercore` - windows version 10.0.14393.3986; amd64

```console
$ docker pull openjdk@sha256:098a9fd7e13c9b7d3e5a1c84d6d7a99bc3553457e02a203d8b42e01067cc40cd
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5798562494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbfabdb61055c49a3fa534c64764344f463511e20759fae70bd70fe2879b3616`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 02 Oct 2020 17:07:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Oct 2020 12:31:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 18:16:20 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 14 Oct 2020 18:17:35 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Wed, 14 Oct 2020 18:17:36 GMT
ENV JAVA_VERSION=8u265
# Wed, 14 Oct 2020 18:21:51 GMT
ENV JAVA_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_windows_8u265b01.zip
# Wed, 14 Oct 2020 18:23:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  java -version'; java -version; 		Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:17a32268498b2feefa5457f0423ac15473596d514e48c694ef54d740a9a5067d`  
		Size: 1.7 GB (1671365753 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e300a13db0fbbf48a676ace9db3b0de292c825dfa01e6d82979d96ebc23d3675`  
		Last Modified: Wed, 14 Oct 2020 12:51:34 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cffa1e768304d56e30305c9ac557468df987effb01142b8bffef4c43698d8707`  
		Last Modified: Wed, 14 Oct 2020 18:51:23 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5135402b2d35127448acb3ec865346d17536f47e5ed865a0b400e6d93d0a9b7e`  
		Last Modified: Wed, 14 Oct 2020 18:51:26 GMT  
		Size: 9.9 MB (9915365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcee61f33ae775b68099ccb97829873903a919d6a873df3d6bf1e0345c03d200`  
		Last Modified: Wed, 14 Oct 2020 18:51:24 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:204a3597d0fa4e60dd9451932896f3096e0a934d4b577e160afcb0ee1a7c3d04`  
		Last Modified: Wed, 14 Oct 2020 18:54:36 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f6603493a57cef7017ac38d9438585f146ed7c027cd6962908246f6624cf3df`  
		Last Modified: Wed, 14 Oct 2020 18:54:44 GMT  
		Size: 47.3 MB (47290888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
