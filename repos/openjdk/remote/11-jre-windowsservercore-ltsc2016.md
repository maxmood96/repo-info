## `openjdk:11-jre-windowsservercore-ltsc2016`

```console
$ docker pull openjdk@sha256:f1ed585b67b930b35487fd6007392b4110ca9d05ada4ba06f4d2c5800bddf461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3384; amd64

### `openjdk:11-jre-windowsservercore-ltsc2016` - windows version 10.0.14393.3384; amd64

```console
$ docker pull openjdk@sha256:e15159b7f3456ffcf22544c8e2e9766213fa09074579d4f49611aeaf63d46a90
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5772478341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec1731ed24fad75e24f55e0b23e0021444b2bbc516be39d858e571ae75bd277e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 00:35:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2019 19:04:54 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 11 Dec 2019 19:06:08 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Wed, 11 Dec 2019 19:06:10 GMT
ENV JAVA_VERSION=11.0.5
# Wed, 11 Dec 2019 19:12:25 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jre_
# Wed, 11 Dec 2019 19:12:26 GMT
ENV JAVA_URL_VERSION=11.0.5_10
# Wed, 11 Dec 2019 19:14:08 GMT
RUN $url = ('{0}x64_windows_{1}.zip' -f $env:JAVA_BASE_URL, $env:JAVA_URL_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
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
	-	`sha256:8fa4ef335f1b1565604d41801b905e6994e1469c953db542d16d71ae2e3f0049`  
		Last Modified: Wed, 11 Dec 2019 20:08:52 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5776facb75e87a0700c8d90e51078c19b31f028bb99eaef60ca68bc0a27036d3`  
		Last Modified: Wed, 11 Dec 2019 20:08:55 GMT  
		Size: 5.4 MB (5367077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c25542212d761cacae600dcaf408b08a49e4bed9006d3237f81ef879d2b38bc8`  
		Last Modified: Wed, 11 Dec 2019 20:08:50 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b361b5bdc68c7ae0dbe77e3d1ef41afe70fd7fec6f013d09e5e5bafca8eb357a`  
		Last Modified: Wed, 11 Dec 2019 20:12:09 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d918517c3c037c8305cc91514a65ec29b6fb4f9adf349169b3839cfdd81b275`  
		Last Modified: Wed, 11 Dec 2019 20:12:09 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d2e7020cc97f0a001edf01b864905cd2e3fa5e1a6145e504745eba0ff03aa6e`  
		Last Modified: Wed, 11 Dec 2019 20:12:19 GMT  
		Size: 44.4 MB (44401429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
