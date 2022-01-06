## `golang:1-windowsservercore-ltsc2022`

```console
$ docker pull golang@sha256:a089e440f8ea033223cf62d5a81293b83b9cd41633770f89327a912b394b4e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.405; amd64

### `golang:1-windowsservercore-ltsc2022` - windows version 10.0.20348.405; amd64

```console
$ docker pull golang@sha256:4ba5c254fc0f968e294b5231cbdd8e0ef3e1f03d5f40db554d015e8d2525c840
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2362652041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b893363878583f62c7908ebffc7a49e12adb4d97374d12172d1ed0b341335965`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Wed, 08 Dec 2021 01:54:07 GMT
RUN Install update ltsc2022-amd64
# Sat, 18 Dec 2021 00:09:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 18 Dec 2021 00:09:40 GMT
ENV GIT_VERSION=2.23.0
# Sat, 18 Dec 2021 00:09:41 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Sat, 18 Dec 2021 00:09:42 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Sat, 18 Dec 2021 00:09:43 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Sat, 18 Dec 2021 00:11:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Sat, 18 Dec 2021 00:11:09 GMT
ENV GOPATH=C:\go
# Sat, 18 Dec 2021 00:12:19 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 06 Jan 2022 22:16:22 GMT
ENV GOLANG_VERSION=1.17.6
# Thu, 06 Jan 2022 22:19:25 GMT
RUN $url = 'https://dl.google.com/go/go1.17.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '5bf8f87aec7edfc08e6bc845f1c30dba6de32b863f89ae46553ff4bbcc1d4954'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 06 Jan 2022 22:19:28 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4d1d74adc6a92e44b3cd592ec9459f1fff926eaf6fc20bb7526360bec71aefc0`  
		Size: 939.1 MB (939072515 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5bc74beb7593c703ac99379d225f3a9a445549cc06a3fe18f44e356a45f225f3`  
		Last Modified: Sat, 18 Dec 2021 01:18:31 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b1028951f991b091013b1342c0e005f85e982a60b48918d08057ec5e557fb5`  
		Last Modified: Sat, 18 Dec 2021 01:18:30 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d9a2d78bb32397305b0c23baa615b85b3bb959b897b93830235374f7cea60e`  
		Last Modified: Sat, 18 Dec 2021 01:18:28 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b41481e344ce29afc0524200535b20b998a6ef0f78efeb38911f7505d88f7ff5`  
		Last Modified: Sat, 18 Dec 2021 01:18:26 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c29bf69ec8994283a1109ba28d117561a4fa559f8b21454ffe509ead402ba193`  
		Last Modified: Sat, 18 Dec 2021 01:18:25 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cae36644c2d4df990180986e375123e6dfec1ef62ba5ea747a745113d9bad3`  
		Last Modified: Sat, 18 Dec 2021 01:18:34 GMT  
		Size: 25.7 MB (25725691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8bfce83a6320adcc6f00b53bdffe03ab46c6536b80bb4fdcf41974c942c78b6`  
		Last Modified: Sat, 18 Dec 2021 01:18:23 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dd152958fc672765a54b3cd82f4d65b636569e6854ae27fa2526d2389587ed8`  
		Last Modified: Sat, 18 Dec 2021 01:18:24 GMT  
		Size: 546.6 KB (546617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14d4246b5ff39937e0155690d4d08b9ae56c6a87f1b846cc37a0e9d6eb113b91`  
		Last Modified: Thu, 06 Jan 2022 22:59:39 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e6291f0e57ed7a27158f255a5aed6e73487d3b5e91c4122fd51bfcd50b43f2`  
		Last Modified: Thu, 06 Jan 2022 23:00:27 GMT  
		Size: 145.6 MB (145596669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2f5e85bd862cc717a5ac897ff053ac33d8a1d7f5109eedf042c7a358a8ea81`  
		Last Modified: Thu, 06 Jan 2022 22:59:39 GMT  
		Size: 1.6 KB (1559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
