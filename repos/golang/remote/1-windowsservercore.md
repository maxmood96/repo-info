## `golang:1-windowsservercore`

```console
$ docker pull golang@sha256:e70de01d9482e0fe3a624ea72d50b974edd44040ff4de4cdb97cc3232f135d14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `golang:1-windowsservercore` - windows version 10.0.20348.2762; amd64

```console
$ docker pull golang@sha256:67fc9f9fdbc9791a990ed4c7884ae6ae0f8307807c13b357441c63e29a427ace
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1902581230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35af519f2a81290d7577c119cb68c94f587219186b0f3f207ebc41c769bc3a8d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Wed, 09 Oct 2024 23:00:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 23:00:01 GMT
ENV GIT_VERSION=2.23.0
# Wed, 09 Oct 2024 23:00:02 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 09 Oct 2024 23:00:03 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 09 Oct 2024 23:00:08 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 09 Oct 2024 23:00:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 09 Oct 2024 23:00:29 GMT
ENV GOPATH=C:\go
# Wed, 09 Oct 2024 23:00:34 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Oct 2024 23:00:35 GMT
ENV GOLANG_VERSION=1.23.2
# Wed, 09 Oct 2024 23:01:52 GMT
RUN $url = 'https://dl.google.com/go/go1.23.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'bc28fe3002cd65cec65d0e4f6000584dacb8c71bfaff8801dfb532855ca42513'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 09 Oct 2024 23:01:53 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5ee69cc7a7c00cdf4c7f1dbff132533631d0ad0ceaa5b5ff3db486c5b53c91`  
		Last Modified: Wed, 09 Oct 2024 23:02:01 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cbbe74f967f0f9a9ef684fce9a9aa625821acdbfe105c34435074aef0d4d18`  
		Last Modified: Wed, 09 Oct 2024 23:02:01 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf92431dccc391f1ee38a98f1ca77b1097bda8214d7419e6969cb3abf8430c4`  
		Last Modified: Wed, 09 Oct 2024 23:02:00 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41eaca868705c9e05560d53495acf3d495d0b7a06c6ca9b329fbd507d7d6edea`  
		Last Modified: Wed, 09 Oct 2024 23:02:00 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba929dd024b4609634374ae5172ba04b23b9a0d30aa37a2b7ca3d881d55c2b6`  
		Last Modified: Wed, 09 Oct 2024 23:01:59 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1298a5450abb7290201ff8c77efe56187bfa7a3ebef66eff603c77c1b506b6fa`  
		Last Modified: Wed, 09 Oct 2024 23:02:02 GMT  
		Size: 25.6 MB (25565156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64778e8a77ed158cfedca607e2abc463e88daa09877472b22079c2d7bb486626`  
		Last Modified: Wed, 09 Oct 2024 23:01:58 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82ce14ff8404e31e6ceaaaaa071eea060149cdb4568c12d3539669a2744c2fff`  
		Last Modified: Wed, 09 Oct 2024 23:01:58 GMT  
		Size: 335.7 KB (335731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7b91e7a00fd9533319ca369401b4fe2dcefda3dfa70aa511d56ca40081abd57`  
		Last Modified: Wed, 09 Oct 2024 23:01:58 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd6e8a148665bc2d68668af00265458e6f605be340e500fc302c1c9ca4e7437`  
		Last Modified: Wed, 09 Oct 2024 23:02:09 GMT  
		Size: 77.3 MB (77328388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74da972d21cb88b99cb078df72e224aff083f94475d206d2cd1f1536774545cd`  
		Last Modified: Wed, 09 Oct 2024 23:01:58 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull golang@sha256:297687d686b8a28bd06de3cf4c8c232f43eedc77c5b889d2c40a13429d17496f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2005229032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa8e81ecaa31896c5c040f3942d8ca486e031e1836e6161268c78a1a28da232b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Wed, 09 Oct 2024 23:07:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 23:07:08 GMT
ENV GIT_VERSION=2.23.0
# Wed, 09 Oct 2024 23:07:09 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 09 Oct 2024 23:07:09 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 09 Oct 2024 23:07:10 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 09 Oct 2024 23:08:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 09 Oct 2024 23:08:17 GMT
ENV GOPATH=C:\go
# Wed, 09 Oct 2024 23:08:23 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Oct 2024 23:08:24 GMT
ENV GOLANG_VERSION=1.23.2
# Wed, 09 Oct 2024 23:10:26 GMT
RUN $url = 'https://dl.google.com/go/go1.23.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'bc28fe3002cd65cec65d0e4f6000584dacb8c71bfaff8801dfb532855ca42513'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 09 Oct 2024 23:10:27 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c0b69ce3049c27995588e18993ed09137752980cac80c4663648f5089cd9275`  
		Last Modified: Wed, 09 Oct 2024 23:10:35 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbba7602ffdb33cd282009cf1d68032a22821a3999cb542a3ad983d4d826621b`  
		Last Modified: Wed, 09 Oct 2024 23:10:35 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85184f815a4ea0c2d893d89869ca572c31fb105c4c70b03706bd4f58ca4aaf0a`  
		Last Modified: Wed, 09 Oct 2024 23:10:33 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc241ab5ab4740281e28481724541dcc6e188f2ffa28e4861f5648d630ace57`  
		Last Modified: Wed, 09 Oct 2024 23:10:33 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c76426ffa00c2faa295c3cc1b31156e15134b0690e4a1b629a64fe729e7056`  
		Last Modified: Wed, 09 Oct 2024 23:10:33 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c03c0444578ea76cd2a730e33886d9c2ec957c31c4341bddd62b67f34508c3`  
		Last Modified: Wed, 09 Oct 2024 23:10:35 GMT  
		Size: 25.6 MB (25566436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81fe3d482d8c7ec1f9a8be4b592907ad8c05d338a0c9edb4a4b734a79eee532`  
		Last Modified: Wed, 09 Oct 2024 23:10:31 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1ed797d603bcaafab01b729f9f4997af2b4b044ee40a85449f400aead10eed`  
		Last Modified: Wed, 09 Oct 2024 23:10:31 GMT  
		Size: 324.8 KB (324810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54630601fb93553af5e9d2e83bb1e0d212cce73f4bea992c668aef743868d62d`  
		Last Modified: Wed, 09 Oct 2024 23:10:31 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc433f483b37ead71df015348df3261600f715ed35293715ecb7153d8b78a20c`  
		Last Modified: Wed, 09 Oct 2024 23:10:43 GMT  
		Size: 77.5 MB (77501886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2af687eb62f54159437b2fb0cf416cb98e217cc5a67ef09d2f3dfbf072c95c6`  
		Last Modified: Wed, 09 Oct 2024 23:10:31 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
