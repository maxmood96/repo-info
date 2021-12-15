## `golang:rc-windowsservercore`

```console
$ docker pull golang@sha256:049df0df4a279f78ed30868043ae8eac4931eccc902321c0fce6a99be52afcf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.20348.405; amd64
	-	windows version 10.0.17763.2366; amd64
	-	windows version 10.0.14393.4825; amd64

### `golang:rc-windowsservercore` - windows version 10.0.20348.405; amd64

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

### `golang:rc-windowsservercore` - windows version 10.0.17763.2366; amd64

```console
$ docker pull golang@sha256:7ff1f2b9b7ef8b12693f83eaa6203fb597fc1e8c753833d89467441c7752da22
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2886417754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c442b97961db89da58b3267a31e96465b82be8b7d2ea005387db661066bb19ad`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 07 Dec 2021 04:56:01 GMT
RUN Install update 1809-amd64
# Wed, 15 Dec 2021 00:45:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Dec 2021 00:45:53 GMT
ENV GIT_VERSION=2.23.0
# Wed, 15 Dec 2021 00:45:54 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 15 Dec 2021 00:45:55 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 15 Dec 2021 00:45:57 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 15 Dec 2021 00:48:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 15 Dec 2021 00:48:32 GMT
ENV GOPATH=C:\go
# Wed, 15 Dec 2021 00:50:15 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 15 Dec 2021 00:50:16 GMT
ENV GOLANG_VERSION=1.18beta1
# Wed, 15 Dec 2021 00:53:49 GMT
RUN $url = 'https://dl.google.com/go/go1.18beta1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '3a43ab4ec28eee6b10fd412a055724d962227f1c27a78960d6d229d741f8353d'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 15 Dec 2021 00:53:51 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5ee7a7ea9cf22f75886179907a41810a992e21f3d0c57cc10d2147ce9237701c`  
		Size: 990.3 MB (990271574 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:aabd70b2463e8240ac41c7d726f6fcfc25424b74f20bb5e8642dbb9bc2b789c8`  
		Last Modified: Wed, 15 Dec 2021 01:53:57 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a8639e414e28c147782b979f15c11cacfe3670dc5a898f9d0fc95ebadeb3f5a`  
		Last Modified: Wed, 15 Dec 2021 01:53:57 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a032d0c95307404bb3f5ccd3d69031082f2a3a1ab0eadd1ce3b12d931bd3e6`  
		Last Modified: Wed, 15 Dec 2021 01:53:54 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4ddbbfd5905588817615b135bf7431f7a67d054028d23d234b326a68097b39`  
		Last Modified: Wed, 15 Dec 2021 01:53:53 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22bfacbdbf128875fdbf7e39f4d3b2030fe3e310d9069f2a55924a2cf3e91ac`  
		Last Modified: Wed, 15 Dec 2021 01:53:53 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f566d739bb0bdf88e33c8c46b5751f6dcdf79a57d123fc0a559e3e189924cf4c`  
		Last Modified: Wed, 15 Dec 2021 01:54:00 GMT  
		Size: 25.5 MB (25463347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e73a67af47aee0d209f8dfd5ea371efb1b0c5205c8d5be95680c9675c302cb`  
		Last Modified: Wed, 15 Dec 2021 01:53:51 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9036358af62e5d57f75caa56f99c1236c8bd7a61e2dd902f023c4ab45877aee`  
		Last Modified: Wed, 15 Dec 2021 01:53:51 GMT  
		Size: 341.0 KB (341030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d3bcf72ba9a6930431ae06b4db502b15984779b5ac966b6a9d3344d5effa312`  
		Last Modified: Wed, 15 Dec 2021 01:53:51 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ebb35ce0ce1792d2209c4e10ac146af70fb711d87e535d787ecbc107f3aefc`  
		Last Modified: Wed, 15 Dec 2021 01:54:29 GMT  
		Size: 152.0 MB (151997368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee95d777af991f26dff195dbec4239cd84385837257a40d55b12dff07d93f8f`  
		Last Modified: Wed, 15 Dec 2021 01:53:51 GMT  
		Size: 1.5 KB (1547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-windowsservercore` - windows version 10.0.14393.4825; amd64

```console
$ docker pull golang@sha256:e7a9ee6182f68b2a52af90df9040a61a99eceb09d2ecd61ef44ba0a05ced4a90
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 GB (6456928916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b780952a5844f628221329df4d17717a81906840cef39557351a3ea2c2dddf`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 08 Dec 2021 08:38:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Dec 2021 00:54:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Dec 2021 00:54:10 GMT
ENV GIT_VERSION=2.23.0
# Wed, 15 Dec 2021 00:54:11 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 15 Dec 2021 00:54:12 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 15 Dec 2021 00:54:13 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 15 Dec 2021 00:56:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 15 Dec 2021 00:56:06 GMT
ENV GOPATH=C:\go
# Wed, 15 Dec 2021 00:57:05 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 15 Dec 2021 00:57:06 GMT
ENV GOLANG_VERSION=1.18beta1
# Wed, 15 Dec 2021 01:00:25 GMT
RUN $url = 'https://dl.google.com/go/go1.18beta1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '3a43ab4ec28eee6b10fd412a055724d962227f1c27a78960d6d229d741f8353d'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 15 Dec 2021 01:00:27 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2d026d646213ccf73d9f0584941d108253d62e73df2a74e070776884b7b0242b`  
		Size: 2.2 GB (2204728802 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e473536e08c92a08f92b05dcf009604fd3f0425171a596a8efeeeb5f69746a24`  
		Last Modified: Wed, 15 Dec 2021 01:54:48 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a097f1c6da1d1d6045b118791cf5076a7360b91373bae76209dbfa4609e661`  
		Last Modified: Wed, 15 Dec 2021 01:54:48 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32ba63b1b2e53158cc5902f8107d4421a8a12f929e4c67242ce3fa2cbc0553a`  
		Last Modified: Wed, 15 Dec 2021 01:54:46 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80515b90b11c42a574f7c31fcadd4d31668f93066540f17e3b0905fe12eacb59`  
		Last Modified: Wed, 15 Dec 2021 01:54:45 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002818a5b378a085c7e0c0f95258fb97a557afe6e00e35912ce0902965cd52d8`  
		Last Modified: Wed, 15 Dec 2021 01:54:44 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6826b991d808a789450cae893bca8fe52c185ba68567aa7c9ec3246d8b657b0`  
		Last Modified: Wed, 15 Dec 2021 01:54:51 GMT  
		Size: 25.4 MB (25419377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd193319409f137bee128603a046e69ee6159b35485612b9e65f81b4ecf814e6`  
		Last Modified: Wed, 15 Dec 2021 01:54:42 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:915b9557c339e8e1394558abd44be62c971aa5b7a6294be429b85d48fdf24bfe`  
		Last Modified: Wed, 15 Dec 2021 01:54:42 GMT  
		Size: 327.7 KB (327679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed259bae46542ad85004c59fe5e3cd3c824acd5d4a5579730cc4174b39a34be`  
		Last Modified: Wed, 15 Dec 2021 01:54:42 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42488de26b327a81edad0a8caf1a3f7210a86a0edb70ab80cf77d1c931fd2a23`  
		Last Modified: Wed, 15 Dec 2021 01:55:20 GMT  
		Size: 156.5 MB (156456115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53379f266690ee7192c9975c49f8c79d9a355f2dad6f82996293fcbde7669f45`  
		Last Modified: Wed, 15 Dec 2021 01:54:42 GMT  
		Size: 1.5 KB (1502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
