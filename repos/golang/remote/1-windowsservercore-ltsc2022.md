## `golang:1-windowsservercore-ltsc2022`

```console
$ docker pull golang@sha256:f22fee59b8787fcdd960c9a73330d46f44901cb44db37903a50dc8d625477ab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `golang:1-windowsservercore-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull golang@sha256:3915f12448cd0eeb5904605d5f8f72970708eff5eec4a540a6d0233899b8a0f7
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2407389088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eff297937d38a806b6e722fb905457d85d7013e378adcc42bad322886799284`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Tue, 06 May 2025 19:25:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 06 May 2025 19:25:11 GMT
ENV GIT_VERSION=2.48.1
# Tue, 06 May 2025 19:25:12 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 06 May 2025 19:25:12 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 06 May 2025 19:25:13 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 06 May 2025 19:26:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 06 May 2025 19:26:28 GMT
ENV GOPATH=C:\go
# Tue, 06 May 2025 19:26:35 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 06 May 2025 19:26:36 GMT
ENV GOLANG_VERSION=1.24.3
# Tue, 06 May 2025 19:29:11 GMT
RUN $url = 'https://dl.google.com/go/go1.24.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'be9787cb08998b1860fe3513e48a5fe5b96302d358a321b58e651184fa9638b3'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 06 May 2025 19:29:12 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b6ee194dfee460cc53e0f761b7ff976c08380d6cd1e70cc50ff92cfa99d176`  
		Last Modified: Thu, 08 May 2025 17:22:47 GMT  
		Size: 811.4 MB (811390127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c98d92f22ab0d5c6c5ea3f06ad91355c59e318a738fe9a058cf6fd0da506ee81`  
		Last Modified: Thu, 08 May 2025 17:22:22 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb78dd05f81f129b030ea299588a235605b4b9801832ad5bb55307421220dec`  
		Last Modified: Thu, 08 May 2025 17:22:22 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caee6e09da45816722ae4119e6b23b4a94f6dcee98212b92d53766faa0b05d3b`  
		Last Modified: Thu, 08 May 2025 17:22:22 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:380a4d5f00e122cb5c72104331a6ce92abdcb724c738b7866f7f30b278732770`  
		Last Modified: Thu, 08 May 2025 17:22:24 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e487273d43722bcdbb731db8d220c06f6b424df8c9a8962b050ddd00e5e96c30`  
		Last Modified: Thu, 08 May 2025 17:22:24 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4072413ce3a00860917addef04cd728dbb113dc489fb8d61e0cf151c4332c6ee`  
		Last Modified: Thu, 08 May 2025 17:22:32 GMT  
		Size: 51.2 MB (51210564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f119da440b47772ac2bc4b137513245e424af28de85eb880ed398e0d7d5138`  
		Last Modified: Thu, 08 May 2025 17:22:26 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7609a3365fbbfe8598bd85d9ff49ca733041b13747a76c618c5ed38c6de4c7ee`  
		Last Modified: Thu, 08 May 2025 17:22:27 GMT  
		Size: 314.6 KB (314611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65952ef9921c0868bb6a5035d8db0d15d71b6956f5836a4dacdf34fd63cb4aa0`  
		Last Modified: Thu, 08 May 2025 17:22:29 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2a2ab2fb53c0e7db78829d23691aec4105c117d07fa842fa889012c652eba1a`  
		Last Modified: Thu, 08 May 2025 17:22:42 GMT  
		Size: 82.3 MB (82270922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c53bae34a3be3d2830ea7605006ae635b27040e56aa0d56f441a446f630978`  
		Last Modified: Thu, 08 May 2025 17:22:32 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
