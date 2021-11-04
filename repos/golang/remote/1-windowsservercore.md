## `golang:1-windowsservercore`

```console
$ docker pull golang@sha256:06a5f38c86b0eba2a0f22f99a74f36fcf450fd663c2ac7b9d9d3af27a5d30fd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.20348.288; amd64
	-	windows version 10.0.17763.2237; amd64
	-	windows version 10.0.14393.4704; amd64

### `golang:1-windowsservercore` - windows version 10.0.20348.288; amd64

```console
$ docker pull golang@sha256:311bb6d05cec77fecffba9065f9abc420257a2250324f372feb229c04fed7e5a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2313347894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feaa5f37c77d77d379757afbd058cebab0d554cc7fb459eeac62f639b290c8b4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Thu, 07 Oct 2021 11:33:56 GMT
RUN Install update ltsc2022-amd64
# Wed, 13 Oct 2021 12:26:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Oct 2021 12:26:43 GMT
ENV GIT_VERSION=2.23.0
# Wed, 13 Oct 2021 12:26:45 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 13 Oct 2021 12:26:46 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 13 Oct 2021 12:26:47 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 13 Oct 2021 12:28:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Oct 2021 12:28:31 GMT
ENV GOPATH=C:\go
# Wed, 13 Oct 2021 12:29:01 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 04 Nov 2021 20:15:11 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 20:17:36 GMT
RUN $url = 'https://dl.google.com/go/go1.17.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'e78684b955742e215926204afc6ed62b9d165b509e25a687d62902516f08726b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 04 Nov 2021 20:17:44 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b03bbc71f9254a4ad2fba472595c859655b9d0cfefa638928416e277e0f0d497`  
		Size: 889.8 MB (889767519 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b201e45e5b11128e36517715f5b6ae98e5782737c1b112a5fae2aa83206f57bf`  
		Last Modified: Wed, 13 Oct 2021 13:23:57 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2567242b2a3285f24a11ecba702f0e8b3101e1bdaa300b874ba21e16a41b243`  
		Last Modified: Wed, 13 Oct 2021 13:23:57 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6489a6e74029239fb6c471499059266518bce590609bab375525b8cda02168d`  
		Last Modified: Wed, 13 Oct 2021 13:23:55 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:523db4167183ae79d9e363507d248619537805b522b84a3e996a859b61adbe00`  
		Last Modified: Wed, 13 Oct 2021 13:23:54 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8854acf2bd25d9e39c1d4b2387dab690473b72507a036371bc721d43be7c8348`  
		Last Modified: Wed, 13 Oct 2021 13:23:54 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214f893930da68e8c7375a58d2327848d1d80af63c8c28a750e40b3e2a0cc53b`  
		Last Modified: Wed, 13 Oct 2021 13:24:21 GMT  
		Size: 25.7 MB (25710356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b3721e5d0ad0c109458f60c7543d626e543fbe9f992e8f56d387090ba96cb07`  
		Last Modified: Wed, 13 Oct 2021 13:23:51 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145661d5dbf5dce3611b59d5a48a1fc641250e534b0e93a0ee8dcb792c34db12`  
		Last Modified: Wed, 13 Oct 2021 13:23:52 GMT  
		Size: 552.1 KB (552063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8cc7bab962c000a17829d08c517a74c799844fbce96ff636c5f30f2b63e1b11`  
		Last Modified: Thu, 04 Nov 2021 20:48:56 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b48ec46717f45dfcb227eed525825561a31c3148058f7ec2b833f26dc652e0`  
		Last Modified: Thu, 04 Nov 2021 20:49:29 GMT  
		Size: 145.6 MB (145607690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:794c597c157c987d3a522f5719c27e32507a6d44fb4cd243055885b53b0f5a78`  
		Last Modified: Thu, 04 Nov 2021 20:48:56 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-windowsservercore` - windows version 10.0.17763.2237; amd64

```console
$ docker pull golang@sha256:887991b677b8a88a7a264da8406cf5f112ad90a2d81a347980a16c4a4dd68317
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2857483808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d7afc3225d886996109e0f91124176029e37df391aa32c17333cd791bc6d60f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 07 Oct 2021 08:25:51 GMT
RUN Install update 1809-amd64
# Wed, 13 Oct 2021 12:02:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Oct 2021 12:32:43 GMT
ENV GIT_VERSION=2.23.0
# Wed, 13 Oct 2021 12:32:44 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 13 Oct 2021 12:32:45 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 13 Oct 2021 12:32:46 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 13 Oct 2021 12:34:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Oct 2021 12:34:46 GMT
ENV GOPATH=C:\go
# Wed, 13 Oct 2021 12:36:15 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 04 Nov 2021 20:17:54 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 20:21:25 GMT
RUN $url = 'https://dl.google.com/go/go1.17.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'e78684b955742e215926204afc6ed62b9d165b509e25a687d62902516f08726b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 04 Nov 2021 20:21:26 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c0698cf91ebd6bcfb319be6a50421b356d6a3dbbd213d9b2b9dca0f837d7a999`  
		Size: 968.0 MB (967985917 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cc0c4e719f418d49c6a0fb87abd2e0e480c5b6fec1bacc3077cacfad9b4ab3e0`  
		Last Modified: Wed, 13 Oct 2021 12:18:09 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d093aa59fa3e73510b5da63dcef636e5235aaa573c5d0f5fbc57a513bbe216f`  
		Last Modified: Wed, 13 Oct 2021 13:25:02 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c1884eb3ae8f5cad6f4f7a1ad84d352d9a58df436992d1ae80aa11dae35eed`  
		Last Modified: Wed, 13 Oct 2021 13:25:00 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af02b19432c852a1314fe0e01fc2e4896dac408320e91c07ac8ccccb98a093c`  
		Last Modified: Wed, 13 Oct 2021 13:25:00 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7229c7f278a4641a436ffffc5534cf7d46f51e9be8cfb7ea99bfab1c3be6577a`  
		Last Modified: Wed, 13 Oct 2021 13:25:00 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07065e3aa0e037321f634a838f77f322999b1e42f1d8a31012c23dbff249475`  
		Last Modified: Wed, 13 Oct 2021 13:25:06 GMT  
		Size: 25.4 MB (25446235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af043bb60653aabe595cd946487ae7c5c011f8b98d98441c0e034e75e84fb46a`  
		Last Modified: Wed, 13 Oct 2021 13:24:57 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a2710ec37f778ea44892dafe41a303fc27b1423348cf44ef311e0766828aee0`  
		Last Modified: Wed, 13 Oct 2021 13:24:58 GMT  
		Size: 314.8 KB (314815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf6cdd7461f1543b755c22b37e0bfee07e6bf14ab3e30647df915b63507ec4d`  
		Last Modified: Thu, 04 Nov 2021 20:49:44 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:515cd11e4c62efb9faf954282b3f1bffc3826d44ac64912087198791157d7ad6`  
		Last Modified: Thu, 04 Nov 2021 20:50:16 GMT  
		Size: 145.4 MB (145392559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c869560009a7a0010cc6906ce04a22530ef45355e9b4292a7b3439a1403ebaf4`  
		Last Modified: Thu, 04 Nov 2021 20:49:44 GMT  
		Size: 1.6 KB (1567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-windowsservercore` - windows version 10.0.14393.4704; amd64

```console
$ docker pull golang@sha256:863c0549eee99d01e766c702e4def2a81d6ebc48d41bb328d016776107b8d12d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 GB (6448417882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f9cbf0b0ad69c843c7df9b897d3efcdfb903984cce39390bf8ec9266f4a579b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 06 Oct 2021 21:16:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 Oct 2021 12:40:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Oct 2021 12:40:36 GMT
ENV GIT_VERSION=2.23.0
# Wed, 13 Oct 2021 12:40:37 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 13 Oct 2021 12:40:39 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 13 Oct 2021 12:40:40 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 13 Oct 2021 12:43:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Oct 2021 12:43:06 GMT
ENV GOPATH=C:\go
# Wed, 13 Oct 2021 12:44:36 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 04 Nov 2021 20:21:37 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 20:25:26 GMT
RUN $url = 'https://dl.google.com/go/go1.17.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'e78684b955742e215926204afc6ed62b9d165b509e25a687d62902516f08726b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 04 Nov 2021 20:25:28 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0c776a8e8e3c02d360995b7fa26a3fd7c0928965795fac57b69ff07418ab07bf`  
		Size: 2.2 GB (2202780626 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6974b1bd85ba3f9ce16d86231eced43f720fed9c13411d37584dfe7193bcde60`  
		Last Modified: Wed, 13 Oct 2021 13:27:57 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7a41ff4b4f042e62d5c92f3d77a8b07abbe639615dd3c82c4de466c8f44c67f`  
		Last Modified: Wed, 13 Oct 2021 13:27:56 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c02d7d3f40b11b8450a6f82aaeade52a871f8bd89cd1d93c11889b8d3b0219d3`  
		Last Modified: Wed, 13 Oct 2021 13:27:53 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae238abf6097e7b188fc12cace8753067804d4d7d0ce700e8eb15eb81e841181`  
		Last Modified: Wed, 13 Oct 2021 13:27:52 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63c56aed90b0f1415d6aa0f7b18f321cf1c1706a970f0eb885099a8567a1a7c`  
		Last Modified: Wed, 13 Oct 2021 13:27:52 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a205445ee4eb097496ba6f8c71969d7fb8d13de1c26282953b8c224ed3638480`  
		Last Modified: Wed, 13 Oct 2021 13:28:02 GMT  
		Size: 25.4 MB (25446028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600685d5fe3d37b53026a027c0bc19affe258579d3eed1f34414fa405c1b53da`  
		Last Modified: Wed, 13 Oct 2021 13:27:49 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b24162a37292c04cd6b7382e44872740764fb08f2ee07f10bb4ee1abf1dec69`  
		Last Modified: Wed, 13 Oct 2021 13:27:49 GMT  
		Size: 311.4 KB (311356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55450361975d5cd4ab840bb2273696c21af00d16383a1856e240f75a342668e7`  
		Last Modified: Thu, 04 Nov 2021 20:50:32 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6b413858b8da36a185836e7c377d6c8af7f473c5a2a34ebceda23b9925c129`  
		Last Modified: Thu, 04 Nov 2021 20:51:04 GMT  
		Size: 149.9 MB (149883114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:627662bff3a997e98608b3b1845cabae8c1b66b8265ddcae38e5243d3c659582`  
		Last Modified: Thu, 04 Nov 2021 20:50:31 GMT  
		Size: 1.6 KB (1571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
