## `openjdk:8u265-windowsservercore`

```console
$ docker pull openjdk@sha256:0b2295f33c40f33bd148a23969cfe32a0bb297a5b1a2885f8e1578498ee8ee6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64
	-	windows version 10.0.14393.3986; amd64

### `openjdk:8u265-windowsservercore` - windows version 10.0.17763.1518; amd64

```console
$ docker pull openjdk@sha256:9bc844747ff9dbcc0430fa1bd441ad2537a8bfd5ba9e8d86694092ae6c69e4da
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2488165167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c82ed09aa82efe1ebdf146517d746f8637bc5996d7415f8eb3bedd85198821e1`
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
# Wed, 14 Oct 2020 18:15:02 GMT
ENV JAVA_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jdk_x64_windows_8u265b01.zip
# Wed, 14 Oct 2020 18:16:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac -version'; javac -version; 	Write-Host '  java -version'; java -version; 		Write-Host 'Complete.'
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
	-	`sha256:59ac9f9aa25bd9b4b8d5b779a57e6835de607c47035d11fcea2d87aa14a050d7`  
		Last Modified: Wed, 14 Oct 2020 18:50:47 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d44758530654f5e2791541381a9f8440f25c8a618f116ce97708519373c14a11`  
		Last Modified: Wed, 14 Oct 2020 18:51:02 GMT  
		Size: 104.8 MB (104840962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:8u265-windowsservercore` - windows version 10.0.14393.3986; amd64

```console
$ docker pull openjdk@sha256:6ca59a93d2ba2ced480c7f70f8f2a3a819577b9128798a9fc1c829ba503d49e3
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5861288816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e4a5980ce9e84b3ec6647874a3ac2f45e4eab6bad287c753c2e29670301de18`
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
# Wed, 14 Oct 2020 18:17:37 GMT
ENV JAVA_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jdk_x64_windows_8u265b01.zip
# Wed, 14 Oct 2020 18:19:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac -version'; javac -version; 	Write-Host '  java -version'; java -version; 		Write-Host 'Complete.'
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
	-	`sha256:08220b508c237bc69db8562b892d5a8af7cea1e4a1456031bcc3301105ddbbf0`  
		Last Modified: Wed, 14 Oct 2020 18:51:23 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014718f15400c24a98d156565b46e0f8313ed29701d32045368cdc930c06e5de`  
		Last Modified: Wed, 14 Oct 2020 18:51:42 GMT  
		Size: 110.0 MB (110017201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
