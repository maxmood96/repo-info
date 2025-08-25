## `caddy:builder-windowsservercore-ltsc2025`

```console
$ docker pull caddy@sha256:c8f1420ef1f3b2c6beee3989c77169c5b35e505098aecbd8cdf91fa99cc1342e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `caddy:builder-windowsservercore-ltsc2025` - windows version 10.0.26100.4946; amd64

```console
$ docker pull caddy@sha256:f0ecd5bc38691c997cfbb4eaff5bede8b9d25421e5a2fb78b50ac5fbf79f08f5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3615224351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:818b87c61031d564c20e4c7aadd128b369ac69af5472854d710e6709eec622c5`
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
# Mon, 25 Aug 2025 19:56:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Aug 2025 19:56:35 GMT
ENV XCADDY_VERSION=v0.4.5
# Mon, 25 Aug 2025 19:56:36 GMT
ENV CADDY_VERSION=v2.10.2
# Mon, 25 Aug 2025 19:56:37 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Aug 2025 19:56:47 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 25 Aug 2025 19:56:49 GMT
WORKDIR C:\
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
	-	`sha256:8bb8523736186869f7a49f95f8b318bee25824ebbb010838d15db88667b969e3`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb124c01828ece301417db645f6bd33502d9fa4004bbabb93d8483d9adee73fc`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc48728b561dbd7581689079fb9e459be5b1b835c2a19d3e6ad8d63472b2b7b4`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7009143406fac9c3402bce23cf7487a8d83bf93fd0dacf936aa17661011450dd`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a06a632575ebdb5c471cc6aeed6865b4ed1bda3ead85aaa00ed5488712d68f3`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 2.3 MB (2324141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7cb76a0655e886937e45d30114efbcbb8b7dcf4f622e834abea3396c37a8494`  
		Last Modified: Mon, 25 Aug 2025 19:57:03 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
