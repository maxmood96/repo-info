## `golang:1-windowsservercore-ltsc2022`

```console
$ docker pull golang@sha256:32b32b93ab4ec1f7371200c4a46738729782dc743640174688dc423bb198ebfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1006; amd64

### `golang:1-windowsservercore-ltsc2022` - windows version 10.0.20348.1006; amd64

```console
$ docker pull golang@sha256:044dca0ee9c1625c640fdc90b2e47b0024039deb7fd6a086fcf31b280666cfcf
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2530919678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86651f8736e15186e4115e73e35607ac6c00c1ff200f2829325dbc5c9ed9910c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 08 Sep 2022 20:30:55 GMT
RUN Install update 10.0.20348.1006
# Wed, 14 Sep 2022 12:09:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 12:48:49 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Sep 2022 12:48:50 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Sep 2022 12:48:51 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Sep 2022 12:48:52 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Sep 2022 12:49:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Sep 2022 12:49:30 GMT
ENV GOPATH=C:\go
# Wed, 14 Sep 2022 12:49:53 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 14 Sep 2022 12:49:54 GMT
ENV GOLANG_VERSION=1.19.1
# Wed, 14 Sep 2022 12:52:51 GMT
RUN $url = 'https://dl.google.com/go/go1.19.1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'b33584c1d93b0e9c783de876b7aa99d3018bdeccd396aeb6d516a74e9d88d55f'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Sep 2022 12:52:53 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4486102fd3820ed9527fa3e7bfefa8305c2f054e65b46dffe9675755e3d8f288`  
		Size: 910.1 MB (910085953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c5da8902b0918fe9bb0d466157622ccaf8209e4becbdd188ec41ecb563c068e6`  
		Last Modified: Wed, 14 Sep 2022 12:41:36 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8b6316baacdbe5997d732fa3555c0cd6f52fd467b41d4d41b596d460cfe8aa`  
		Last Modified: Wed, 14 Sep 2022 13:23:35 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8de847c6f89452694f7278d29e3920062ee79faf74467742e329a71dc1db8805`  
		Last Modified: Wed, 14 Sep 2022 13:23:32 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1a6aca4358241a5ae1012bcd11240db54df9849aa25d07166c302dd3014dee`  
		Last Modified: Wed, 14 Sep 2022 13:23:31 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a0740ce986dad4039bc222ec6cfe798adfe4573d313d4e3583b8694109298e`  
		Last Modified: Wed, 14 Sep 2022 13:23:31 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:256ed2e7f7ad8700539fdcbbfa0a73ce470c9b68aad955ee06135135e35f19d3`  
		Last Modified: Wed, 14 Sep 2022 13:23:39 GMT  
		Size: 25.7 MB (25676400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bde228a76aaef32add4bb50c16be55584a1328125aa2b2436d22da9d311837a4`  
		Last Modified: Wed, 14 Sep 2022 13:23:28 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab59b5ad3cb6d91ad9c3a3064155bffbd0cafff4fa66dc0d04e68d873a23c2c9`  
		Last Modified: Wed, 14 Sep 2022 13:23:29 GMT  
		Size: 526.6 KB (526562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba542d708f2b1feabca84a31213c17f3a8b1f17c2e45e37acac57be1dd2b751`  
		Last Modified: Wed, 14 Sep 2022 13:23:28 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907d5eb41d138b06cd3e9de3f6a3953de34f1f134efe8cd9417231cceee1cd59`  
		Last Modified: Wed, 14 Sep 2022 13:24:12 GMT  
		Size: 157.8 MB (157755822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f58924cb53a26ed63fe6b3cab74ddf85b6b5c25e29fcbf949a2af6c7009c013`  
		Last Modified: Wed, 14 Sep 2022 13:23:28 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
