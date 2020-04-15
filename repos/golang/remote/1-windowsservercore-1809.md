## `golang:1-windowsservercore-1809`

```console
$ docker pull golang@sha256:ac196bfafe4af0c60e7c3c2578cb3d07792d9a68dca20f1e63220b8d166e1144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1158; amd64

### `golang:1-windowsservercore-1809` - windows version 10.0.17763.1158; amd64

```console
$ docker pull golang@sha256:db08e5c5bdcdca93af63aac5a3df56ae2c766ae71ddf315e487deafea2c583e2
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2434071862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:243ad5611aae50fe9dd1e05734468b9b7d39cd2dc737f2a387a60cabeaa4cf28`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Tue, 14 Apr 2020 21:32:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Apr 2020 12:21:01 GMT
ENV GIT_VERSION=2.23.0
# Wed, 15 Apr 2020 12:21:02 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 15 Apr 2020 12:21:02 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 15 Apr 2020 12:21:03 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 15 Apr 2020 12:22:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 15 Apr 2020 12:22:14 GMT
ENV GOPATH=C:\gopath
# Wed, 15 Apr 2020 12:22:36 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 15 Apr 2020 12:22:36 GMT
ENV GOLANG_VERSION=1.14.2
# Wed, 15 Apr 2020 12:25:15 GMT
RUN $url = ('https://golang.org/dl/go{0}.windows-amd64.zip' -f $env:GOLANG_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '1b5a60b3bbaa81106d5ee03499b5734ec093c6a255abf9a6a067f0f497a57916'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 15 Apr 2020 12:25:17 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edc29de224149bd438350512f7a31a67edbd3fcafce757aa60620dc459c184ad`  
		Last Modified: Tue, 14 Apr 2020 22:15:56 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73418a0571fcf99cda633f93148961556a000d6ca83382f82523ca5a8b0be23`  
		Last Modified: Wed, 15 Apr 2020 12:39:04 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65102d68f0797795223f1f4585ad2b34d000b8e35f180b0f16b3b493f9d3717`  
		Last Modified: Wed, 15 Apr 2020 12:39:01 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3489945d0cac3a39fb186a751328c9ff31076871951d8fa879c17175c562a232`  
		Last Modified: Wed, 15 Apr 2020 12:39:01 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a59f7dec5086ddc5e0977d8f0ed27eb4feb8da6bebdeafb10cb3abe403026d0`  
		Last Modified: Wed, 15 Apr 2020 12:39:01 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aadc1abf3e539cc5d0cfe0421103007d11d6656dd1e615a26fe73a863a4710f`  
		Last Modified: Wed, 15 Apr 2020 12:39:31 GMT  
		Size: 29.8 MB (29755877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64dbdd00c086e554067ca9c230fbcdb94e17c61fb645e42f17bf6aa78bf8ac32`  
		Last Modified: Wed, 15 Apr 2020 12:38:58 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2758f4c98fac0882dfcd1c09b1fc228e49982d00ebacd0cd61da9d79f7150bfa`  
		Last Modified: Wed, 15 Apr 2020 12:38:58 GMT  
		Size: 300.8 KB (300826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8702fd2c1bf8028e78d58e16657d4f879cd73c6aed154ca63df5d9bb0213b74e`  
		Last Modified: Wed, 15 Apr 2020 12:38:58 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f9ecb3612c460309e122bfa58a93f2b9228ce40db45e981b554d52d43a55e6e`  
		Last Modified: Wed, 15 Apr 2020 12:39:25 GMT  
		Size: 133.3 MB (133298731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e320ddd952c25e45e063757cc86c73e032e88550d22bbb0a84e054dc9661560`  
		Last Modified: Wed, 15 Apr 2020 12:38:58 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
