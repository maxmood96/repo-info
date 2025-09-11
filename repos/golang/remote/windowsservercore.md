## `golang:windowsservercore`

```console
$ docker pull golang@sha256:f2149337a7760b90707cdf3d32367153666fd5e67921890ab10366cf458aa14c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `golang:windowsservercore` - windows version 10.0.26100.6584; amd64

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

### `golang:windowsservercore` - windows version 10.0.20348.4171; amd64

```console
$ docker pull golang@sha256:9f19f7b09766eef447ed369bff375e1dbf7a3fdafd41c88285a1fc45f7b4e0e2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2396242998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d45532386504d5bc9261498480a36173075ac9c4df9b969628939b694fe3181`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 10 Sep 2025 20:20:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:54:52 GMT
ENV GIT_VERSION=2.48.1
# Wed, 10 Sep 2025 21:54:53 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 10 Sep 2025 21:54:53 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 10 Sep 2025 21:54:54 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 10 Sep 2025 21:55:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Sep 2025 21:55:06 GMT
ENV GOPATH=C:\go
# Wed, 10 Sep 2025 21:55:10 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Sep 2025 21:55:11 GMT
ENV GOLANG_VERSION=1.25.1
# Wed, 10 Sep 2025 21:56:23 GMT
RUN $url = 'https://dl.google.com/go/go1.25.1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '4a974de310e7ee1d523d2fcedb114ba5fa75408c98eb3652023e55ccf3fa7cab'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 10 Sep 2025 21:56:24 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abbe60f506e392727a189c473ed3077c57345b082b3f502c4e12299121d8a339`  
		Last Modified: Wed, 10 Sep 2025 21:43:44 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0780f8919cba1a4cab8a7ba29ed322c8f02f4f5a9f7ccd940b287fe95ef291a4`  
		Last Modified: Wed, 10 Sep 2025 21:56:53 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6266fc98281dd096b7b5c07d9e4f3327f7b619c4f76fffcc06bd9a13f6cdd1c`  
		Last Modified: Wed, 10 Sep 2025 21:56:53 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a337271158b2ad1912acfd793fb8b962957ec4007131aaa35baa163167805d02`  
		Last Modified: Wed, 10 Sep 2025 21:56:53 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:490e49a4eacd258553a92b4e5dca482fc3703fd140d5c07deb9fffafe3077d56`  
		Last Modified: Wed, 10 Sep 2025 21:56:53 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442a10c171b869fe2be8955c1b4d5b47d944f0cba7308373f951bb61e9ae3828`  
		Last Modified: Wed, 10 Sep 2025 21:56:57 GMT  
		Size: 51.2 MB (51209642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8b3a09b98dad5f38a4d44f0537e62f1c3839f6c25d72587a064c68959948709`  
		Last Modified: Wed, 10 Sep 2025 21:56:53 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9b5632204625748fe85a9db4849e51e2950e2173b5e9c5364ae3e035e6c5f72`  
		Last Modified: Wed, 10 Sep 2025 21:56:54 GMT  
		Size: 338.7 KB (338714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d507ae436722c5fddd93c264c634770e0170030da6ce78634191a2b6072287`  
		Last Modified: Wed, 10 Sep 2025 21:56:54 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ae1fc566a93e2f64edf3f419625066d9b8518a8d3502d777d5693f7a2b9739`  
		Last Modified: Wed, 10 Sep 2025 21:57:11 GMT  
		Size: 62.5 MB (62539040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3c7239ff5e2c3395a2d988584b72bcca962d92caa2ddf55f6db6a50702a4e9`  
		Last Modified: Wed, 10 Sep 2025 21:56:55 GMT  
		Size: 1.5 KB (1473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
