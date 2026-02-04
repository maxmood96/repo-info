## `golang:windowsservercore`

```console
$ docker pull golang@sha256:23150d7a9ed7721dde9de5e33eac24c8d8fc6f1b49fd7f725675c413c05cfa11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `golang:windowsservercore` - windows version 10.0.26100.32230; amd64

```console
$ docker pull golang@sha256:4d030e9d4363ba6aca04771012584fc0af37581df3c8613569739ba812ec6d1b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1610064800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cab533d09846c004c8b72aaa48bc9e4bb769dac52d12ebe7c182ab5a06afde7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Wed, 04 Feb 2026 17:09:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 04 Feb 2026 17:10:00 GMT
ENV GIT_VERSION=2.48.1
# Wed, 04 Feb 2026 17:10:01 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 04 Feb 2026 17:10:02 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 04 Feb 2026 17:10:03 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 04 Feb 2026 17:10:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 04 Feb 2026 17:11:00 GMT
ENV GOPATH=C:\go
# Wed, 04 Feb 2026 17:11:05 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 04 Feb 2026 17:11:06 GMT
ENV GOLANG_VERSION=1.25.7
# Wed, 04 Feb 2026 17:12:27 GMT
RUN $url = 'https://dl.google.com/go/go1.25.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'c75e5f4ff62d085cc0017be3ad19d5536f46825fa05db06ec468941f847e3228'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 04 Feb 2026 17:12:28 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cff0ca9c86a705f58dbc5b545175e27e5e37766e10b3f12eeabd44caff11efa5`  
		Last Modified: Wed, 04 Feb 2026 17:12:42 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e499bb41ea2ee6826b550d07a26576199995701378f04f8fd311f860e5498a3`  
		Last Modified: Wed, 04 Feb 2026 17:12:42 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a005dfb58609e4e8ce8de3ec9360a81b51137963a749610ff1d46ef75477dd`  
		Last Modified: Wed, 04 Feb 2026 17:12:41 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6fbc05539f831c9c45349c2aaaadc887e6e799f00bf4a4b4c44562981fdc71`  
		Last Modified: Wed, 04 Feb 2026 17:12:41 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fdb8f997f4f44fba880e29c37d9be8680c350303cca74d9c43ae1888ecbc11`  
		Last Modified: Wed, 04 Feb 2026 17:12:41 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac274f4427ab6980702746b2a49be6cb4cdce3ea353f39a3688506c894822ba`  
		Last Modified: Wed, 04 Feb 2026 17:12:47 GMT  
		Size: 51.3 MB (51264713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b62d138ab20880bb60281796d095bc8dbb43708f79541f985fc2585ab770d07c`  
		Last Modified: Wed, 04 Feb 2026 17:12:39 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:105fe71e25097160afa6c6bbf04b00f7cfcc4e2a479439568b4a715e7d577635`  
		Last Modified: Wed, 04 Feb 2026 17:12:40 GMT  
		Size: 403.4 KB (403359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889648476a657c9de440693f6a7b89c70891c85866b6ebbafd132d4a92def4ef`  
		Last Modified: Wed, 04 Feb 2026 17:12:39 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef413425c91b6d357d827848da0c9b3c67209ecc40091e76b1e0c53470329ec2`  
		Last Modified: Wed, 04 Feb 2026 17:12:51 GMT  
		Size: 62.6 MB (62625752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a37e896ee43b80530a21a6597c19f5fece282718295ebb59a1ac191ffc4efc`  
		Last Modified: Wed, 04 Feb 2026 17:12:39 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:windowsservercore` - windows version 10.0.20348.4648; amd64

```console
$ docker pull golang@sha256:2302282af91eac0cd684ae03e9b6be66bf0c0caaede4df6761f267c506eac3ea
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1949965533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ae9b4e4e3c09b869a8b354a25c590d5c96ed8a9722d060fce26623c5dfeba0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Wed, 04 Feb 2026 17:08:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 04 Feb 2026 17:08:57 GMT
ENV GIT_VERSION=2.48.1
# Wed, 04 Feb 2026 17:08:59 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 04 Feb 2026 17:09:00 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 04 Feb 2026 17:09:01 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 04 Feb 2026 17:10:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 04 Feb 2026 17:10:21 GMT
ENV GOPATH=C:\go
# Wed, 04 Feb 2026 17:10:29 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 04 Feb 2026 17:10:30 GMT
ENV GOLANG_VERSION=1.25.7
# Wed, 04 Feb 2026 17:12:16 GMT
RUN $url = 'https://dl.google.com/go/go1.25.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'c75e5f4ff62d085cc0017be3ad19d5536f46825fa05db06ec468941f847e3228'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 04 Feb 2026 17:12:18 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f51f3292cab74bc122a8e5d9613d89a3dd3af346e0aef38c425e66ebaf0557`  
		Last Modified: Wed, 04 Feb 2026 17:12:35 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e09a10fe70359edea1e1e424b5301c2e6ef68325345263b3b1471a5aa9e53ca3`  
		Last Modified: Wed, 04 Feb 2026 17:12:35 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:676ccffa59e0f675115205c7c2568712a29f8e610ea040efc3f2764b51adf0f5`  
		Last Modified: Wed, 04 Feb 2026 17:12:33 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b10739d2fdbf8f8cc65af406174b7a94781c90ae1af5208e03d912b989d9a4`  
		Last Modified: Wed, 04 Feb 2026 17:12:33 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455e2588290ce4848f47a024520ced658ee0a00dac08e4ebdee5e8d1f2d31335`  
		Last Modified: Wed, 04 Feb 2026 17:12:33 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e16c531a17086eca7b57937ecd53e02792eefb49cc641beaf09f24e463d8bd2`  
		Last Modified: Wed, 04 Feb 2026 17:12:40 GMT  
		Size: 51.4 MB (51358306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df79859cd0cffcc83054302f3deca8e5a744193febbab66526e93a5033695c98`  
		Last Modified: Wed, 04 Feb 2026 17:12:32 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b502e8bd93706c4cb7da56422a733eb2b133c0149af4ca7a9f27f9d1d63243b`  
		Last Modified: Wed, 04 Feb 2026 17:12:32 GMT  
		Size: 354.3 KB (354349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c937f88799d39640eca55cf58ee5846106e2d818f64d105b3581056d2dc81757`  
		Last Modified: Wed, 04 Feb 2026 17:12:32 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3eaa293f57715e1e901960440339ccc594bebac920bb965fa9969b64ab14e87`  
		Last Modified: Wed, 04 Feb 2026 17:12:43 GMT  
		Size: 62.6 MB (62583060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19ef23c5f297cf4d7f3c372aa300aecf1e1e135467ec194b0a1f1be32815b9f`  
		Last Modified: Wed, 04 Feb 2026 17:12:32 GMT  
		Size: 1.5 KB (1465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
