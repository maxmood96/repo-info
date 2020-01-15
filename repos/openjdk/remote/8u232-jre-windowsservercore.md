## `openjdk:8u232-jre-windowsservercore`

```console
$ docker pull openjdk@sha256:c48808a4bad60cc4db302377f4dea92e0f53a14d4df2ef90ae71cda8b21314a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64
	-	windows version 10.0.14393.3443; amd64

### `openjdk:8u232-jre-windowsservercore` - windows version 10.0.17763.973; amd64

```console
$ docker pull openjdk@sha256:2ee82e986a4b190372a018db37268158573fa96d2db7d7aa1bca3bd44a47d61b
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2259522298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:addc0bd136855660a376c83e016ec48f9dc6ebecd4578fd9ad5c61635ccc0907`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 11 Jan 2020 05:23:25 GMT
RUN Install update 1809-amd64
# Tue, 14 Jan 2020 23:46:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jan 2020 01:30:46 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 15 Jan 2020 01:31:25 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Wed, 15 Jan 2020 01:31:27 GMT
ENV JAVA_VERSION=8u232
# Wed, 15 Jan 2020 01:38:59 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_
# Wed, 15 Jan 2020 01:39:01 GMT
ENV JAVA_URL_VERSION=8u232b09
# Wed, 15 Jan 2020 01:39:48 GMT
RUN $url = ('{0}x64_windows_{1}.zip' -f $env:JAVA_BASE_URL, $env:JAVA_URL_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  java -version'; java -version; 		Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edbd72df76b46e904108d2f61a63c295b3e3d8092dbd5a03bbeb2fb4d34a3e55`  
		Size: 682.7 MB (682725872 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9d323e253cb21832421dda4ec57dbd597bd4f934e62c162b9dec8b96e06e818`  
		Last Modified: Wed, 15 Jan 2020 01:45:20 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e2d444929b943c4f4f4a475d9f25066ceec820499bc85b52c37c87831991eb9`  
		Last Modified: Wed, 15 Jan 2020 02:14:23 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e259c6c6f5b6748db8b7b81e4971e961596c683c068a25172d53849081c1fee`  
		Last Modified: Wed, 15 Jan 2020 02:14:19 GMT  
		Size: 4.5 MB (4547040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620f62de05b81e7fca822b69da4d0bbd7c017f9344e1b54fafc054c4aca286cd`  
		Last Modified: Wed, 15 Jan 2020 02:14:18 GMT  
		Size: 1.2 KB (1205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af578367d26280a2f62cdc1f6304e5ab94ec3fd17f9241a96cb8ce5c87ee7467`  
		Last Modified: Wed, 15 Jan 2020 02:18:46 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79bef408c2039fef8a7f6c619f35287a17185a9c4808dc5d8c1cb74b46653e14`  
		Last Modified: Wed, 15 Jan 2020 02:18:46 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a774d86dd8af149baa5cd93e02b04f2d19578ed72b616ce5265999c7826e5efa`  
		Last Modified: Wed, 15 Jan 2020 02:18:54 GMT  
		Size: 37.6 MB (37558090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:8u232-jre-windowsservercore` - windows version 10.0.14393.3443; amd64

```console
$ docker pull openjdk@sha256:525635a103a579c7dc08205190c186022d18e60574765cec0598ff44c02a015c
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5772644242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf7c037e0310150b575395e13e8f524d649aa9e61a889b3a348ae2f1e49fb7cf`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 02 Jan 2020 15:48:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 14 Jan 2020 23:50:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jan 2020 01:33:20 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 15 Jan 2020 01:34:26 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Wed, 15 Jan 2020 01:34:27 GMT
ENV JAVA_VERSION=8u232
# Wed, 15 Jan 2020 01:40:08 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_
# Wed, 15 Jan 2020 01:40:10 GMT
ENV JAVA_URL_VERSION=8u232b09
# Wed, 15 Jan 2020 01:41:47 GMT
RUN $url = ('{0}x64_windows_{1}.zip' -f $env:JAVA_BASE_URL, $env:JAVA_URL_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  java -version'; java -version; 		Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:31f9df80631e7b5d379647ee7701ff50e009bd2c03b30a67a0a8e7bba4a26f94`  
		Size: 1.7 GB (1654613376 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f1c8c4c99f36cfcf87884a9382011e93fb05fa4002d8f4eca62a43e744db8e95`  
		Last Modified: Wed, 15 Jan 2020 01:46:47 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64342381c3078746d49b0bd22acdcb54c6ed79741d2dc83408852dbc0f261239`  
		Last Modified: Wed, 15 Jan 2020 02:15:22 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc1b90544f2b8fdcf67d90077c3afe669dd4c0e5cd3913aaa2cce71f0b3e8b1b`  
		Last Modified: Wed, 15 Jan 2020 02:15:21 GMT  
		Size: 5.4 MB (5385785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1fc87cd565ccf7651561eb8a9be23e1c04423befef0ee53654f99f979945018`  
		Last Modified: Wed, 15 Jan 2020 02:15:19 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:940e0f74af044c107b66feda19bed37cc958eb7c32ab9936ba43ba100f2f255c`  
		Last Modified: Wed, 15 Jan 2020 02:19:18 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d961d1ec48fe2c4603d275c33b1fac25d6b7cb83f054e6c4a5dadf1b517973c`  
		Last Modified: Wed, 15 Jan 2020 02:19:18 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f731c5b461b204f48ad4eb6e7eaa00176f8e59da96635e22622bf0c17959790`  
		Last Modified: Wed, 15 Jan 2020 02:19:26 GMT  
		Size: 42.7 MB (42653165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
