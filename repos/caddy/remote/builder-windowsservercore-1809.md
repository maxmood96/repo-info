## `caddy:builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:c787d5e767ea86923cc678e70b4bca60106ce18437b7de4e5cf58a0df676478f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4499; amd64

### `caddy:builder-windowsservercore-1809` - windows version 10.0.17763.4499; amd64

```console
$ docker pull caddy@sha256:3b13f405eb98447f060832fe18bb00ae9fdbe9b4d9e54596ceb7b6190aa85a87
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1835935836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4955d0cc2bb1f14834e1b5b877bdb9c5cd5166922677479085fa11a94c15b9a1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Wed, 21 Jun 2023 08:47:17 GMT
RUN Apply image 10.0.17763.4499
# Sat, 24 Jun 2023 00:40:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 24 Jun 2023 01:43:27 GMT
ENV GIT_VERSION=2.23.0
# Sat, 24 Jun 2023 01:43:27 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Sat, 24 Jun 2023 01:43:28 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Sat, 24 Jun 2023 01:43:29 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Sat, 24 Jun 2023 01:44:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Sat, 24 Jun 2023 01:44:10 GMT
ENV GOPATH=C:\go
# Sat, 24 Jun 2023 01:44:35 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 11 Jul 2023 19:17:09 GMT
ENV GOLANG_VERSION=1.19.11
# Tue, 11 Jul 2023 19:19:59 GMT
RUN $url = 'https://dl.google.com/go/go1.19.11.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '25f04babf4ebb51cebca329d3479771b29721433c924c5707f3b0689878d5232'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 11 Jul 2023 19:20:00 GMT
WORKDIR C:\go
# Tue, 11 Jul 2023 19:47:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Jul 2023 19:47:50 GMT
ENV XCADDY_VERSION=v0.3.4
# Tue, 11 Jul 2023 19:47:51 GMT
ENV CADDY_VERSION=v2.6.4
# Tue, 11 Jul 2023 19:47:52 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 11 Jul 2023 19:48:18 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.4/xcaddy_0.3.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('542b4c083852d41081186c79757b66ff3c26248f72ed461dbc038b51687d0a8a8ce8eee69e3b5a1d43360c48b3405b611b940fa378debe98aaa0b3c5aebfa218')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 11 Jul 2023 19:48:19 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:b1471cc22404d036d95728a9c37c1e3f025a1f0a331072c8613e38cf8f7ff1ed`  
		Last Modified: Fri, 23 Jun 2023 02:36:08 GMT  
		Size: 1.7 GB (1650736778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58717a727cd3a756d7c1180dfb74e95d49735ed12628bd25d2058bc90fa96991`  
		Last Modified: Sat, 24 Jun 2023 01:20:03 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a79a43ac964b3160743c550c9514dabd1bfdb578ce1f98ba1569afcdb5b2aa`  
		Last Modified: Sat, 24 Jun 2023 02:17:06 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9da1c831ff416b065ef3b3c911e6e718799d3a15880029f13ed9cf7f95ee37`  
		Last Modified: Sat, 24 Jun 2023 02:17:04 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ad5b16346994a16fac54d7922a8f10751100d66867522d457c9facb57f86282`  
		Last Modified: Sat, 24 Jun 2023 02:17:03 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:572af76edd6c5c6c258b07c4f447f3d09704d8763f88055819d2af22689c6db5`  
		Last Modified: Sat, 24 Jun 2023 02:17:03 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb015efe9cd98c291567a50142c06c076ad7ba447081c676b90977800324d2ca`  
		Last Modified: Sat, 24 Jun 2023 02:17:08 GMT  
		Size: 25.4 MB (25409927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af0b7dc6940e13a04697fae793e6a6fd4fe42261b113281e7156faf3835df907`  
		Last Modified: Sat, 24 Jun 2023 02:17:01 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc8a72ee4c9bfd8d7f72b343d46dd1d376708a4190d83f5c122935ad6da6354`  
		Last Modified: Sat, 24 Jun 2023 02:17:01 GMT  
		Size: 275.3 KB (275312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc96c5314e31fec507a418a7cd9128f9931c26c66ae6a172ae6df56183e757b`  
		Last Modified: Tue, 11 Jul 2023 19:29:21 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc81759b5dd289127487435b08289965e9f81523d50564e6ce7f1982182dd0a`  
		Last Modified: Tue, 11 Jul 2023 19:29:56 GMT  
		Size: 157.8 MB (157795049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50dbc45536db9b38bbb7c3ed877ac849b0727085920be18333abc0a37cb3bae3`  
		Last Modified: Tue, 11 Jul 2023 19:29:21 GMT  
		Size: 1.6 KB (1564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b5cc4fcae12f855fc1d3266a88d3088a50f0e5a702ff05ab24bb9e489b8db0`  
		Last Modified: Tue, 11 Jul 2023 19:51:01 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b465ea6624e2a159ad99a0c364903368df49391615e65ec7f8d013bf4868b12e`  
		Last Modified: Tue, 11 Jul 2023 19:50:59 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7965e5030d3fd6c9c49342995773c9b160db55683982dcac8d88c0e4bcb5d10`  
		Last Modified: Tue, 11 Jul 2023 19:50:59 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc25e4b20be3514e569766d20e4a87301f5534ec71d64a550b0416cfe93e5b66`  
		Last Modified: Tue, 11 Jul 2023 19:50:58 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30f24570c4fc20c0ebd702719c6cf01929bab8ba0db886cc638ba1268f5f155`  
		Last Modified: Tue, 11 Jul 2023 19:50:59 GMT  
		Size: 1.7 MB (1700864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1980e9c10bbc298a615ef0285de10f004ecc478231b7fe4f0efac8cb14886517`  
		Last Modified: Tue, 11 Jul 2023 19:50:59 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
