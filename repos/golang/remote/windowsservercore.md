## `golang:windowsservercore`

```console
$ docker pull golang@sha256:d975a16f08e5cd81c5deac2b4471320955d6de1bcc63b82e01f358b0bd839909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.20348.405; amd64
	-	windows version 10.0.17763.2366; amd64
	-	windows version 10.0.14393.4825; amd64

### `golang:windowsservercore` - windows version 10.0.20348.405; amd64

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

### `golang:windowsservercore` - windows version 10.0.17763.2366; amd64

```console
$ docker pull golang@sha256:536b452a139f15d194e73b69048a513a0ca93f10b56ffb44e4a93a3ebab72be7
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2879843412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ddbd79ccb57916c23c005ce86d4e9cb2b25a0cb708a48cfcde1353d1ad2c62c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 07 Dec 2021 04:56:01 GMT
RUN Install update 1809-amd64
# Fri, 17 Dec 2021 23:26:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 18 Dec 2021 00:15:38 GMT
ENV GIT_VERSION=2.23.0
# Sat, 18 Dec 2021 00:15:39 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Sat, 18 Dec 2021 00:15:40 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Sat, 18 Dec 2021 00:15:41 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Sat, 18 Dec 2021 00:17:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Sat, 18 Dec 2021 00:17:44 GMT
ENV GOPATH=C:\go
# Sat, 18 Dec 2021 00:18:45 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 06 Jan 2022 22:19:38 GMT
ENV GOLANG_VERSION=1.17.6
# Thu, 06 Jan 2022 22:23:51 GMT
RUN $url = 'https://dl.google.com/go/go1.17.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '5bf8f87aec7edfc08e6bc845f1c30dba6de32b863f89ae46553ff4bbcc1d4954'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 06 Jan 2022 22:23:53 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5ee7a7ea9cf22f75886179907a41810a992e21f3d0c57cc10d2147ce9237701c`  
		Size: 990.3 MB (990271574 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:31b2acce136e44984ba36d64717a6a67fbf1a98ed7ffcf0a14df848c1502a345`  
		Last Modified: Fri, 17 Dec 2021 23:47:14 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c62605b0c86ed37b9b47076c7a5944af667c8ce06e7c6a8509ced095cce159`  
		Last Modified: Sat, 18 Dec 2021 01:19:20 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60899de055c3fa34311259654470bdb9f4fae2bbe462783d8e2aee8b6e0b6cb7`  
		Last Modified: Sat, 18 Dec 2021 01:19:19 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536c6124f0e0905a38e8324ae686057b8d0a17aad59faf3c954b569f52851106`  
		Last Modified: Sat, 18 Dec 2021 01:19:18 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e8769770a2b32ba2424d699b18ab6c4166ecd2c1125b1c191d522cc6fd51f7`  
		Last Modified: Sat, 18 Dec 2021 01:19:18 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c0c1d102127ee33e6999825a23a390dab7c3a328fff970083d7bdfe99537821`  
		Last Modified: Sat, 18 Dec 2021 01:19:23 GMT  
		Size: 25.5 MB (25462958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f8bef9894d29031a7a230102260249b6d03330b291463ae3bbca1ef5cd8da7`  
		Last Modified: Sat, 18 Dec 2021 01:19:16 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b42b9032e958eb0bea7fe89c098d5e729ddc543cf6b86e2284ace9fc062aadc1`  
		Last Modified: Sat, 18 Dec 2021 01:19:16 GMT  
		Size: 340.6 KB (340572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a052b1738ba5f522e9610fbae3f1972bca981ae691e049ed9b07b956068a8d65`  
		Last Modified: Thu, 06 Jan 2022 23:00:50 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:941e7adb7f3a0e89b661cc51fc67d057922f4c81b14529e73cc99bdc617cdbd8`  
		Last Modified: Thu, 06 Jan 2022 23:03:24 GMT  
		Size: 145.4 MB (145423878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888baa7dedfe2a537005ea851c77a196974fc1e1dbcc7be7eb93a95fe7c7299e`  
		Last Modified: Thu, 06 Jan 2022 23:00:50 GMT  
		Size: 1.6 KB (1584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:windowsservercore` - windows version 10.0.14393.4825; amd64

```console
$ docker pull golang@sha256:abc81c5e43bc8b9137b77208e78f212263dba20c20ffbd66bf535eb6450e1145
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 GB (6450310736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8f5f9fbdfc0677017ed9fe3c571b5430ea3cda33b40d659b4de7193307ce7ea`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 08 Dec 2021 08:38:00 GMT
RUN Install update ltsc2016-amd64
# Sat, 18 Dec 2021 00:22:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 18 Dec 2021 00:22:41 GMT
ENV GIT_VERSION=2.23.0
# Sat, 18 Dec 2021 00:22:42 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Sat, 18 Dec 2021 00:22:43 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Sat, 18 Dec 2021 00:22:44 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Sat, 18 Dec 2021 00:24:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Sat, 18 Dec 2021 00:24:45 GMT
ENV GOPATH=C:\go
# Sat, 18 Dec 2021 00:25:51 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 06 Jan 2022 22:24:06 GMT
ENV GOLANG_VERSION=1.17.6
# Thu, 06 Jan 2022 22:28:38 GMT
RUN $url = 'https://dl.google.com/go/go1.17.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '5bf8f87aec7edfc08e6bc845f1c30dba6de32b863f89ae46553ff4bbcc1d4954'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 06 Jan 2022 22:28:40 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2d026d646213ccf73d9f0584941d108253d62e73df2a74e070776884b7b0242b`  
		Size: 2.2 GB (2204728802 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7756a7a3024dbbb7cabda3151e8f8461ae808ae2ad3857f0c9235c5908ff7695`  
		Last Modified: Sat, 18 Dec 2021 01:22:26 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed085eeb0f67ab647ce30dc0ee783df8de1d571c430a88d3ce15c11a5d05be15`  
		Last Modified: Sat, 18 Dec 2021 01:22:25 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a04aa8edbd1b61f0fa86243e7064f8560eb1b8e35bf303a4d2503bbb1d5dde1`  
		Last Modified: Sat, 18 Dec 2021 01:22:22 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bb78b2e65fd6a44aae1b3a98ba2f38960b6832446cc98b2640003b1078e282`  
		Last Modified: Sat, 18 Dec 2021 01:22:22 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd20bdd437ff14a08b9ccc6dbce15b95eb2f8f3a347a0392ff074ab9aa123320`  
		Last Modified: Sat, 18 Dec 2021 01:22:22 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788d8768c001ba1aa83b84957dc3d6fc7be04e0d35240454ec8e36dd8cdb5683`  
		Last Modified: Sat, 18 Dec 2021 01:22:29 GMT  
		Size: 25.4 MB (25427117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f55846325b60c2a45902ea9dc05ce8a2a4997cdf73da1c40989dfb0ca2b102dc`  
		Last Modified: Sat, 18 Dec 2021 01:22:19 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ee386d622d2d0becd206facf979e544b5de665c127e96b69cf04031d59cae7`  
		Last Modified: Sat, 18 Dec 2021 01:22:19 GMT  
		Size: 303.8 KB (303841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:591d5b9d615ffc310f103f37865bafc2bb564e3e73b5c70277ccfc4221e06ebc`  
		Last Modified: Thu, 06 Jan 2022 23:03:40 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4175fd0aa7ac936af2da30c8cca9af9e69cbae20facf3dd7eb4402b1f6e40ac9`  
		Last Modified: Thu, 06 Jan 2022 23:04:26 GMT  
		Size: 149.9 MB (149853583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f484c18290d523243269118a30a808a9a227c82c145fb91c41baf583df41734a`  
		Last Modified: Thu, 06 Jan 2022 23:03:40 GMT  
		Size: 1.6 KB (1583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
