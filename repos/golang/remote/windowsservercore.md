## `golang:windowsservercore`

```console
$ docker pull golang@sha256:7d55892f0b66b2e2cf2379bd09d9c6d3e731244a938ed88082401a918bcce55d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `golang:windowsservercore` - windows version 10.0.26100.4946; amd64

```console
$ docker pull golang@sha256:7067b4ccc0fb05bdb3584ced31e3724c0e91bfcf098041b75bff0397501e1846
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3612970966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb442f143ed1228d0190e9ccfe21a448e6a6d55a9968164da08d8ff473ccf115`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Wed, 03 Sep 2025 18:54:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Sep 2025 18:54:11 GMT
ENV GIT_VERSION=2.48.1
# Wed, 03 Sep 2025 18:54:12 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 03 Sep 2025 18:54:13 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 03 Sep 2025 18:54:14 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 03 Sep 2025 18:54:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 03 Sep 2025 18:54:32 GMT
ENV GOPATH=C:\go
# Wed, 03 Sep 2025 18:54:40 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 03 Sep 2025 18:54:41 GMT
ENV GOLANG_VERSION=1.25.1
# Wed, 03 Sep 2025 18:56:23 GMT
RUN $url = 'https://dl.google.com/go/go1.25.1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '4a974de310e7ee1d523d2fcedb114ba5fa75408c98eb3652023e55ccf3fa7cab'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 03 Sep 2025 18:56:24 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f495bbd35ca8371e7ec2ae6c370e5682cb4115fab536c9282a01229768afc4`  
		Last Modified: Wed, 03 Sep 2025 18:59:51 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43216771afdda44565d262c41cb4e449d6be29edd33e3e8bb55360a9da328d53`  
		Last Modified: Wed, 03 Sep 2025 18:59:51 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a19e361e0b9d583cb99cba5f0bc5e433894e70eb6bcfd03408daa7e0513885`  
		Last Modified: Wed, 03 Sep 2025 18:59:51 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc3cdf339cc1b15f23e17648fb50e6dfa0a82edee34b12a0edc43f3304b8f8c`  
		Last Modified: Wed, 03 Sep 2025 18:59:51 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a59f12ead65b3b97d30afe4e69cd209e7eb29dadd77a965d9616f7e60f3ccab`  
		Last Modified: Wed, 03 Sep 2025 18:59:51 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1920035ea1acffe071d8a1a6e540cbc05a2227b03f219f5f60cfeea15d4f5a2`  
		Last Modified: Wed, 03 Sep 2025 18:59:55 GMT  
		Size: 51.3 MB (51255221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6209f159116204b114dc0a4ee1f3c7ab824b77eeb134fa89a6c4db43f33457ab`  
		Last Modified: Wed, 03 Sep 2025 18:59:51 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520317e2ec06ea76cc88364e82fab6db4e97c7a1f8841409d5bad1ed377db1ab`  
		Last Modified: Wed, 03 Sep 2025 18:59:51 GMT  
		Size: 376.9 KB (376942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b200dd9d7936388cee63e986533a5e6f4c5cd3e17fd0cd0c8ce10689499288`  
		Last Modified: Wed, 03 Sep 2025 18:59:51 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e66a3739df18124532e005e6e2f676fee662b557add1fb9f756e2fa1aa3a235`  
		Last Modified: Wed, 03 Sep 2025 19:00:01 GMT  
		Size: 62.5 MB (62497761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2d4085daa7946c18453d6431bca13352e3a418408ce342846fab2a53a4750e3`  
		Last Modified: Wed, 03 Sep 2025 18:59:55 GMT  
		Size: 1.5 KB (1466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:windowsservercore` - windows version 10.0.20348.4052; amd64

```console
$ docker pull golang@sha256:e16851b2650d1ff8e921502d0ccb1188ab4ccbc79dbd6e572539e2145bba4ea4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2395537717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558c57b336c45927bb34dfb332351e40f09d768acaca8918fbd0e42a548d50ab`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Wed, 03 Sep 2025 18:48:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Sep 2025 18:48:02 GMT
ENV GIT_VERSION=2.48.1
# Wed, 03 Sep 2025 18:48:03 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 03 Sep 2025 18:48:04 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 03 Sep 2025 18:48:05 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 03 Sep 2025 18:48:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 03 Sep 2025 18:48:40 GMT
ENV GOPATH=C:\go
# Wed, 03 Sep 2025 18:48:48 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 03 Sep 2025 18:48:49 GMT
ENV GOLANG_VERSION=1.25.1
# Wed, 03 Sep 2025 18:50:54 GMT
RUN $url = 'https://dl.google.com/go/go1.25.1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '4a974de310e7ee1d523d2fcedb114ba5fa75408c98eb3652023e55ccf3fa7cab'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 03 Sep 2025 18:50:55 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55b4ef7b22d881631bb814f6dc5455e9f552bb1d067b28ce008be2a063e63ce`  
		Last Modified: Wed, 03 Sep 2025 18:51:43 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32dfba081f0cce40b460d95e533de00858b144d90786ce8706d7f37c7e88dc38`  
		Last Modified: Wed, 03 Sep 2025 18:51:43 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c29706c8046c63eb160ce1b8f6f1c8113d6450c5a6081812ba1b184665d1df`  
		Last Modified: Wed, 03 Sep 2025 18:51:43 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49bf7117a3c722b63bafbe893751fbc9d1f270e9d8a8d02545624993b284fe69`  
		Last Modified: Wed, 03 Sep 2025 18:51:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2416bbf64eff4950370f959628f2ae2bb16ec69741dd79ff9d00d10696a3fcb`  
		Last Modified: Wed, 03 Sep 2025 18:51:43 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecbd241fa90be05d0b54c20c957bb16af4c997344a9ea74ea6076b2ae351c5ea`  
		Last Modified: Wed, 03 Sep 2025 18:51:52 GMT  
		Size: 51.2 MB (51209907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7662d22bdccac02850ff814f6a0bdc0d4d1f409dfc5ecae417260b5afa857f67`  
		Last Modified: Wed, 03 Sep 2025 18:51:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79219794d49356813ef838e353f4bf0f6b5b60f8d110b660146fc95e8592f363`  
		Last Modified: Wed, 03 Sep 2025 18:51:43 GMT  
		Size: 348.3 KB (348313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4de42a340b60b1f23809e958183e2f7ae8ebcc27c28cbfa4cbcf8c6e1d82890`  
		Last Modified: Wed, 03 Sep 2025 18:51:43 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b151d32783f0d4f9471f00d851630ba3b26156e93a30191f50084ef4eafe2d90`  
		Last Modified: Wed, 03 Sep 2025 18:51:56 GMT  
		Size: 62.3 MB (62277112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:349e51596a7dbfa83e2250f0505aaeceff684958f862f3d7d67cf01f570577b9`  
		Last Modified: Wed, 03 Sep 2025 18:51:44 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
