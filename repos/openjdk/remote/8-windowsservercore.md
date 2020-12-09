## `openjdk:8-windowsservercore`

```console
$ docker pull openjdk@sha256:c6e1b3a0f2ef4c3bd0403f218ab161027774ac5c1cccdd2aa875168126810151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64
	-	windows version 10.0.14393.4104; amd64

### `openjdk:8-windowsservercore` - windows version 10.0.17763.1637; amd64

```console
$ docker pull openjdk@sha256:077167ddf433c1f9fe17fb94e586aa2851fce45db686c6205acb2f1332fd1bd8
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2505775594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0aa3b114d48fe1280307dc0ea3e220c1fd0a0586eb2db8cb4da9ae43ac12b02`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 04 Dec 2020 02:13:01 GMT
RUN Install update 1809-amd64
# Wed, 09 Dec 2020 13:30:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Dec 2020 19:18:49 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 09 Dec 2020 19:19:28 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Wed, 09 Dec 2020 19:19:29 GMT
ENV JAVA_VERSION=8u275
# Wed, 09 Dec 2020 19:19:30 GMT
ENV JAVA_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jdk_x64_windows_8u275b01.zip
# Wed, 09 Dec 2020 19:20:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac -version'; javac -version; 	Write-Host '  java -version'; java -version; 		Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:aa4f58cd6da1aaf1a0b44d443bd88e7fbe5b0a6f193995a1a61d6bd63990f314`  
		Size: 672.5 MB (672541583 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a4372d14958dc8a7eaaace9e4774e7f1db524da5eb4474b5e46738848a3a61a5`  
		Last Modified: Wed, 09 Dec 2020 13:54:38 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac4b1e24729915954012340ecb4cb170d576ae556ff3c0cff8fd4d986b04d88`  
		Last Modified: Wed, 09 Dec 2020 19:47:29 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff422a5acc25debf8fae6ecb9fa59b2917f9dac8a90dde3d8ced3e1829463a7`  
		Last Modified: Wed, 09 Dec 2020 19:47:31 GMT  
		Size: 9.2 MB (9235279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b65ede68f3b1b272e0e54f6dcad8b65b2e4e26141aa59f8ae6087e391ec61bb`  
		Last Modified: Wed, 09 Dec 2020 19:47:28 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf837f8597e8da129e8715c58425042638ba315d0c09a6441c01b7603f62d6b`  
		Last Modified: Wed, 09 Dec 2020 19:47:29 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6261a582311d24fe3e07a4711dcd6e8651d2d255e15850e492cf049cb0ff32d3`  
		Last Modified: Wed, 09 Dec 2020 19:47:42 GMT  
		Size: 105.7 MB (105661309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:8-windowsservercore` - windows version 10.0.14393.4104; amd64

```console
$ docker pull openjdk@sha256:79b19ae66f8df83989235587d17cd70c6711b93c7a7b6a628c0a3636a83fe87c
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5889892999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:665cb1650f1f2713eb651c869ed0f5ddb01d09a0f5ba82d97066f3d4b163a622`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 02 Dec 2020 17:42:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Dec 2020 13:34:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Dec 2020 19:20:45 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 09 Dec 2020 19:22:01 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Wed, 09 Dec 2020 19:22:03 GMT
ENV JAVA_VERSION=8u275
# Wed, 09 Dec 2020 19:22:04 GMT
ENV JAVA_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jdk_x64_windows_8u275b01.zip
# Wed, 09 Dec 2020 19:24:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac -version'; javac -version; 	Write-Host '  java -version'; java -version; 		Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d2696dc2a40dc121fc5acaa02242817ac416c69d17c113e2ac5136d21a3942d8`  
		Size: 1.7 GB (1698858125 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c6d005eb9e78ad42f77f3dad7e29d954e78f0547f9884fe024a71f4042412970`  
		Last Modified: Wed, 09 Dec 2020 13:55:31 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9751a5061235368009ebce52c059fcc925d581fb5ec946aed8ba61812fd8b80`  
		Last Modified: Wed, 09 Dec 2020 19:48:02 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c721000783e08dda85eff6f46731ef68c4f8670118194d010a3309bf1912844`  
		Last Modified: Wed, 09 Dec 2020 19:48:05 GMT  
		Size: 10.0 MB (10038993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a2f3258330823823b5f5d87dcd764608a53081a6f9633fb83143b773ca9916`  
		Last Modified: Wed, 09 Dec 2020 19:48:02 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834c4bcc4e69470844702c4e6f4a7163c0bebccbfd1322b07d903b4270eceef2`  
		Last Modified: Wed, 09 Dec 2020 19:48:02 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75857d3580e8d5206e627e901d93532dde9060be200b02d73b8061d7a63f873b`  
		Last Modified: Wed, 09 Dec 2020 19:48:15 GMT  
		Size: 111.0 MB (111005355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
