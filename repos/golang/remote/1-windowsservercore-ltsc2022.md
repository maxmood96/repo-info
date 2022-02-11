## `golang:1-windowsservercore-ltsc2022`

```console
$ docker pull golang@sha256:4fb80ea9740c08a8703478271e781b921fed3012366401331a0fb0c5ed44db15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.524; amd64

### `golang:1-windowsservercore-ltsc2022` - windows version 10.0.20348.524; amd64

```console
$ docker pull golang@sha256:51b14dba5a127ecfe32818d07546e5889250e0cd26f2bb222e03f2ce8de887ab
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2386821713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d717bbe8c93eeec85a1767099b3744363da4578cdde2e86bc06e4833cec0b3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Tue, 01 Feb 2022 02:49:40 GMT
RUN Install update ltsc2022-amd64
# Wed, 09 Feb 2022 13:37:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Feb 2022 13:37:19 GMT
ENV GIT_VERSION=2.23.0
# Wed, 09 Feb 2022 13:37:20 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 09 Feb 2022 13:37:21 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 09 Feb 2022 13:37:22 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 09 Feb 2022 13:38:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 09 Feb 2022 13:38:30 GMT
ENV GOPATH=C:\go
# Wed, 09 Feb 2022 13:38:49 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 11 Feb 2022 01:16:16 GMT
ENV GOLANG_VERSION=1.17.7
# Fri, 11 Feb 2022 01:19:03 GMT
RUN $url = 'https://dl.google.com/go/go1.17.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '1b648165d62a2f5399f3c42c7e59de9f4aa457212c4ea763e1b650546fac72e2'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Fri, 11 Feb 2022 01:19:05 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:898469748ff68223ab87b654b29fb366c1f4f2b7cfad7a37426346ea16db8dfa`  
		Size: 963.2 MB (963225591 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7062696b7aef1ca33afdf32084a532f7e3151a844eb7cb2455bcc907e0f42a58`  
		Last Modified: Wed, 09 Feb 2022 14:28:27 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e671073281e0a800f3f64cb8a9d1092a4e93d2f94cd818b0c1d47824366a5cd`  
		Last Modified: Wed, 09 Feb 2022 14:28:27 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc69c3c295ae9d3878060e3969bb79b86d5163188d65fb1e7afb60d6a74308b`  
		Last Modified: Wed, 09 Feb 2022 14:28:25 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18dfebfb35a8f45f52ec961615f102607858d20fa48cc66d2b29225c9642a0f2`  
		Last Modified: Wed, 09 Feb 2022 14:28:25 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:712a35dd10725b5d8b6c55235638512bae5e3f33553578ee34182bb664c413a4`  
		Last Modified: Wed, 09 Feb 2022 14:28:25 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:842429c8e7997e5d0455ed2cdd37856f1caddc8f07913623d0d1de313c7c75a9`  
		Last Modified: Wed, 09 Feb 2022 14:28:30 GMT  
		Size: 25.7 MB (25700843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f724804f007d606a9b3ef21df6efbede87da7e499e740b09cdb131cd840e245e`  
		Last Modified: Wed, 09 Feb 2022 14:28:22 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9089a4c47de35611de02ff572f618dd2020421763479d5b63e3215eefdee80`  
		Last Modified: Wed, 09 Feb 2022 14:28:23 GMT  
		Size: 534.7 KB (534739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8912491cfd01cfac373b5a2024eb0c23aeb5e67cc3c008628daa45a1a33cd91b`  
		Last Modified: Fri, 11 Feb 2022 01:44:09 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:156cfd73b0257283ed2936f904cfd3a36e3058e4c64e2d4a543458d25bf8cb2e`  
		Last Modified: Fri, 11 Feb 2022 01:46:41 GMT  
		Size: 145.7 MB (145650027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317730e168a7e6d466975131c3c1c88bd6a82646b57dcc9afda8c72b3c9186d3`  
		Last Modified: Fri, 11 Feb 2022 01:44:09 GMT  
		Size: 1.5 KB (1531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
