## `caddy:2-builder-windowsservercore-ltsc2025`

```console
$ docker pull caddy@sha256:73266310290e46377d7b5caea232b0fa9be3d1e99e3aa2a07f118cf3eb450232
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7462; amd64

### `caddy:2-builder-windowsservercore-ltsc2025` - windows version 10.0.26100.7462; amd64

```console
$ docker pull caddy@sha256:1bbc052bd7bd0e09838111690b4a49890c04b82b57409de5ec4303cd0393eb8a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3369576614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbc4264c41d8cf9138951c59748d9c046e74b5d268757d2c62f6780e31bc1041`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Dec 2025 21:49:56 GMT
RUN Install update 10.0.26100.7462
# Tue, 09 Dec 2025 20:32:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 20:45:22 GMT
ENV GIT_VERSION=2.48.1
# Tue, 09 Dec 2025 20:45:23 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 09 Dec 2025 20:45:23 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 09 Dec 2025 20:45:24 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 09 Dec 2025 20:45:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 09 Dec 2025 20:45:36 GMT
ENV GOPATH=C:\go
# Tue, 09 Dec 2025 20:45:41 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Dec 2025 20:45:42 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 09 Dec 2025 20:46:55 GMT
RUN $url = 'https://dl.google.com/go/go1.25.5.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ae756cce1cb80c819b4fe01b0353807178f532211b47f72d7fa77949de054ebb'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 09 Dec 2025 20:46:56 GMT
WORKDIR C:\go
# Tue, 09 Dec 2025 21:19:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 21:19:22 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 09 Dec 2025 21:19:23 GMT
ENV CADDY_VERSION=v2.10.2
# Tue, 09 Dec 2025 21:19:23 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Dec 2025 21:19:30 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 09 Dec 2025 21:19:30 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Mon, 08 Dec 2025 10:02:12 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890b21ccebaeedf053c6c32fb4fe8d98ab2c60496b12e6b730ac67df9096fc5b`  
		Last Modified: Tue, 09 Dec 2025 19:44:14 GMT  
		Size: 1.0 GB (1037813290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2fe319ee30340452819276b474d727c837b38b988cffead971ab498342327a0`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a65c5945d6a62fba2ec80d5ba8557ff15b9221af5c1a340771dcf96df595b1`  
		Last Modified: Tue, 09 Dec 2025 20:47:20 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9a4fa9c9ac64b71ccc2fabadeecb13af75450cd7e311f804f50e4bd67d2b9f`  
		Last Modified: Tue, 09 Dec 2025 20:47:20 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5077794eb2c12fd6b4cc6e7fac06a6f7efdfe3ede5b40efd0ebd364dc5dcd308`  
		Last Modified: Tue, 09 Dec 2025 20:47:20 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8840b213f30390e857d141451ac0a43281e75242cb2518129c634c2e0c07cc`  
		Last Modified: Tue, 09 Dec 2025 20:47:20 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715838288520ed30f0461c463620eff73bea39c9e8a442ec9bcb47ed1af4377d`  
		Last Modified: Tue, 09 Dec 2025 20:47:26 GMT  
		Size: 51.2 MB (51219379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8149f62c0cdd569980796b1e62b492c262c217cfd51f6651656eb178b9f78061`  
		Last Modified: Tue, 09 Dec 2025 20:47:21 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a31222f73ee68aab83a8205d925974262f03852ffe9bdc5f499cc33961d5cc`  
		Last Modified: Tue, 09 Dec 2025 20:47:21 GMT  
		Size: 343.4 KB (343378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb72f61a5d963bf1ed66d5ba6b41a713c01955422d11000824ff4d9d2e182fc`  
		Last Modified: Tue, 09 Dec 2025 20:47:21 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b6808e90e2265e2c4369b29bd9c548203728aa0f8316616c98696f616e03ef`  
		Last Modified: Tue, 09 Dec 2025 20:47:28 GMT  
		Size: 62.6 MB (62555607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:933ca3a51b8c7d4ca0ffd4e53bd8537791de8a22ba21e328576ee7ff96aab88d`  
		Last Modified: Tue, 09 Dec 2025 20:47:21 GMT  
		Size: 1.5 KB (1470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c43b41d5ab2686577d08094998bf329354aad51081b78fb6bc01598b136427`  
		Last Modified: Tue, 09 Dec 2025 21:19:43 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6ed03d2ad946a64d4fbb5aa43a595907eab9643582bdc7500fb7c33b7a21c63`  
		Last Modified: Tue, 09 Dec 2025 21:19:43 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2d5d08f2b365aa35477df82efd640574f5d9b15dc801375646ccae9125924a`  
		Last Modified: Tue, 09 Dec 2025 21:19:43 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d560e8c4009871bd2211dadd8f3b936b523826a0147485a2b0878002dcecf32f`  
		Last Modified: Tue, 09 Dec 2025 21:19:43 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5055f39f93018e51e821384fba31780e008c7f8329bebdb350aad985f8a9aa2d`  
		Last Modified: Tue, 09 Dec 2025 21:19:43 GMT  
		Size: 2.3 MB (2320611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c004a8814ca3e0b32487499d7209fa376fce7538e830b44bdcb2eeb54c9ebd14`  
		Last Modified: Tue, 09 Dec 2025 21:19:43 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
