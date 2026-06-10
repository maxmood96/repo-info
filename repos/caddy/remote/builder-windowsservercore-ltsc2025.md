## `caddy:builder-windowsservercore-ltsc2025`

```console
$ docker pull caddy@sha256:e68ba79e488cc22be7bd6e59d3617d0ebac39b3c0b570998f089bfa38fd30018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32995; amd64

### `caddy:builder-windowsservercore-ltsc2025` - windows version 10.0.26100.32995; amd64

```console
$ docker pull caddy@sha256:c014d2f376d017f53c92355b44a582432d2d2f9d3b763c194d8d0bb15dd6796c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2403052943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2575c84cb04855e09a14e4c2fb88ac7d178f0bf869fd6f9184e37b457e21c0a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Tue, 09 Jun 2026 22:13:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2026 22:22:06 GMT
ENV GIT_VERSION=2.48.1
# Tue, 09 Jun 2026 22:22:06 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 09 Jun 2026 22:22:07 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 09 Jun 2026 22:22:08 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 09 Jun 2026 22:22:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:22:24 GMT
ENV GOPATH=C:\go
# Tue, 09 Jun 2026 22:22:30 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Jun 2026 22:22:31 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 09 Jun 2026 22:24:09 GMT
RUN $url = 'https://dl.google.com/go/go1.26.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '3ca8fb4630b07c419cbdd51f754e31363cfcfb83b3a5354d9e895c90be2cc345'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:24:10 GMT
WORKDIR C:\go
# Tue, 09 Jun 2026 23:22:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2026 23:22:34 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 09 Jun 2026 23:22:34 GMT
ENV CADDY_VERSION=v2.11.4
# Tue, 09 Jun 2026 23:22:34 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jun 2026 23:22:53 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 09 Jun 2026 23:22:54 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee71d57b2226db82d002abc39a97b7dd144f007db435566364a0285bf115b83`  
		Last Modified: Tue, 09 Jun 2026 18:08:12 GMT  
		Size: 756.1 MB (756083682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde3f87c92fa7d0ae280c09db445ee43c8fe0d6469fc2c7ef39eccb597a279d6`  
		Last Modified: Tue, 09 Jun 2026 22:15:30 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:272b25e4f9b588ef12b114aef37881b37bd4c18f895164f93fedb5b662d1214e`  
		Last Modified: Tue, 09 Jun 2026 22:24:22 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f95bbf2e19b06ae0fafacddcc2311a15a0e674639be5e9face2c87a623c5f6`  
		Last Modified: Tue, 09 Jun 2026 22:24:21 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd99af064001b3271c7db22a640bb6dd5ea71b5c34a6535fcae25a3502b626f9`  
		Last Modified: Tue, 09 Jun 2026 22:24:20 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb86163344ae33bad3e1f715047069c88dc758a5cb0b1bd7309d1be450f95b7`  
		Last Modified: Tue, 09 Jun 2026 22:24:20 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:742b10c70845db0bb2dd0bf72ddb8a8c35425483635824b24bb3e380d7a676f5`  
		Last Modified: Tue, 09 Jun 2026 22:24:26 GMT  
		Size: 51.3 MB (51252538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5946af3e634fa1b8f9f213c3e22f7e86e4318880f7d7f9940df28595a9bf3b`  
		Last Modified: Tue, 09 Jun 2026 22:24:18 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51dca8b428570c892454e9e7c960d09fec5e8cb4d7934dee10c4f27f229182c5`  
		Last Modified: Tue, 09 Jun 2026 22:24:19 GMT  
		Size: 383.5 KB (383489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456b6d42fed7962d0e86f03ef354a2e4c204796bdc66219dac933313cd2194dc`  
		Last Modified: Tue, 09 Jun 2026 22:24:18 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9db39ba4238180e591f9f214b990f235c8a6b6361066df530c7bd042bebd134`  
		Last Modified: Tue, 09 Jun 2026 22:24:30 GMT  
		Size: 69.9 MB (69934339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e77db804920b355a661f85c770aee26cd4a797c68ed868076d88e5533180ebe`  
		Last Modified: Tue, 09 Jun 2026 22:24:19 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1de00644d35002c94f070463e8abd113796da2571659705f0f2704553688603`  
		Last Modified: Tue, 09 Jun 2026 23:23:02 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f06659823c7fb2424007d8a9634047c1b9a1adfa8840ed0a91c5215ce9ea5a`  
		Last Modified: Tue, 09 Jun 2026 23:23:00 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bb43513a07d02d7c193a9d08d429d2e061ac5bb220c6857b54ae4ca555a78c9`  
		Last Modified: Tue, 09 Jun 2026 23:23:00 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf3109a6438db81a2169df15538a8925997140dc33f6253e6a13f3f6a10125d`  
		Last Modified: Tue, 09 Jun 2026 23:23:00 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8ff8b0d96800c2b8aeb9ac79bf85a61cecb8c4e28a6eccd550272829d8b9eb`  
		Last Modified: Tue, 09 Jun 2026 23:23:01 GMT  
		Size: 2.3 MB (2322679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f96924f312b7960def306105f55f61a04ee4a2bb785ec658896667935bddf58b`  
		Last Modified: Tue, 09 Jun 2026 23:23:00 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
