## `golang:1-windowsservercore-1809`

```console
$ docker pull golang@sha256:f8d77af32f7cd1173f2b54baa891f3b21eab67443850dfcc179d1a916a0d7e91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `golang:1-windowsservercore-1809` - windows version 10.0.17763.2300; amd64

```console
$ docker pull golang@sha256:689b482ce8a6b6b2dacc5859ceff69de0366d1bc73077f0b98fbb4e892a9b5ff
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2877355152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821f2fb0cc1102f2f498e2d2325e5813ed6bb22e943088df64723610d67e7eac`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 01:42:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 13:26:17 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Nov 2021 13:26:18 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Nov 2021 13:26:19 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Nov 2021 13:26:20 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Nov 2021 13:27:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Nov 2021 13:27:38 GMT
ENV GOPATH=C:\go
# Wed, 10 Nov 2021 13:28:31 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 03 Dec 2021 22:18:55 GMT
ENV GOLANG_VERSION=1.17.4
# Fri, 03 Dec 2021 22:22:55 GMT
RUN $url = 'https://dl.google.com/go/go1.17.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '903cffeb7c6ab7490b9101086a2b978076bd9356e56369404b9c45dff866da77'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Fri, 03 Dec 2021 22:22:57 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b35c0957cca5902f3108e43a3c2c11250dc754ee0bb43900eb0719b4350f0bc2`  
		Last Modified: Wed, 10 Nov 2021 02:08:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f32622fe466bd678a47b75fa13ebb7781336e6a776a22f424036aa8e91fe1d`  
		Last Modified: Wed, 10 Nov 2021 14:05:07 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d684ea4a6b52df2d3b5c7f7876e3b784ff1def8eb60f9637d920f4e0e7870b`  
		Last Modified: Wed, 10 Nov 2021 14:05:03 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5ff61f0f89258dd1f49b766ef30baddd8f3e3821737778748ba95b52c1a480c`  
		Last Modified: Wed, 10 Nov 2021 14:05:03 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16dc9a497b44a664b28524686ca0e75c6a244af505429f54f80a6aaa96c7af9`  
		Last Modified: Wed, 10 Nov 2021 14:05:04 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e724f5e2b6e2fb2598ad100e7efa9cf30fe013f56537a5587d8e8868ae82d50`  
		Last Modified: Wed, 10 Nov 2021 14:05:09 GMT  
		Size: 25.4 MB (25446198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84e37bf01f689e54241d5e76695c5cbcc3313f3f8a85748e9d086c6cf3e4c3d`  
		Last Modified: Wed, 10 Nov 2021 14:05:00 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f6ed9286b06435dae34f3d3e03f2c62a4415e3703740a83381b4ac0a3d1804`  
		Last Modified: Wed, 10 Nov 2021 14:05:00 GMT  
		Size: 325.4 KB (325448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1108703a40e03daf7603ceb5fbb9f68f924f0dda151989c955960f5fe71f79e3`  
		Last Modified: Fri, 03 Dec 2021 22:53:03 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e95d151623ca427304ced0a78e7b3af9f3c9a690631f72d9a4e6a247d4d1498`  
		Last Modified: Fri, 03 Dec 2021 22:53:50 GMT  
		Size: 145.5 MB (145450792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a90d26ed259dde47ac95a396422bc836c5880287dca3623dec9ed8e54d0748fb`  
		Last Modified: Fri, 03 Dec 2021 22:53:03 GMT  
		Size: 1.6 KB (1557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
