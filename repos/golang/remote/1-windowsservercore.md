## `golang:1-windowsservercore`

```console
$ docker pull golang@sha256:f52890726479830f5a409a05ba42320a0a98c03e1ebdbab8a49445c10428dd2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

### `golang:1-windowsservercore` - windows version 10.0.20348.2402; amd64

```console
$ docker pull golang@sha256:cc9a62e0a48664b751da407dffc4a9a59e0a18e850ac07422e7a5afc113d8fce
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2096847651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:322d4940353a34ad4872847b7ec450be37b956c62681357b5ce8336950b683a9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:06:58 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Apr 2024 01:06:59 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Apr 2024 01:06:59 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Apr 2024 01:07:00 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Apr 2024 01:07:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 01:07:38 GMT
ENV GOPATH=C:\go
# Wed, 10 Apr 2024 01:07:59 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Apr 2024 01:08:00 GMT
ENV GOLANG_VERSION=1.22.2
# Wed, 10 Apr 2024 01:10:17 GMT
RUN $url = 'https://dl.google.com/go/go1.22.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '8e581cf330f49d3266e936521a2d8263679ef7e2fc2cbbceb85659122d883596'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 01:10:19 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446b37fecac1159dce92ccce6a16e77fd3b7c7302e5d36492b37a85cc20e5a`  
		Last Modified: Wed, 10 Apr 2024 00:44:18 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea5ca144c62db12ea36d3f00f6640c6e4758e616b730c3d993fb57c3c8ebad9`  
		Last Modified: Wed, 10 Apr 2024 01:34:50 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d031792c46321e7a0a81f081515ffa50d7c86201a35780d03b0a1a0ecd68ebac`  
		Last Modified: Wed, 10 Apr 2024 01:34:49 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d91b14b8df5887a0feab0adbfcf0dea95d1aab9c3e32619bf6ec5bdc4971a9a4`  
		Last Modified: Wed, 10 Apr 2024 01:34:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099fb3ff689379a9da8dc64f6c1c8d941fb9f0cf66715dc1af16055bdb8e63ec`  
		Last Modified: Wed, 10 Apr 2024 01:34:48 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ca11c05a0028bb84d4b2b76249dfcce87ea1f22340e50e79681c2055ee1d27`  
		Last Modified: Wed, 10 Apr 2024 01:34:54 GMT  
		Size: 25.5 MB (25528844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:587f661259fd2478a26bea01012713bd3afd154dfc37f4aafd87ca98d67f75b7`  
		Last Modified: Wed, 10 Apr 2024 01:34:46 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5830a087830d60f2ed8f1cf87fba9d92cdf7706d61f7692f8aada1a5aec889e8`  
		Last Modified: Wed, 10 Apr 2024 01:34:47 GMT  
		Size: 255.6 KB (255649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba0524d3d449f6bec28fd22fc4893ef4bccc63a6df27e2369f92603cd8f8aa7`  
		Last Modified: Wed, 10 Apr 2024 01:34:46 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6fde223d398d56c25bf4bf900e29f812b150e61b9efb4a4612c527e1fa1c16`  
		Last Modified: Wed, 10 Apr 2024 01:35:08 GMT  
		Size: 71.7 MB (71678634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d4f40b2ec413d1cfd48d890df60e315dbe87ead58931ff0981e4501ecf8e58`  
		Last Modified: Wed, 10 Apr 2024 01:34:46 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-windowsservercore` - windows version 10.0.17763.5696; amd64

```console
$ docker pull golang@sha256:2ea5b4579f8088ed128f51faff20b809cbd4b5db086050728ccf32796ccf65c8
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2261931850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3f4e0de617f934680ff4dd0518687ec088fcafc822ca3e8145935138743ae0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:10:34 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Apr 2024 01:10:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Apr 2024 01:10:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Apr 2024 01:10:37 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Apr 2024 01:12:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 01:12:15 GMT
ENV GOPATH=C:\go
# Wed, 10 Apr 2024 01:13:36 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Apr 2024 01:13:36 GMT
ENV GOLANG_VERSION=1.22.2
# Wed, 10 Apr 2024 01:17:08 GMT
RUN $url = 'https://dl.google.com/go/go1.22.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '8e581cf330f49d3266e936521a2d8263679ef7e2fc2cbbceb85659122d883596'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 01:17:09 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d438ec04c376f7ffff3d4a16e8eb5f805f6f7cd5441a903c7b428c670212f4`  
		Last Modified: Wed, 10 Apr 2024 00:46:06 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843b97b1625fa02e123dfc05bebcf9f05077e6dbdd1f5253c3c6d07b95f0f55f`  
		Last Modified: Wed, 10 Apr 2024 01:35:25 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6532f7333203cbc41355f91a4431427f575a24ad3dc3dd393b4292b4c2660d76`  
		Last Modified: Wed, 10 Apr 2024 01:35:23 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c34d692c7e9d5e97e4674c9fefa41e1c78447d2e9c8db3a3f94f325b6188af`  
		Last Modified: Wed, 10 Apr 2024 01:35:23 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2cead4e65b4492e37b01dc6043de135f9dfad18c9f01232c605eb59e7da4a98`  
		Last Modified: Wed, 10 Apr 2024 01:35:23 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7638380d4eb3933d8241dfe83deaffc516e8bed7b2ab01f96b42864a0d722760`  
		Last Modified: Wed, 10 Apr 2024 01:35:27 GMT  
		Size: 25.5 MB (25535896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159dd7a1de12391b28b5260b6132a515d19e87a7e18b64d7bc843df2c26fb615`  
		Last Modified: Wed, 10 Apr 2024 01:35:20 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3004df08705794a49d57aabf8c97ae8dfe750cedd45eb476bd574ce29807e152`  
		Last Modified: Wed, 10 Apr 2024 01:35:21 GMT  
		Size: 263.3 KB (263307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e227e7e1e73eb30675787faa91206229abfe253a434b7e37e57021c22a59e60`  
		Last Modified: Wed, 10 Apr 2024 01:35:21 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:282b0c0dc4e6505d1cbd89cbf67a95b00d3a0a4cb92fc4eab8e2923ddafc3380`  
		Last Modified: Wed, 10 Apr 2024 01:35:42 GMT  
		Size: 71.7 MB (71693699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32668d9f0337ec3f106c7bb1d5286fe04f60fd7d2a5f1393106647cd1715ae42`  
		Last Modified: Wed, 10 Apr 2024 01:35:21 GMT  
		Size: 1.6 KB (1568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
