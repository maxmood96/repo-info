## `openjdk:8u272-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:af3037109e23b77fc7ce0a058601de816fe27f0b9ab3218b08068e62fe107b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64

### `openjdk:8u272-jdk-windowsservercore-1809` - windows version 10.0.17763.1518; amd64

```console
$ docker pull openjdk@sha256:fcc38dc274221d41d7749c326420ce41a9429f4308e0931c33c1baef0df399cc
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2489002832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da49c3a38d2ebfcdb258a443894aaea25a820d207a6f2119c3bb195fc5bb774`
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
# Mon, 26 Oct 2020 23:16:39 GMT
ENV JAVA_VERSION=8u272
# Mon, 26 Oct 2020 23:16:39 GMT
ENV JAVA_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u272-b10/OpenJDK8U-jdk_x64_windows_8u272b10.zip
# Mon, 26 Oct 2020 23:17:45 GMT
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
	-	`sha256:319edd33d3771a9750d94fe0e08598e37754eec20662b6dbcab8c3c4af9977d4`  
		Last Modified: Mon, 26 Oct 2020 23:28:13 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834220af499fe44a4aa5414039910dc2fdb507c069753d8d06980a33adb87f6a`  
		Last Modified: Mon, 26 Oct 2020 23:28:12 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22fab42a1d0fa13421ec676a3fc51e7ab2bc916691e1c0fd9d5047097c48c76`  
		Last Modified: Mon, 26 Oct 2020 23:30:16 GMT  
		Size: 105.7 MB (105678676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
