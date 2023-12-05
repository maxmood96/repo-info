## `golang:1-windowsservercore-1809`

```console
$ docker pull golang@sha256:cc0934b2374aaa6d95e803eea0dca082239572cd2a75ff4c36430201b27e6299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `golang:1-windowsservercore-1809` - windows version 10.0.17763.5122; amd64

```console
$ docker pull golang@sha256:3fe31a921656b17e43a8fa95ee5079567f1f4931b88380a123277e02e61144fa
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2152604932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:910b1183db563cea5636da56d662c8133276bd1a067de500d1f08d2bf6c4c210`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 01:37:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Nov 2023 02:47:03 GMT
ENV GIT_VERSION=2.23.0
# Thu, 16 Nov 2023 02:47:04 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 16 Nov 2023 02:47:05 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 16 Nov 2023 02:47:06 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 16 Nov 2023 02:48:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 16 Nov 2023 02:48:31 GMT
ENV GOPATH=C:\go
# Thu, 16 Nov 2023 02:49:41 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Dec 2023 20:18:04 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:21:11 GMT
RUN $url = 'https://dl.google.com/go/go1.21.5.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'bbe603cde7c9dee658f45164b4d06de1eff6e6e6b800100824e7c00d56a9a92f'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 05 Dec 2023 20:21:13 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7a1cc914f0f5e059bfdf02906a6e052b1c97cebaf91eb6c2fd835cfddebda2`  
		Last Modified: Thu, 16 Nov 2023 02:26:46 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e901367fac1450f509d3118ada9e004e3613844ebdf91861147a093483930a4`  
		Last Modified: Thu, 16 Nov 2023 03:11:57 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e08004205bd077d8f22b013c70dc2f10796c64fced1eb9927e0055daff2d05d`  
		Last Modified: Thu, 16 Nov 2023 03:11:55 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebc5048afc68ef48e2f2136545e2cccf26bb29eb4926bf4259b370ad55b4e7a`  
		Last Modified: Thu, 16 Nov 2023 03:11:55 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f50fe5c7ef21648f3eaa4304932877a116fcb910b8e9095c779a2fbe6d57f7e`  
		Last Modified: Thu, 16 Nov 2023 03:11:55 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76fe0e37750041d4ede2a0ca3b5245cfe075c3eb2ee27d7ce72ee8c3d7b20cc`  
		Last Modified: Thu, 16 Nov 2023 03:12:00 GMT  
		Size: 25.5 MB (25537512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8097bb9b8778d15dbf89d899653bf1634ec17554e5d84ef1ccfcac8ebf86afe2`  
		Last Modified: Thu, 16 Nov 2023 03:11:53 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b542d31e914d67da86cc5701cdc282ab664dc1170507e3802e22ab3026436a90`  
		Last Modified: Thu, 16 Nov 2023 03:11:53 GMT  
		Size: 263.2 KB (263200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86acdf7d3955fb44136bac433a30ccbbb97863120f270af32659dd65446666c7`  
		Last Modified: Tue, 05 Dec 2023 20:39:22 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1abe126c354944b7db8aa724d8f757167f7c3b36d39f976ef3b1b0d1b1b65ab`  
		Last Modified: Tue, 05 Dec 2023 20:39:41 GMT  
		Size: 69.4 MB (69361283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6338af096e09067ad482a0f4a6df1d1eee5b5595a64ca5f367b94ce27903e284`  
		Last Modified: Tue, 05 Dec 2023 20:39:22 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
