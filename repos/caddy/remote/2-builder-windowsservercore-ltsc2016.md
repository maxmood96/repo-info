## `caddy:2-builder-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:3ba77aff49e3a9dec7fc9bb4648c19c72a5b82ebd3e34bc8c6f8049a4906d4d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4704; amd64

### `caddy:2-builder-windowsservercore-ltsc2016` - windows version 10.0.14393.4704; amd64

```console
$ docker pull caddy@sha256:0365f3c95b018ef38375adb5f79bf25705e4b97f9490f44aa918bd41ddc88469
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 GB (6450073960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:017f807cf59aaa89d3c5608a45db198741c0047045474c1a6696180d21dd03c6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 06 Oct 2021 21:16:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 Oct 2021 12:40:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Oct 2021 12:40:36 GMT
ENV GIT_VERSION=2.23.0
# Wed, 13 Oct 2021 12:40:37 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 13 Oct 2021 12:40:39 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 13 Oct 2021 12:40:40 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 13 Oct 2021 12:43:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Oct 2021 12:43:06 GMT
ENV GOPATH=C:\go
# Wed, 13 Oct 2021 12:44:36 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Oct 2021 12:44:37 GMT
ENV GOLANG_VERSION=1.17.2
# Wed, 13 Oct 2021 12:48:25 GMT
RUN $url = 'https://dl.google.com/go/go1.17.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'fa6da0b829a66f5fab7e4e312fd6aa1b2d8f045c7ecee83b3d00f6fe5306759a'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Oct 2021 12:48:35 GMT
WORKDIR C:\go
# Thu, 14 Oct 2021 01:22:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Oct 2021 01:22:37 GMT
ENV XCADDY_VERSION=v0.2.0
# Thu, 14 Oct 2021 01:22:38 GMT
ENV CADDY_VERSION=v2.4.5
# Thu, 14 Oct 2021 01:22:39 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 14 Oct 2021 01:23:50 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('233a57384b1f82e9420567da74b4fbd19e898112e43b8447dbdb8ddde15cb4d8a66aea58307ccdda74d37c5e525f0dc563f83d4670aee048842754eee9a3bc2b')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 14 Oct 2021 01:23:51 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0c776a8e8e3c02d360995b7fa26a3fd7c0928965795fac57b69ff07418ab07bf`  
		Size: 2.2 GB (2202780626 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6974b1bd85ba3f9ce16d86231eced43f720fed9c13411d37584dfe7193bcde60`  
		Last Modified: Wed, 13 Oct 2021 13:27:57 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7a41ff4b4f042e62d5c92f3d77a8b07abbe639615dd3c82c4de466c8f44c67f`  
		Last Modified: Wed, 13 Oct 2021 13:27:56 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c02d7d3f40b11b8450a6f82aaeade52a871f8bd89cd1d93c11889b8d3b0219d3`  
		Last Modified: Wed, 13 Oct 2021 13:27:53 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae238abf6097e7b188fc12cace8753067804d4d7d0ce700e8eb15eb81e841181`  
		Last Modified: Wed, 13 Oct 2021 13:27:52 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63c56aed90b0f1415d6aa0f7b18f321cf1c1706a970f0eb885099a8567a1a7c`  
		Last Modified: Wed, 13 Oct 2021 13:27:52 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a205445ee4eb097496ba6f8c71969d7fb8d13de1c26282953b8c224ed3638480`  
		Last Modified: Wed, 13 Oct 2021 13:28:02 GMT  
		Size: 25.4 MB (25446028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600685d5fe3d37b53026a027c0bc19affe258579d3eed1f34414fa405c1b53da`  
		Last Modified: Wed, 13 Oct 2021 13:27:49 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b24162a37292c04cd6b7382e44872740764fb08f2ee07f10bb4ee1abf1dec69`  
		Last Modified: Wed, 13 Oct 2021 13:27:49 GMT  
		Size: 311.4 KB (311356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d92b26e43860a64e127bb6cfffaf5274778dd5025626791b5a9d36e5ac70305`  
		Last Modified: Wed, 13 Oct 2021 13:27:49 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d052710e2b42d7bddbf15d7dbb22365c8ab7bcdfb0bae6553cc12553c4fc0dc`  
		Last Modified: Wed, 13 Oct 2021 13:28:34 GMT  
		Size: 149.9 MB (149883054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfc602ae61702d3bfeb1500c4188c0fbcbd41f89d633ef14968d0a5ed1c5f8e5`  
		Last Modified: Wed, 13 Oct 2021 13:27:49 GMT  
		Size: 1.6 KB (1565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f2f05e8b995693b5f8f38be1571d8fce75e356011f4a0232cc812fdd1e1367`  
		Last Modified: Thu, 14 Oct 2021 01:25:50 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fafa6ae65d6daccd791ddb813acdeb6bbd3c9623aefd647eb8084bbb7aaf3afa`  
		Last Modified: Thu, 14 Oct 2021 01:25:47 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87255e5c150e5f38b9e9006ac27eb533cb04b3678e7b9c03a1dbe1366d3ec3bc`  
		Last Modified: Thu, 14 Oct 2021 01:25:47 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f969a272f1695d3c74909abaad5504762a259895af8b4ba6df000856ed9695`  
		Last Modified: Thu, 14 Oct 2021 01:25:47 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b655cb94aaa437a1357529b99aa1207c1a634c7a37aa2798c1399f868fa035`  
		Last Modified: Thu, 14 Oct 2021 01:25:48 GMT  
		Size: 1.6 MB (1649064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6050999d4367152864f9202b4d07df93c8477740f3c788a3b711a12b580770f`  
		Last Modified: Thu, 14 Oct 2021 01:25:47 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
