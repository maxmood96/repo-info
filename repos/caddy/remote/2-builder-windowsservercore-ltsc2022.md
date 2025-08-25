## `caddy:2-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:f3fcc4c5efa8823e03e7be22f1a617cc774c603b0d8f168c048688337bdeb715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `caddy:2-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull caddy@sha256:fae8c3555cf3840ff8637313f178c0317b41466226312ea50a9d597b377a982b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2397840105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5006347b108bafda0318a83f34338f8ef74ab52d118e9d335f14fcd1870a70a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Wed, 13 Aug 2025 18:06:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Aug 2025 18:06:54 GMT
ENV GIT_VERSION=2.48.1
# Wed, 13 Aug 2025 18:06:55 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 13 Aug 2025 18:06:56 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 13 Aug 2025 18:06:56 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 13 Aug 2025 18:07:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Aug 2025 18:07:11 GMT
ENV GOPATH=C:\go
# Wed, 13 Aug 2025 18:07:17 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Aug 2025 18:07:18 GMT
ENV GOLANG_VERSION=1.25.0
# Wed, 13 Aug 2025 18:08:48 GMT
RUN $url = 'https://dl.google.com/go/go1.25.0.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '89efb4f9b30812eee083cc1770fdd2913c14d301064f6454851428f9707d190b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Aug 2025 18:08:49 GMT
WORKDIR C:\go
# Mon, 25 Aug 2025 19:49:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Aug 2025 19:49:53 GMT
ENV XCADDY_VERSION=v0.4.5
# Mon, 25 Aug 2025 19:49:54 GMT
ENV CADDY_VERSION=v2.10.2
# Mon, 25 Aug 2025 19:49:55 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Aug 2025 19:50:12 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 25 Aug 2025 19:50:13 GMT
WORKDIR C:\
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
	-	`sha256:3a9380c184b3613450235fc0562d48b7c1aeb69072e1e188efd675b317114e13`  
		Last Modified: Wed, 13 Aug 2025 18:10:28 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fbb25f9f3a6b5b2e582eb535d357af7f125a5eb0d07250886e7275753bba63b`  
		Last Modified: Wed, 13 Aug 2025 18:10:30 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406b1b81a88b515880f2398d85c50e12604a0be218b43024e6273e174b171a33`  
		Last Modified: Wed, 13 Aug 2025 18:10:31 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe632c05e48eccbb4f65220b5c6cd3d2c38482c1aff7c8a70dedef13c2d8cde3`  
		Last Modified: Wed, 13 Aug 2025 18:10:33 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2281e6abc340f61cf79bb6641d015955f72d05413007591f91ca52d8fcb2020b`  
		Last Modified: Wed, 13 Aug 2025 18:10:33 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6aa352166614c00f1cc5419011f1a211ffaa26ece1203ddb8a7248c0f9dee1`  
		Last Modified: Wed, 13 Aug 2025 18:10:50 GMT  
		Size: 51.2 MB (51199537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36716abacdfd69d4d84aaeb498a02c39e5df07d380dc62c6f93a43dd18bd8b36`  
		Last Modified: Wed, 13 Aug 2025 18:10:33 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992bb304a4c05d05ad6f9fce52e761eaca24471880c19303b2d27362b731cf77`  
		Last Modified: Wed, 13 Aug 2025 18:10:33 GMT  
		Size: 335.3 KB (335287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363744c527b6172af2deba44c4735f38293dd27bc326cde515fa1e40d983cbed`  
		Last Modified: Wed, 13 Aug 2025 18:10:33 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6c232258d56f8ebfb4d22b50309c11595a9cd50805699bb1edc2ff5cac8dc2`  
		Last Modified: Wed, 13 Aug 2025 18:11:01 GMT  
		Size: 62.3 MB (62261944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318c09560fb6a640397158d02fb52738a3d51b23a8f80d35724a4ece31d4cf72`  
		Last Modified: Wed, 13 Aug 2025 18:10:34 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf1f3385040c90c1ee57f2d21940227c7a049f3442ac13a978b145cf185a15f`  
		Last Modified: Mon, 25 Aug 2025 19:50:35 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe569c48af273bca5f90b236956c3823ba707807419d4b3d31037b23731ca95`  
		Last Modified: Mon, 25 Aug 2025 19:50:36 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244ee2fe3346da9436f4b3f9faa2052570d594821c15b4458df33433e70d4cf0`  
		Last Modified: Mon, 25 Aug 2025 19:50:37 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11bbd758a87764c779cea8fe9429c091634198b909b6faadc2c04c4add5049a0`  
		Last Modified: Mon, 25 Aug 2025 19:50:38 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e0dab63cb896e209cbc5b4577e607d35a3df8d9e39d5dca15bc9208710b2ec`  
		Last Modified: Mon, 25 Aug 2025 19:50:40 GMT  
		Size: 2.3 MB (2334479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:769960fd4bcf873320f369a1ea9ae102548c30a01938b0886cbafefe311b4353`  
		Last Modified: Mon, 25 Aug 2025 19:50:40 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
