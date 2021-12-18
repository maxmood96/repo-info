## `caddy:2-builder-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:554235bb8c64b095b014b6d830f88b17f0762c420bff1f6abe6e1853518bcba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4825; amd64

### `caddy:2-builder-windowsservercore-ltsc2016` - windows version 10.0.14393.4825; amd64

```console
$ docker pull caddy@sha256:986441e5402d8408a65e413a76af17566390c2051473ba5f8995ea0eada90b5c
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 GB (6451955487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c5474b08ddb9e551b2da8430f0c5388f433fdcc2f744d20462aef54e7cb1c1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 08 Dec 2021 08:38:00 GMT
RUN Install update ltsc2016-amd64
# Sat, 18 Dec 2021 00:22:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 18 Dec 2021 00:22:41 GMT
ENV GIT_VERSION=2.23.0
# Sat, 18 Dec 2021 00:22:42 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Sat, 18 Dec 2021 00:22:43 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Sat, 18 Dec 2021 00:22:44 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Sat, 18 Dec 2021 00:24:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Sat, 18 Dec 2021 00:24:45 GMT
ENV GOPATH=C:\go
# Sat, 18 Dec 2021 00:25:51 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 18 Dec 2021 00:45:00 GMT
ENV GOLANG_VERSION=1.17.5
# Sat, 18 Dec 2021 00:48:57 GMT
RUN $url = 'https://dl.google.com/go/go1.17.5.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '671faf99cd5d81cd7e40936c0a94363c64d654faa0148d2af4bbc262555620b9'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Sat, 18 Dec 2021 00:48:59 GMT
WORKDIR C:\go
# Sat, 18 Dec 2021 07:56:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 18 Dec 2021 07:56:03 GMT
ENV XCADDY_VERSION=v0.2.0
# Sat, 18 Dec 2021 07:56:04 GMT
ENV CADDY_VERSION=v2.4.6
# Sat, 18 Dec 2021 07:56:05 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 18 Dec 2021 07:57:06 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('233a57384b1f82e9420567da74b4fbd19e898112e43b8447dbdb8ddde15cb4d8a66aea58307ccdda74d37c5e525f0dc563f83d4670aee048842754eee9a3bc2b')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Sat, 18 Dec 2021 07:57:07 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2d026d646213ccf73d9f0584941d108253d62e73df2a74e070776884b7b0242b`  
		Size: 2.2 GB (2204728802 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7756a7a3024dbbb7cabda3151e8f8461ae808ae2ad3857f0c9235c5908ff7695`  
		Last Modified: Sat, 18 Dec 2021 01:22:26 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed085eeb0f67ab647ce30dc0ee783df8de1d571c430a88d3ce15c11a5d05be15`  
		Last Modified: Sat, 18 Dec 2021 01:22:25 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a04aa8edbd1b61f0fa86243e7064f8560eb1b8e35bf303a4d2503bbb1d5dde1`  
		Last Modified: Sat, 18 Dec 2021 01:22:22 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bb78b2e65fd6a44aae1b3a98ba2f38960b6832446cc98b2640003b1078e282`  
		Last Modified: Sat, 18 Dec 2021 01:22:22 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd20bdd437ff14a08b9ccc6dbce15b95eb2f8f3a347a0392ff074ab9aa123320`  
		Last Modified: Sat, 18 Dec 2021 01:22:22 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788d8768c001ba1aa83b84957dc3d6fc7be04e0d35240454ec8e36dd8cdb5683`  
		Last Modified: Sat, 18 Dec 2021 01:22:29 GMT  
		Size: 25.4 MB (25427117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f55846325b60c2a45902ea9dc05ce8a2a4997cdf73da1c40989dfb0ca2b102dc`  
		Last Modified: Sat, 18 Dec 2021 01:22:19 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ee386d622d2d0becd206facf979e544b5de665c127e96b69cf04031d59cae7`  
		Last Modified: Sat, 18 Dec 2021 01:22:19 GMT  
		Size: 303.8 KB (303841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c124ac8352370bf5677f2bccb412580b2cbbeea8f28d9efdb93408fcc9d582d3`  
		Last Modified: Sat, 18 Dec 2021 01:30:56 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162ec1b17249dc0f70da327d7154a08ab82e06a1821cdb2ce20eb0f8568b638c`  
		Last Modified: Sat, 18 Dec 2021 01:33:42 GMT  
		Size: 149.9 MB (149864499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bbf2669140e04b7d8e68710be4c8f5bde3ed568fe313a2c3299ac8ccf3a7ea`  
		Last Modified: Sat, 18 Dec 2021 01:30:56 GMT  
		Size: 1.6 KB (1569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8dcc84b1472cb21b168be841be8b6abb9f47df5af361e082b4116e913a1aed2`  
		Last Modified: Sat, 18 Dec 2021 07:58:57 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23dae94d509e617d7affa8a7c5530fb4b44095a8d8033722246ea62e502234dd`  
		Last Modified: Sat, 18 Dec 2021 07:58:54 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60db63fea76ddbf0e32939245adcc0a26969fdd455d0ad329f21c16a1be0e17`  
		Last Modified: Sat, 18 Dec 2021 07:58:54 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da76577f6e1f71c8042562fe80c7307f2297f2b96cbcc30bdb4fbf84b73cc27`  
		Last Modified: Sat, 18 Dec 2021 07:58:54 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97b8180867dec3b0b32749eeaecc604fe1027ea5031b019ccb3b3ad181d2aed`  
		Last Modified: Sat, 18 Dec 2021 07:58:56 GMT  
		Size: 1.6 MB (1627356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be4ee9d6802bf7bf667f804f3fed64de6438ad36be569d8af5f96d72ab5b210c`  
		Last Modified: Sat, 18 Dec 2021 07:58:54 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
