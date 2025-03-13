## `golang:windowsservercore`

```console
$ docker pull golang@sha256:06e300553d88cb739005394684004c1ebeeb1066a056b8d6901151c3fa0b79f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `golang:windowsservercore` - windows version 10.0.26100.3476; amd64

```console
$ docker pull golang@sha256:93663e2a3f82cddc281b508f0845081d35d6e0541aac65389246289ccb566d15
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (3042716400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4521fea3b4ab32b6c4894786d417d38077e4bac0149393e066c1765526b11ff`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Thu, 13 Mar 2025 17:56:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Mar 2025 17:56:27 GMT
ENV GIT_VERSION=2.48.1
# Thu, 13 Mar 2025 17:56:28 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Thu, 13 Mar 2025 17:56:29 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Thu, 13 Mar 2025 17:56:30 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Thu, 13 Mar 2025 17:56:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 13 Mar 2025 17:56:44 GMT
ENV GOPATH=C:\go
# Thu, 13 Mar 2025 17:56:51 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 13 Mar 2025 17:56:52 GMT
ENV GOLANG_VERSION=1.24.1
# Thu, 13 Mar 2025 17:58:06 GMT
RUN $url = 'https://dl.google.com/go/go1.24.1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '95666b551453209a2b8869d29d177285ff9573af10f085d961d7ae5440f645ce'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 13 Mar 2025 17:58:07 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cabafad37383a76746edfcb2071953269124a2265ba09441ee0f5d7f71198d`  
		Last Modified: Thu, 13 Mar 2025 17:58:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f50de0436cf9ecfa74fc5d95587b22832b984ea8227ca754847427f312104c6d`  
		Last Modified: Thu, 13 Mar 2025 17:58:12 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c75aed525537a85f0e03308401bcdc47750a3300892abc8ea627041e4b835f29`  
		Last Modified: Thu, 13 Mar 2025 17:58:11 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:467bb08e0639dedd01fcce8a6154413b2afb3dbb2ebb7299bb398784b35bb790`  
		Last Modified: Thu, 13 Mar 2025 17:58:11 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bcf78f047f3484aaece02ecd4a59d5984810bdf2d5627eae59f7a6a64bdc99f`  
		Last Modified: Thu, 13 Mar 2025 17:58:11 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc180882dccbcbfa8ed2c24aeed59fe82f22d7c2703782b9671137e04efb6df`  
		Last Modified: Thu, 13 Mar 2025 17:58:18 GMT  
		Size: 51.2 MB (51243951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28a136d0465fb143e0d7d496e097d70e9811be3247a61030b9295bba520699a`  
		Last Modified: Thu, 13 Mar 2025 17:58:10 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba33351ae4b9fc70289ba768d1144182d84527ca94055f51de19e8002557af1`  
		Last Modified: Thu, 13 Mar 2025 17:58:10 GMT  
		Size: 368.5 KB (368501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f818c7fc05eb20c78075dd4cac280ba03d2788ebe1ec8a4f8ebe72aeacec52d`  
		Last Modified: Thu, 13 Mar 2025 17:58:10 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b877f11928db80d3e7990cbe1a38b96b6f336c9c4e8dae51dc5af77a13999e1e`  
		Last Modified: Thu, 13 Mar 2025 17:58:26 GMT  
		Size: 82.4 MB (82445659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7b36712399b98e09d95ac09a8711d211d7817039520c1b2bdf76e202e9b32c`  
		Last Modified: Thu, 13 Mar 2025 17:58:10 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:windowsservercore` - windows version 10.0.20348.3328; amd64

```console
$ docker pull golang@sha256:800cffaa1fb68ea86108aa0e47799657cefb5eb2dafec292736d26a250d5090d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2403740620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cebe5eef200c42e308ad630eb5e0ff1ca5a8648c191a55290b9e515a29d77c4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Thu, 13 Mar 2025 18:03:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Mar 2025 18:03:52 GMT
ENV GIT_VERSION=2.48.1
# Thu, 13 Mar 2025 18:03:53 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Thu, 13 Mar 2025 18:03:54 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Thu, 13 Mar 2025 18:03:54 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Thu, 13 Mar 2025 18:04:16 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 13 Mar 2025 18:04:17 GMT
ENV GOPATH=C:\go
# Thu, 13 Mar 2025 18:04:23 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 13 Mar 2025 18:04:24 GMT
ENV GOLANG_VERSION=1.24.1
# Thu, 13 Mar 2025 18:05:39 GMT
RUN $url = 'https://dl.google.com/go/go1.24.1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '95666b551453209a2b8869d29d177285ff9573af10f085d961d7ae5440f645ce'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 13 Mar 2025 18:05:41 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e55f99de87a30a6a17cfcb672b7f4ee158a3b5e425660bab42f52d6a7e2f669`  
		Last Modified: Thu, 13 Mar 2025 18:05:47 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9abedd7c76e3f893429d285cf368820ab93c85364936bb1b75c3b477a3d05fc7`  
		Last Modified: Thu, 13 Mar 2025 18:05:47 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:070850bc0ca89244d2c69c30e03d37ea28b65fe02554aeaf19492b5f6a8df521`  
		Last Modified: Thu, 13 Mar 2025 18:05:46 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b85d83886b6143c40018855a4ba72fb650d98a4f16e07e4183f42ae42c5410`  
		Last Modified: Thu, 13 Mar 2025 18:05:45 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf89c75fd7760c0c1b1b2cc82356717272f0ceb467fc8ce8a85d07fdc903fa29`  
		Last Modified: Thu, 13 Mar 2025 18:05:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33517bbae483baac54ac53322dc846f325d40014b2a10dff5fe6132bc948ac99`  
		Last Modified: Thu, 13 Mar 2025 18:05:51 GMT  
		Size: 51.2 MB (51208026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c00643481be58c834803b2f8f601e7d1fd01e6e6f762bc6140b32109c95bd5`  
		Last Modified: Thu, 13 Mar 2025 18:05:44 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b6b771b9dd29327d0054d0805bd84833beb52b8cce661da3dfbcd86894fb098`  
		Last Modified: Thu, 13 Mar 2025 18:05:44 GMT  
		Size: 347.5 KB (347465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d47ceb326f6b5b5f9fd92c4bac848bd184921f3996ec43442666bd196f7163`  
		Last Modified: Thu, 13 Mar 2025 18:05:44 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4805646d0f77baad2a61712dce4bea52d805818c042a864bed39b4470a400e4`  
		Last Modified: Thu, 13 Mar 2025 18:05:57 GMT  
		Size: 82.2 MB (82233485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205471dd2aad8662d29c018eb66cee449a0b7f964499a8010340edcef468801e`  
		Last Modified: Thu, 13 Mar 2025 18:05:44 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:windowsservercore` - windows version 10.0.17763.7009; amd64

```console
$ docker pull golang@sha256:2940aedd805dfb2c60a71de5cfd7494ee9f27ed2b9bfba6a0ffece0a30129ea9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2285425680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e8284e2aa9c65a7dd983155736b366f64fabe6ce46da64e85904641e9534dbf`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Thu, 13 Mar 2025 17:54:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Mar 2025 17:54:58 GMT
ENV GIT_VERSION=2.48.1
# Thu, 13 Mar 2025 17:54:59 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Thu, 13 Mar 2025 17:55:00 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Thu, 13 Mar 2025 17:55:00 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Thu, 13 Mar 2025 17:55:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 13 Mar 2025 17:55:28 GMT
ENV GOPATH=C:\go
# Thu, 13 Mar 2025 17:55:34 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 13 Mar 2025 17:55:35 GMT
ENV GOLANG_VERSION=1.24.1
# Thu, 13 Mar 2025 17:56:48 GMT
RUN $url = 'https://dl.google.com/go/go1.24.1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '95666b551453209a2b8869d29d177285ff9573af10f085d961d7ae5440f645ce'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 13 Mar 2025 17:56:49 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81be870f634812fa1f6d6ef69c59c30cc849eb7596a61e1f3f6373a0a383d4ac`  
		Last Modified: Thu, 13 Mar 2025 17:56:57 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a8b22dbc93c5dd5761e377d70a307b01859c72506a434bc7980ec33dd3aa2e`  
		Last Modified: Thu, 13 Mar 2025 17:56:57 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b726286f3b4261c8b41eab22833c2eab62b8539b5d35de8da22ccc3be40d2d`  
		Last Modified: Thu, 13 Mar 2025 17:56:55 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c64d4aaf2deb795cad856869013cbc6ea6c0ba2e8e476e4334e0acc8853062`  
		Last Modified: Thu, 13 Mar 2025 17:56:55 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a721b86de1025ca9822807d4bd52272090272764f25dfb8ac69d0eb36d6bba`  
		Last Modified: Thu, 13 Mar 2025 17:56:55 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755ff4d29b2cfc97e0bd2e86cd87cd9db4f784be84bba2afad44d47e1d586839`  
		Last Modified: Thu, 13 Mar 2025 17:57:02 GMT  
		Size: 51.2 MB (51205680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b7600c08bff7cb8b879392f339bf34ba620f20b441e46dfa3ab55239124304`  
		Last Modified: Thu, 13 Mar 2025 17:56:53 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d55a8591bfdbf361f4d5d6e9b6d827ba7fd30637673aefa88663f8833d6c1d`  
		Last Modified: Thu, 13 Mar 2025 17:56:54 GMT  
		Size: 345.5 KB (345509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474e482464a247f4b87adba57ccbb331fc183aa2204a3cff45093cdc076ba360`  
		Last Modified: Thu, 13 Mar 2025 17:56:54 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7729385db686e034d720cf2a1617ed95ae204a798aa1d74e015319a4426eaaf3`  
		Last Modified: Thu, 13 Mar 2025 17:57:07 GMT  
		Size: 82.2 MB (82229348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5350fe0982ad03eb420de2fdf529fceca297915292bd006b4cb4e29d6d84b487`  
		Last Modified: Thu, 13 Mar 2025 17:56:53 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
