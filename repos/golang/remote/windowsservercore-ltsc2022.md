## `golang:windowsservercore-ltsc2022`

```console
$ docker pull golang@sha256:996128855feaff24b9653fc9ba24e6ce82ac30a9f4d9088fd1708c617d4b42b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `golang:windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

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
