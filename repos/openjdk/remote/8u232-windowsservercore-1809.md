## `openjdk:8u232-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:02134c81a59c044e38d237da6a6fe580aa494ef9285942372dbc27ce91590871
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.914; amd64

### `openjdk:8u232-windowsservercore-1809` - windows version 10.0.17763.914; amd64

```console
$ docker pull openjdk@sha256:a604455d897227c0d463c565ad404635356745cecb1f08f21f232a6175750cc1
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2320650565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e02267ee3f6255c8fb9f4a4917cd568311b88b718bce4b33aa3008ec941bc4c2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 29 Nov 2019 04:34:15 GMT
RUN Install update 1809-amd64
# Tue, 10 Dec 2019 21:34:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2019 19:14:55 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 11 Dec 2019 19:15:29 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Wed, 11 Dec 2019 19:15:30 GMT
ENV JAVA_VERSION=8u232
# Wed, 11 Dec 2019 19:15:32 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_
# Wed, 11 Dec 2019 19:15:34 GMT
ENV JAVA_URL_VERSION=8u232b09
# Wed, 11 Dec 2019 19:16:57 GMT
RUN $url = ('{0}x64_windows_{1}.zip' -f $env:JAVA_BASE_URL, $env:JAVA_URL_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac -version'; javac -version; 	Write-Host '  java -version'; java -version; 		Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:faf31ee0aa3d3c60a38dd03c7554d632065cef50eab052ef1444590786249d07`  
		Size: 681.6 MB (681618026 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e147f14e0d6a9cbd5261162dea8f3aac7a34db5d9f6a587a9aac6b88722a2da4`  
		Last Modified: Tue, 10 Dec 2019 22:07:34 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616f056aa5a533be44b6ee07856cba49d6ee5ae61de81fdf6966a266c4ab152a`  
		Last Modified: Wed, 11 Dec 2019 20:13:21 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7b6e120a2440dff2cd08c579927e73cea8f0a81f6728e1ca1205fc82bba7bb`  
		Last Modified: Wed, 11 Dec 2019 20:13:21 GMT  
		Size: 4.6 MB (4576681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65208a824b31b32d5858921f38bb814de4c7a9e6fa0e1a9094101d1811199210`  
		Last Modified: Wed, 11 Dec 2019 20:13:19 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2135681a8f13f38fd7834040203cff6d4ac04dad2c3591c415fe22964b49e69`  
		Last Modified: Wed, 11 Dec 2019 20:13:19 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03bba51b432b5fe63679de23497f89bccedf4bca8e971cb00f06fb9aecefa405`  
		Last Modified: Wed, 11 Dec 2019 20:13:20 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb0375cadc9ae536877166e9efb41f8f395835725f1f9c7670b0134b34222d24`  
		Last Modified: Wed, 11 Dec 2019 20:13:36 GMT  
		Size: 99.8 MB (99764554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
