## `golang:1-windowsservercore-ltsc2025`

```console
$ docker pull golang@sha256:447fbda6e56e6f4c92c9f6eb817aef575b5b6a6ba75d04307cd9778b9f3b6de8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `golang:1-windowsservercore-ltsc2025` - windows version 10.0.26100.4946; amd64

```console
$ docker pull golang@sha256:e33da27ea2523f7c43941be2c40c43f67d0993a77822d871f355ab567b1176ed
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3612893630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a964c1474bdce6ee990dc47fffe74e38bdb943ed7955a9d30aa7c63e2911316`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Wed, 13 Aug 2025 18:08:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Aug 2025 18:08:27 GMT
ENV GIT_VERSION=2.48.1
# Wed, 13 Aug 2025 18:08:28 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 13 Aug 2025 18:08:28 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 13 Aug 2025 18:08:29 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 13 Aug 2025 18:08:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Aug 2025 18:08:43 GMT
ENV GOPATH=C:\go
# Wed, 13 Aug 2025 18:08:49 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Aug 2025 18:08:50 GMT
ENV GOLANG_VERSION=1.25.0
# Wed, 13 Aug 2025 18:10:07 GMT
RUN $url = 'https://dl.google.com/go/go1.25.0.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '89efb4f9b30812eee083cc1770fdd2913c14d301064f6454851428f9707d190b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Aug 2025 18:10:07 GMT
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
	-	`sha256:3329feb8c3f471d93f04a4afc376778f359481b9b10abd677ae7f8105b7a1982`  
		Last Modified: Wed, 13 Aug 2025 18:14:06 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b683ebca7e697913d8f93eeb03b85a4924fa297a5830b694441bb31e2ef2a8`  
		Last Modified: Wed, 13 Aug 2025 18:14:07 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27a25a1b355f0af537456d6695b8cbf9c0c5582795add71831072b1f2067593`  
		Last Modified: Wed, 13 Aug 2025 18:14:08 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5469c0152f4c91f8d66bd59239beec913796e4d17d8977dcf67364f6916d3aae`  
		Last Modified: Wed, 13 Aug 2025 18:14:08 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9e732885c916712df386d920174e3f95dcc40377352391c6f5e8ccc9e59be5`  
		Last Modified: Wed, 13 Aug 2025 18:14:09 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9ebf49453f4f127c2dffe22dcb483f4eeef5d0260fe4724472d7fc5b89ecaf`  
		Last Modified: Wed, 13 Aug 2025 18:14:25 GMT  
		Size: 51.2 MB (51223826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b55bb43d7b4377e022452dadea8a547292c78952945e888b4c3a99193a0e78f`  
		Last Modified: Wed, 13 Aug 2025 18:14:09 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec885b71c379ce9bdce0b6477ef6652f6b9d9f566e7e571c9863ba6adb40cede`  
		Last Modified: Wed, 13 Aug 2025 18:14:09 GMT  
		Size: 351.5 KB (351496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e05cdc4ff30cbd5098771fc7b97628d410fe4d7f2afb43e7ddcd5256d51d407`  
		Last Modified: Wed, 13 Aug 2025 18:14:09 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5def4f4469cc1db786df7b6975d1fc3c3bd4c534434e05e676d67edd1f0af9f`  
		Last Modified: Wed, 13 Aug 2025 18:14:22 GMT  
		Size: 62.5 MB (62477144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48dd29c29527d22890d7b81985987d57cceb811888344ca07659b7c0f2e94151`  
		Last Modified: Wed, 13 Aug 2025 18:14:10 GMT  
		Size: 1.5 KB (1466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
