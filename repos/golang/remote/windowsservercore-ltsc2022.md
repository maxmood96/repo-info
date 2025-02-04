## `golang:windowsservercore-ltsc2022`

```console
$ docker pull golang@sha256:19eebace78a3d315af4bcea6e425464c3c8ddd4370ff16c35f1c708d2d09c244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `golang:windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull golang@sha256:fbe0f26f6ef43c539114846969afccc8a61be00b0d7ff3f949007d719c7bed3a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2365582960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011d0bb3473a69296785a6d2cb4f721db06febb53c18a6eac3b3e599fc7ff10d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Tue, 04 Feb 2025 19:32:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 04 Feb 2025 19:32:27 GMT
ENV GIT_VERSION=2.23.0
# Tue, 04 Feb 2025 19:32:28 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Tue, 04 Feb 2025 19:32:28 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Tue, 04 Feb 2025 19:32:29 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Tue, 04 Feb 2025 19:32:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 04 Feb 2025 19:32:53 GMT
ENV GOPATH=C:\go
# Tue, 04 Feb 2025 19:32:59 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 04 Feb 2025 19:33:00 GMT
ENV GOLANG_VERSION=1.23.6
# Tue, 04 Feb 2025 19:34:31 GMT
RUN $url = 'https://dl.google.com/go/go1.23.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '53fec1586850b2cf5ad6438341ff7adc5f6700dd3ec1cfa3f5e8b141df190243'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 04 Feb 2025 19:34:32 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c4a80f3032c9f92ee0690ae7f3b87b004fba3330571fcf81a59b65a9d579dc`  
		Last Modified: Tue, 04 Feb 2025 19:34:41 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62d0d235247f69d66eeca78877498320774d1a7980a3f5292bf98784141dd4a5`  
		Last Modified: Tue, 04 Feb 2025 19:34:40 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:476227555e60e1812aecaafff1ac7ea9f3e8b6a4f628f11abf464904d3c285e4`  
		Last Modified: Tue, 04 Feb 2025 19:34:39 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc7b137de7fe84994da0509410eb663799437c980f198f60b9c4444eaed6afeb`  
		Last Modified: Tue, 04 Feb 2025 19:34:39 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:360e464acad2cc059abb482ffaa164684a587e3722ff3871e497dd991f4cb293`  
		Last Modified: Tue, 04 Feb 2025 19:34:39 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee66e6d929b11af9d0f76bd82c40b009ed985d092ca255b1f19e08c4439d01d`  
		Last Modified: Tue, 04 Feb 2025 19:34:42 GMT  
		Size: 25.5 MB (25453430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed45a24e1a2b99b1c1197642bae508c0b7495085f0f7c3d0bac3f0464145f2f0`  
		Last Modified: Tue, 04 Feb 2025 19:34:37 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7aadb9d7c991a5ae80e2b4d21049057bfbddb7980280630af1408b34ce5ad8c`  
		Last Modified: Tue, 04 Feb 2025 19:34:37 GMT  
		Size: 356.8 KB (356802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fdd84c7d1500206a9d9714668860e79066cd37ab27a37aab74722cc73f4890c`  
		Last Modified: Tue, 04 Feb 2025 19:34:37 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8bfb2acdca75f95bd3dcf680a6e32942b4f874908bbabf6003785fd862167a6`  
		Last Modified: Tue, 04 Feb 2025 19:34:49 GMT  
		Size: 77.4 MB (77377050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3656e1cbe3a45783481d60440d516cc3fc892e8be85892fd8429c15c76827772`  
		Last Modified: Tue, 04 Feb 2025 19:34:37 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
