## `golang:windowsservercore-ltsc2022`

```console
$ docker pull golang@sha256:bc4e70522902823ba8724a995ecb79d3aea3112feabd46db08d81ef29d1c3d7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `golang:windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull golang@sha256:fdd07f21d33a2883687169e3c0ab49a7a559982765f487c51c45052bbb2f840a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2103829634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62343813b34bbc346858443e9e41671763f2e13fdd5ee4267c52de1b57e22794`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 10 Mar 2026 21:56:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Mar 2026 22:08:15 GMT
ENV GIT_VERSION=2.48.1
# Tue, 10 Mar 2026 22:08:15 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 10 Mar 2026 22:08:16 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 10 Mar 2026 22:08:17 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 10 Mar 2026 22:08:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 10 Mar 2026 22:08:30 GMT
ENV GOPATH=C:\go
# Tue, 10 Mar 2026 22:08:36 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 10 Mar 2026 22:08:36 GMT
ENV GOLANG_VERSION=1.26.1
# Tue, 10 Mar 2026 22:10:08 GMT
RUN $url = 'https://dl.google.com/go/go1.26.1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '9b68112c913f45b7aebbf13c036721264bbba7e03a642f8f7490c561eebd1ecc'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 10 Mar 2026 22:10:09 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01bce865a5fef3c3d366224bb94ee05dc622261950fdd529edc41f69aa86a82`  
		Last Modified: Tue, 10 Mar 2026 21:59:15 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9059baa231ace69538d98801b5f30ffe2126f2644971c0a5e1f1ff7ea4d7d6c8`  
		Last Modified: Tue, 10 Mar 2026 22:10:27 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:651107031cb9c76c72a3dff51a55e12db7465a0608babbd79ed3c05c4f323bc6`  
		Last Modified: Tue, 10 Mar 2026 22:10:26 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5cfcc106b1cd6c8910dcb8c9c502287340907aa4d1da09f36e2c5d89470b9e`  
		Last Modified: Tue, 10 Mar 2026 22:10:26 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcba0c26b8ed8ce7c95303ef278e96880371b58a262f9eaa8f2b27391a331d60`  
		Last Modified: Tue, 10 Mar 2026 22:10:26 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e501a5641cc66390105a05d8e6acedc3b550b45c321a2b407e6369e56a3502`  
		Last Modified: Tue, 10 Mar 2026 22:10:32 GMT  
		Size: 51.4 MB (51354870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65bd5c4ee5cb757bcc3cc84dda430bbcb5af5184bd5a32e4c8a41457d871233f`  
		Last Modified: Tue, 10 Mar 2026 22:10:24 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b83f542f1e29c3e63c29d942116e301b7ccf3a81fa94d26674444c9215986ec`  
		Last Modified: Tue, 10 Mar 2026 22:10:24 GMT  
		Size: 348.3 KB (348328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6f90bdaf8f7759ae4c97e8a498bd1a94a4a7c77e0d7584c692fbb00728fd33`  
		Last Modified: Tue, 10 Mar 2026 22:10:24 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:794087f7e9b49f5acfbcea536844ab35b1dd3f0e614139ab194710f93902aba0`  
		Last Modified: Tue, 10 Mar 2026 22:10:36 GMT  
		Size: 69.8 MB (69834349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f77d6574ad874837b8aad143b0dede2ed5826b8e18afe75a15edcacd11dedeb`  
		Last Modified: Tue, 10 Mar 2026 22:10:24 GMT  
		Size: 1.5 KB (1488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
