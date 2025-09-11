## `golang:1-windowsservercore-ltsc2025`

```console
$ docker pull golang@sha256:2a7eb9b4f6927ad5450861e2bde6cc1c6a3b1a9e6bc6a7527a7e2c180b1e379f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `golang:1-windowsservercore-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull golang@sha256:249d7e129dd29dc9ccf6c08cd4d8374d4166ded8e8d349859133b4008d978547
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3685574353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc14c8bbb92dd8832bc7de389e1c0c4ad5c75436f4f1e65fe62fcd84693b6001`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 10 Sep 2025 21:48:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:57:48 GMT
ENV GIT_VERSION=2.48.1
# Wed, 10 Sep 2025 21:57:49 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 10 Sep 2025 21:57:50 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 10 Sep 2025 21:57:50 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 10 Sep 2025 21:58:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Sep 2025 21:58:05 GMT
ENV GOPATH=C:\go
# Wed, 10 Sep 2025 21:58:10 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Sep 2025 21:58:11 GMT
ENV GOLANG_VERSION=1.25.1
# Wed, 10 Sep 2025 21:59:36 GMT
RUN $url = 'https://dl.google.com/go/go1.25.1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '4a974de310e7ee1d523d2fcedb114ba5fa75408c98eb3652023e55ccf3fa7cab'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 10 Sep 2025 21:59:37 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b46f99bf24fa286feb298caca522f226b7edcadf9f5fbfe6ced69e99e66309a`  
		Last Modified: Wed, 10 Sep 2025 21:56:35 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf2dd796d25630d4461d102dcabe9e16db6ce77348eef1537a7322babdc323c`  
		Last Modified: Wed, 10 Sep 2025 22:00:30 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2099449ce7d2ed651909c3f67b3eb887ff4e87da2760bac8e8224e20f87faea3`  
		Last Modified: Wed, 10 Sep 2025 22:00:29 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c91db736d99c7fc9a4ba7e72939f80a397a7465f5e4af637dbb4ad81560bb97c`  
		Last Modified: Wed, 10 Sep 2025 22:00:29 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ac511f2fa9abf855a537efdc268a01918e482320739a3a6146afbcec900ce7`  
		Last Modified: Wed, 10 Sep 2025 22:00:29 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cafcfcc002dcb03bb67a598e85f1dea5dbd30a0e6ac2e74bd22154e4837d82b`  
		Last Modified: Wed, 10 Sep 2025 22:00:51 GMT  
		Size: 51.2 MB (51224896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85e368ce57264ebdaa6e43c10d0dda1190d98499487cd6042983867a58fd03a5`  
		Last Modified: Wed, 10 Sep 2025 22:00:29 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798c3f885bd26eb6bcb29389b47d0f6fc22288c40f0a4e9c57cf1395bd70c384`  
		Last Modified: Wed, 10 Sep 2025 22:00:29 GMT  
		Size: 347.2 KB (347244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9e36ce96ecf4b5dfc99df7fefbabd26c0aa1148f51c48e45dc2c9c239dfc75`  
		Last Modified: Wed, 10 Sep 2025 22:00:30 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c7dc663e9a932956563a88ed18e28798f6e3ce15d43ef1cf357da05fc69f1e`  
		Last Modified: Wed, 10 Sep 2025 22:00:36 GMT  
		Size: 62.6 MB (62551755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:860caa661ec23e09a06b57c9c5c8e09927ebdffc36e6725779110dd29128ef1d`  
		Last Modified: Wed, 10 Sep 2025 22:00:29 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
