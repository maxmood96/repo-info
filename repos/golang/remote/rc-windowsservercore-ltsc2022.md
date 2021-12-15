## `golang:rc-windowsservercore-ltsc2022`

```console
$ docker pull golang@sha256:9829c67640131adc917c044ffeb9b8241c494e783147165cf86b384c5ca462c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.405; amd64

### `golang:rc-windowsservercore-ltsc2022` - windows version 10.0.20348.405; amd64

```console
$ docker pull golang@sha256:d52c2288e49c6f7db60b7b6489cd0e0337528f3fffed6e80f61a2564d3956829
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2369228344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a4dac2dea7354eba268fdb5d9d22a2c77bd0589774ef252fb551e17d7d2b11c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Wed, 08 Dec 2021 01:54:07 GMT
RUN Install update ltsc2022-amd64
# Wed, 15 Dec 2021 00:40:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Dec 2021 00:40:22 GMT
ENV GIT_VERSION=2.23.0
# Wed, 15 Dec 2021 00:40:24 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 15 Dec 2021 00:40:25 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 15 Dec 2021 00:40:26 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 15 Dec 2021 00:41:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 15 Dec 2021 00:41:27 GMT
ENV GOPATH=C:\go
# Wed, 15 Dec 2021 00:42:02 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 15 Dec 2021 00:42:03 GMT
ENV GOLANG_VERSION=1.18beta1
# Wed, 15 Dec 2021 00:45:43 GMT
RUN $url = 'https://dl.google.com/go/go1.18beta1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '3a43ab4ec28eee6b10fd412a055724d962227f1c27a78960d6d229d741f8353d'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 15 Dec 2021 00:45:45 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4d1d74adc6a92e44b3cd592ec9459f1fff926eaf6fc20bb7526360bec71aefc0`  
		Size: 939.1 MB (939072515 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0b41c99bb368eaadf91343c8bfccaa11a92f02d60d86febeda9e009eaed579fa`  
		Last Modified: Wed, 15 Dec 2021 01:51:03 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7eb1a5e7dea0a53c9ea436a1dbe9567968300217e1ad744ef5fc0af5fd17e3d`  
		Last Modified: Wed, 15 Dec 2021 01:51:03 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a18dfd01553a8cab256080e47c5c8111521866afb32c6f694b59683dbe2416be`  
		Last Modified: Wed, 15 Dec 2021 01:51:01 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad7e1ebdc3cbf59de41a76791006597e0f8927c01920f858f33f65d36ce0e4b`  
		Last Modified: Wed, 15 Dec 2021 01:51:01 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0532fcfb6c734340e3e1ab8c6c1416b21ae9239967a945bb1d9921e31232300d`  
		Last Modified: Wed, 15 Dec 2021 01:51:00 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b8a70b5f349c15ad0f783b3b04b14ea2a68730ecd0f0b9ea63f970c9870505`  
		Last Modified: Wed, 15 Dec 2021 01:51:07 GMT  
		Size: 25.7 MB (25708582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddc2b44cb36f7cbe88bbfafea3b88eae5ec8d2554ac7e9934e5598ac613d7b1`  
		Last Modified: Wed, 15 Dec 2021 01:50:58 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f26f8a160719f2d2f778607a2ef1c8a213b65b76cdd2e67ced5d9ca5eef763`  
		Last Modified: Wed, 15 Dec 2021 01:50:59 GMT  
		Size: 534.0 KB (534011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad4afa4371abd5a7b9777f6677d63fb4e6249f4721941dc297ba2f35cd544167`  
		Last Modified: Wed, 15 Dec 2021 01:50:58 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58fea725dd63dca70df2e7c5bda96fa24116ab01f696f674144cd68e6c9543fd`  
		Last Modified: Wed, 15 Dec 2021 01:53:38 GMT  
		Size: 152.2 MB (152203380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c01a8ee42ff592f86952a446e4910b5f4db9149a11c35307fdc3c0117ce6bf`  
		Last Modified: Wed, 15 Dec 2021 01:50:58 GMT  
		Size: 1.6 KB (1560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
