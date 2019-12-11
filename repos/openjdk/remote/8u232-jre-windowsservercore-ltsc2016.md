## `openjdk:8u232-jre-windowsservercore-ltsc2016`

```console
$ docker pull openjdk@sha256:b501a50e4733694666eaa592fd0a8a96a6983781b0c0e0fe740481daf9f5ca66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3384; amd64

### `openjdk:8u232-jre-windowsservercore-ltsc2016` - windows version 10.0.14393.3384; amd64

```console
$ docker pull openjdk@sha256:53b936e034fdc20f91131b17ccdb71e5cf8fc0dee21bf2bfa39246b4c407ecb1
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5770707155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17905356066de71995bd1a106e8be9a8f51eaf8ecd2b3e0c03dd72ed5a0efb7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 00:35:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2019 19:17:15 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 11 Dec 2019 19:18:19 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Wed, 11 Dec 2019 19:18:21 GMT
ENV JAVA_VERSION=8u232
# Wed, 11 Dec 2019 19:53:50 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_
# Wed, 11 Dec 2019 19:53:51 GMT
ENV JAVA_URL_VERSION=8u232b09
# Wed, 11 Dec 2019 19:55:26 GMT
RUN $url = ('{0}x64_windows_{1}.zip' -f $env:JAVA_BASE_URL, $env:JAVA_URL_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  java -version'; java -version; 		Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:530e4240d4261ce165890648d1df6230dc4f9ce5df2e6cf9f0d5876694c3d4f0`  
		Last Modified: Wed, 11 Dec 2019 01:14:39 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f320b58c538ea7ebfbf9d0ed9f8997b8f6719267fa573146aa5bc7efcc323ecf`  
		Last Modified: Wed, 11 Dec 2019 20:14:18 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2806dc04a2c60cb7c7f90855aa0101d3a3aa1f1229e46672d676b5344a879b9`  
		Last Modified: Wed, 11 Dec 2019 20:14:17 GMT  
		Size: 5.4 MB (5362306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7bce14919ce58880d93f314b7803ad17dc096774801dd5df0db2e407d7928a`  
		Last Modified: Wed, 11 Dec 2019 20:14:15 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fadc217751f87deb7052768236eb2f48bb3932199c0ef169bdca620496d7fef`  
		Last Modified: Wed, 11 Dec 2019 20:16:36 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac01ad6a2b730db3985cfec3e90f2614933e61bfed7864b12b88ce541d6a0b34`  
		Last Modified: Wed, 11 Dec 2019 20:16:37 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:717e0a28b0366da71707871a940d525ed4296b5edf33238406831d2163e5aa15`  
		Last Modified: Wed, 11 Dec 2019 20:16:45 GMT  
		Size: 42.6 MB (42634984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
