## `golang:windowsservercore-ltsc2022`

```console
$ docker pull golang@sha256:7eaf530c684b059d3197361d3e8318e035a03cc6ccfee36386321360d205df85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `golang:windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull golang@sha256:8e22f3f87af250241e729bff779ec382d9842fd73a3fed491f93dbab20488cca
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2365683068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa2eeb17ea0e007bc2a6d2651746c36b74b48ff0f05960bb1474220851548628`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Tue, 14 Jan 2025 23:37:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:37:38 GMT
ENV GIT_VERSION=2.23.0
# Tue, 14 Jan 2025 23:37:38 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Tue, 14 Jan 2025 23:37:39 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Tue, 14 Jan 2025 23:37:40 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Tue, 14 Jan 2025 23:37:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 23:37:55 GMT
ENV GOPATH=C:\go
# Tue, 14 Jan 2025 23:38:00 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Jan 2025 23:38:01 GMT
ENV GOLANG_VERSION=1.23.4
# Tue, 14 Jan 2025 23:39:09 GMT
RUN $url = 'https://dl.google.com/go/go1.23.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '16c59ac9196b63afb872ce9b47f945b9821a3e1542ec125f16f6085a1c0f3c39'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 23:39:10 GMT
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
	-	`sha256:1990eac92b4f705872f5bef3233ae4636574c8ff3b96d34a4a0bbe58426b9454`  
		Last Modified: Tue, 14 Jan 2025 23:39:15 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d36cfee202326232aacd23cf22e6b3d3e8d0c90e7ee832c70fefb64c15a424a`  
		Last Modified: Tue, 14 Jan 2025 23:39:15 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ab35b0cedbf8e8f3ddd7747d2c5735a4e087504017df4b2ec7aa34ae25e7b1`  
		Last Modified: Tue, 14 Jan 2025 23:39:14 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffeffe02b2c341d32586332d54b189a87c41c6b5a8c5f3eaf97fdb9dd4595f7f`  
		Last Modified: Tue, 14 Jan 2025 23:39:14 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b1a21f3f1a8368b83d8e59cd69d24da0dc3c94cabef4e03717db7e3d13c863`  
		Last Modified: Tue, 14 Jan 2025 23:39:14 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdac93b5081407f7abd6d534011e76fb54d2b321a3dbacff1ea791e12405e092`  
		Last Modified: Tue, 14 Jan 2025 23:39:17 GMT  
		Size: 25.4 MB (25430619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:932a09e77451a9f93887ff101dce74b0cc98403984f1f35234696c17d029a4bc`  
		Last Modified: Tue, 14 Jan 2025 23:39:13 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783b2caac7f2dea428984f82fba4e2124b9d5ea1dbceac2e172eadceac5c43fa`  
		Last Modified: Tue, 14 Jan 2025 23:39:13 GMT  
		Size: 335.4 KB (335374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5914eb6a4f10e2b77a7736d1668f41e5802194edf1166bfa0c0116bcf1ec1d3`  
		Last Modified: Tue, 14 Jan 2025 23:39:13 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5af0e4753f7eaa1a86ab0d2369542d5963f3d1bf071a3a8f49c1db1313674ab`  
		Last Modified: Tue, 14 Jan 2025 23:39:25 GMT  
		Size: 77.5 MB (77521322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:871b50d9c4c09823bcc9cc8eb4eb98a2b966b9b4049fb416a0ffa2fb3240245a`  
		Last Modified: Tue, 14 Jan 2025 23:39:13 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
