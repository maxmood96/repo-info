## `openjdk:8-windowsservercore-ltsc2016`

```console
$ docker pull openjdk@sha256:b60ade6fbaa27ff6dcd1d8fb8e88f9e75c5a1702d279d30dbf8c20516bd056e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3384; amd64

### `openjdk:8-windowsservercore-ltsc2016` - windows version 10.0.14393.3384; amd64

```console
$ docker pull openjdk@sha256:4df5134b75b5405528784c40b1ea5c780c8f79f1c91217a15d620752bb0c5fa9
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5832881437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ad5d82ab03b391965b2bbe98c070eb6c685f72859184ff804a19a13f5e1c732`
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
# Wed, 11 Dec 2019 19:18:23 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_
# Wed, 11 Dec 2019 19:18:24 GMT
ENV JAVA_URL_VERSION=8u232b09
# Wed, 11 Dec 2019 19:20:36 GMT
RUN $url = ('{0}x64_windows_{1}.zip' -f $env:JAVA_BASE_URL, $env:JAVA_URL_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac -version'; javac -version; 	Write-Host '  java -version'; java -version; 		Write-Host 'Complete.'
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
	-	`sha256:1201db30b34ed07c651f279719c1227af94009b41cd2d7a0adc43f4f8337d9be`  
		Last Modified: Wed, 11 Dec 2019 20:14:16 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e97430f9c7e0348fc852da4d7accf7b522a466ed20acc9f495514f80831378`  
		Last Modified: Wed, 11 Dec 2019 20:14:15 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5adaa735cda5721bbdb0332b0423f76fcf1655e459319cbf8e321a0daac0280`  
		Last Modified: Wed, 11 Dec 2019 20:14:33 GMT  
		Size: 104.8 MB (104809242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
