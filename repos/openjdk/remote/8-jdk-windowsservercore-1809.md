## `openjdk:8-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:2648d9dcde4dea3d6bc052470b618dfb3ecfd6f6a6c7b05d7421fe8cfe28f975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64

### `openjdk:8-jdk-windowsservercore-1809` - windows version 10.0.17763.1637; amd64

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
