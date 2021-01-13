## `openjdk:8u275-jdk-windowsservercore-ltsc2016`

```console
$ docker pull openjdk@sha256:1a5433a08a337c4f8ac4dc27c1c6b762a5529573bd6508a87c78201255e232bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4169; amd64

### `openjdk:8u275-jdk-windowsservercore-ltsc2016` - windows version 10.0.14393.4169; amd64

```console
$ docker pull openjdk@sha256:3d67fca1be85b3e5aaa91f1d90e894838f80ff6d48ca8c2ace5f83f7c78b1e32
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5915150513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96265f4d516acde28eb68c312fb489b3560e4d2a526fcaa538bf38a85319d7c1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 07 Jan 2021 11:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 Jan 2021 13:37:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jan 2021 20:58:10 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 13 Jan 2021 20:59:31 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Wed, 13 Jan 2021 20:59:32 GMT
ENV JAVA_VERSION=8u275
# Wed, 13 Jan 2021 20:59:33 GMT
ENV JAVA_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jdk_x64_windows_8u275b01.zip
# Wed, 13 Jan 2021 21:01:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac -version'; javac -version; 	Write-Host '  java -version'; java -version; 		Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bd091f41e44cabc11504b7e130c74a7ef654f58840ba102e3507c4fdf2bae994`  
		Size: 1.7 GB (1723908142 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:51e9c5c519fdcd28aa0ed033a3cc16cf37dd76bea8ec06b2dc4a344415bdd224`  
		Last Modified: Wed, 13 Jan 2021 15:10:27 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d099a75438e800bdc52bf4e96ce679540e315aeb79c38071bf9c71a60799d5a7`  
		Last Modified: Wed, 13 Jan 2021 21:38:21 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e6efe4c025674f508f6b320e81ccbb01dbb030fbfb955701ab03ce3aa867f7`  
		Last Modified: Wed, 13 Jan 2021 21:38:32 GMT  
		Size: 10.1 MB (10146857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb28ea97365042cef4e4e4938b845155712e5c19d910c0dfca8ac244331e22b3`  
		Last Modified: Wed, 13 Jan 2021 21:38:21 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d64dab9ef17d284bdb7a2f5070d01b1b2ca9053ea2d69a57ec1f31c854bf30dd`  
		Last Modified: Wed, 13 Jan 2021 21:38:21 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d61d8955f379b59e5fbc2fdf2158acfe2b0a86ee2229f9096cb16771f4b2405`  
		Last Modified: Wed, 13 Jan 2021 21:40:24 GMT  
		Size: 111.1 MB (111105018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
