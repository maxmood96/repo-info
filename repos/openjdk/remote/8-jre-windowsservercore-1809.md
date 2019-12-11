## `openjdk:8-jre-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:56dc5802220476e554ae6607f3a98331e81c6e1122cff26c29ad74a0946b215d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.914; amd64

### `openjdk:8-jre-windowsservercore-1809` - windows version 10.0.17763.914; amd64

```console
$ docker pull openjdk@sha256:78d6024082625d04d1cad21cea3e6c7730ddbffafe0b285252b55216de59be5c
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2258468819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05f061184210a772ed7d143dc1a00cb68c19c378657075b0e1e5ee1bb814743`
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
# Wed, 11 Dec 2019 19:22:24 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_
# Wed, 11 Dec 2019 19:22:26 GMT
ENV JAVA_URL_VERSION=8u232b09
# Wed, 11 Dec 2019 19:53:36 GMT
RUN $url = ('{0}x64_windows_{1}.zip' -f $env:JAVA_BASE_URL, $env:JAVA_URL_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  java -version'; java -version; 		Write-Host 'Complete.'
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
	-	`sha256:ce3704bef30ab717e03a1e604783dcedbaadaa50801c01423aa34653b51584dd`  
		Last Modified: Wed, 11 Dec 2019 20:16:08 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e660a7d863a7e86c0f04be3bc449b49a5c53107cf0888009d770bebd271d2a12`  
		Last Modified: Wed, 11 Dec 2019 20:16:07 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ef07bd6c1536132e5ee65e207b4fa7b23ffd772eea1391c655cbd640aee89d`  
		Last Modified: Wed, 11 Dec 2019 20:16:15 GMT  
		Size: 37.6 MB (37582822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
