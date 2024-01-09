## `golang:windowsservercore`

```console
$ docker pull golang@sha256:45c35385efc2b7218837dcba7d3382ef794b84bb2cab924f68fe07d77eea52dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2159; amd64
	-	windows version 10.0.17763.5206; amd64

### `golang:windowsservercore` - windows version 10.0.20348.2159; amd64

```console
$ docker pull golang@sha256:d0cb724341bf89bc679c3e68dffb0fae6eb37547243fc8a4149e6f315d1d60e5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1984556528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd5f13e08adf1fa8f656f9478e185d5f8d3f97caa645705820c0d8eb3a35f17`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 02 Dec 2023 12:42:56 GMT
RUN Install update 10.0.20348.2159
# Tue, 12 Dec 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Dec 2023 23:35:08 GMT
ENV GIT_VERSION=2.23.0
# Tue, 12 Dec 2023 23:35:08 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Tue, 12 Dec 2023 23:35:09 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Tue, 12 Dec 2023 23:35:10 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Tue, 12 Dec 2023 23:35:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 12 Dec 2023 23:35:47 GMT
ENV GOPATH=C:\go
# Tue, 12 Dec 2023 23:36:11 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Jan 2024 22:16:03 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:18:27 GMT
RUN $url = 'https://dl.google.com/go/go1.21.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '27ac9dd6e66fb3fd0acfa6792ff053c86e7d2c055b022f4b5d53bfddec9e3301'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 09 Jan 2024 22:18:28 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7839fc47f6e056f9e09a214230f8b7115e69419dbc74acbbb1ad6bc0caa28862`  
		Last Modified: Tue, 12 Dec 2023 18:27:40 GMT  
		Size: 500.7 MB (500674814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d0c853ded9068434b9128a8016b3ae5e18f748f62801c7bb6e6092495300ec`  
		Last Modified: Wed, 13 Dec 2023 00:02:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf365c1e9d59a58fc8cee2522db9139b36cf02ecabe7302489a9a3667b62cea`  
		Last Modified: Wed, 13 Dec 2023 00:02:39 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69dbeb610a3fa1c3f2962202c58796ff120ea20cc3ba1f2fce807cbbe2c37ab0`  
		Last Modified: Wed, 13 Dec 2023 00:02:37 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a3be8233329999132fa6e504f39c44abd589439a96846e31508037334d6d11`  
		Last Modified: Wed, 13 Dec 2023 00:02:37 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755721e8166183821011ca0acdb563f67887cfe33da36997710b182f049fbede`  
		Last Modified: Wed, 13 Dec 2023 00:02:37 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4700bd9f606505ec47d78dc66a509ca78ea2a8269a8e2b9bcf28ec33c5cbea74`  
		Last Modified: Wed, 13 Dec 2023 00:02:42 GMT  
		Size: 25.6 MB (25554973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777ab971ccee32e15de39ed82eceeb004d2d6f94af7c43ab3d6cfc1baf0abd07`  
		Last Modified: Wed, 13 Dec 2023 00:02:35 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958aa1458398ceb3a543d13279579cc48507080df3b269a5aa1a09da23b03ccf`  
		Last Modified: Wed, 13 Dec 2023 00:02:35 GMT  
		Size: 284.9 KB (284874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ed7a59b16104881efb9e3ac02b81f631cff124b04d7494d955a2c697b7c4ce`  
		Last Modified: Tue, 09 Jan 2024 22:39:21 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b1d528d83cdc1c6fb3f551b955643ffa64d14478df3d1b2aa1faf3cf95d454`  
		Last Modified: Tue, 09 Jan 2024 22:39:41 GMT  
		Size: 69.4 MB (69432029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a8730c2425648e897784c3ff628a5fd72bb913811c924412142d22ce7f7d36c`  
		Last Modified: Tue, 09 Jan 2024 22:39:21 GMT  
		Size: 1.5 KB (1539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:windowsservercore` - windows version 10.0.17763.5206; amd64

```console
$ docker pull golang@sha256:19e5467ed5880db50d14b684588fcf160a4d9698fbb3af07ba4a4f9116230a40
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2154990003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79734498eae78c6de79f97079207f53ea4671b669045abb4b1eba0b42a0d7b36`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Dec 2023 11:24:49 GMT
RUN Install update 10.0.17763.5206
# Tue, 12 Dec 2023 23:38:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Dec 2023 23:38:53 GMT
ENV GIT_VERSION=2.23.0
# Tue, 12 Dec 2023 23:38:53 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Tue, 12 Dec 2023 23:38:54 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Tue, 12 Dec 2023 23:38:55 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Tue, 12 Dec 2023 23:40:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 12 Dec 2023 23:40:27 GMT
ENV GOPATH=C:\go
# Tue, 12 Dec 2023 23:41:35 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Jan 2024 22:18:47 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:22:02 GMT
RUN $url = 'https://dl.google.com/go/go1.21.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '27ac9dd6e66fb3fd0acfa6792ff053c86e7d2c055b022f4b5d53bfddec9e3301'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 09 Jan 2024 22:22:04 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35ae5ad761bfd7e5fb48c234de8722eaa28e17e2c956816fecb417ab6259c29`  
		Last Modified: Tue, 12 Dec 2023 19:14:24 GMT  
		Size: 409.1 MB (409088642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767e95390edb4050b2c57e1d564c9e4722c5ae776ebfb8907a539571a2609f7c`  
		Last Modified: Wed, 13 Dec 2023 00:04:16 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c57683b4a629f3325c8517d99f497d4ffbcd0e70354e70a95d983a275bfe398`  
		Last Modified: Wed, 13 Dec 2023 00:04:16 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95bef40c25d2abc3a12986675189e7152f6197fdc5a17343bdee3f0bc2e95a8`  
		Last Modified: Wed, 13 Dec 2023 00:04:14 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b043d50fbb4f0d8961fe3a95130f520d57cfe7e6e85b15cd4f9f14a01364f7ee`  
		Last Modified: Wed, 13 Dec 2023 00:04:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55867ab446b5d5e34f9e6d414898b9a0b31051afc81b28ace1ce47e27d9e24ee`  
		Last Modified: Wed, 13 Dec 2023 00:04:14 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10285db29cf842d22a49b00cb66fbbfe20e7d4e72a0d3e393d58824190f6835b`  
		Last Modified: Wed, 13 Dec 2023 00:04:19 GMT  
		Size: 25.6 MB (25558777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3037ad7a881ee540014f48a43aa3a857c479d9cefb413ce61a914c943901890b`  
		Last Modified: Wed, 13 Dec 2023 00:04:12 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788faab53b378465ec447dde1961338c1349487d1152856c0524e2f6a503ec70`  
		Last Modified: Wed, 13 Dec 2023 00:04:12 GMT  
		Size: 282.5 KB (282534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca23066a92625cdc8de9b99f08faf5c3e756534401f72ec8aff465b29c481ee`  
		Last Modified: Tue, 09 Jan 2024 22:39:56 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b92d2b727a3677f7df423fdb871102a4f49e8ab3c3f27447b46a8bb9d6315c5`  
		Last Modified: Tue, 09 Jan 2024 22:40:17 GMT  
		Size: 69.4 MB (69428911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c07e208b8230a3cf4f0d09d8d2e0964843388a9334a811e7537778242b4610`  
		Last Modified: Tue, 09 Jan 2024 22:39:56 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
