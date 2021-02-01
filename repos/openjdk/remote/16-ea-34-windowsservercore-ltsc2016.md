## `openjdk:16-ea-34-windowsservercore-ltsc2016`

```console
$ docker pull openjdk@sha256:ba1118f1448f3f2750d9b4eec06bfdf8c9063c0d9ef76a5459c0aff35e12a536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4169; amd64

### `openjdk:16-ea-34-windowsservercore-ltsc2016` - windows version 10.0.14393.4169; amd64

```console
$ docker pull openjdk@sha256:9e2d96c708dcf8a78ce4d696c25b72cf0671844fbdc2767ca8dc2c4eee9d0695
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (5999818029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9215a54d0b28dbd5502a85f0631a94356c85b3144361fc7781776fbd784f16c5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 07 Jan 2021 11:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 Jan 2021 13:37:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 01 Feb 2021 19:18:44 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 01 Feb 2021 19:24:26 GMT
ENV JAVA_HOME=C:\openjdk-16
# Mon, 01 Feb 2021 19:25:42 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 01 Feb 2021 19:25:43 GMT
ENV JAVA_VERSION=16-ea+34
# Mon, 01 Feb 2021 19:25:44 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk16/34/GPL/openjdk-16-ea+34_windows-x64_bin.zip
# Mon, 01 Feb 2021 19:25:44 GMT
ENV JAVA_SHA256=3a3a6d963036a20df0ce9ed0a0e9eae6ea27ca34279d9f1960390d3cc56b0f0e
# Mon, 01 Feb 2021 19:27:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 01 Feb 2021 19:27:30 GMT
CMD ["jshell"]
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
	-	`sha256:66978b7d55ff893ec83c214709ae41b4b65f437e7e8b19278fc48aaa5804d9a5`  
		Last Modified: Mon, 01 Feb 2021 19:57:01 GMT  
		Size: 10.2 MB (10159693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef6dbc7ed34635ca4af6ddca862e4e803c1bda6cfb4c020191cf55bafef376b0`  
		Last Modified: Mon, 01 Feb 2021 19:58:55 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9132119e2f146d1b77bf06a3495b876ec6a0b8932c83a9e5129d1525f17dfdd5`  
		Last Modified: Mon, 01 Feb 2021 19:58:56 GMT  
		Size: 5.6 MB (5600328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2217bc34a421871c9a7098f1723b0217d78a38eac2b30bed789ca884715f644`  
		Last Modified: Mon, 01 Feb 2021 19:58:52 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f54c57fbd8ba1e309720892223a561f52116fe17b4eb782fa115885a718b69`  
		Last Modified: Mon, 01 Feb 2021 19:58:52 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3293d2be5e1e866298c53161d13b903916353bb0d77a0704d75fe939ad7975`  
		Last Modified: Mon, 01 Feb 2021 19:58:52 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf8bff1dc24704ce977e4c26f9d017160ad2755f14e545217fd9f44d4ad7b66`  
		Last Modified: Mon, 01 Feb 2021 19:59:24 GMT  
		Size: 190.2 MB (190155992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae158bbbb42d837a0879b485a38078b3ab5c482d9903c551cddfe0e3238df82`  
		Last Modified: Mon, 01 Feb 2021 19:58:51 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
