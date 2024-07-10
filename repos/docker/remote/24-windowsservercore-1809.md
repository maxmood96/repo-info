## `docker:24-windowsservercore-1809`

```console
$ docker pull docker@sha256:d6fe41f7c27b1f582e8a05b5a3b7dc8113f50401ef36823e56a8d327bea49573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `docker:24-windowsservercore-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull docker@sha256:485cb698e1ad4b7fc56dc3483bdad4de3b54c35b2c76f25602e85487df96b8c2
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2295196482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8594b0a04ec1045a09a553aab3ade24e0b23062f7c24d24075382bd8f2850b2b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Wed, 10 Jul 2024 17:01:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jul 2024 17:02:11 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Jul 2024 17:02:12 GMT
ENV DOCKER_VERSION=24.0.9
# Wed, 10 Jul 2024 17:02:12 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.9.zip
# Wed, 10 Jul 2024 17:02:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 10 Jul 2024 17:02:39 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Wed, 10 Jul 2024 17:02:40 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.windows-amd64.exe
# Wed, 10 Jul 2024 17:02:40 GMT
ENV DOCKER_BUILDX_SHA256=d28cff3df9fdbb37aa7434edb09d8befe5e90e5ef5887807569b694f25bebd33
# Wed, 10 Jul 2024 17:03:05 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 10 Jul 2024 17:03:06 GMT
ENV DOCKER_COMPOSE_VERSION=2.28.1
# Wed, 10 Jul 2024 17:03:06 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-windows-x86_64.exe
# Wed, 10 Jul 2024 17:03:07 GMT
ENV DOCKER_COMPOSE_SHA256=7dbd8848d9b8dce489c4d2ce1bb4f4b7a3dccb07a08596ae98b85091e1645bcc
# Wed, 10 Jul 2024 17:03:32 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f98e7fe87492b83d7775a348ae0c94412b638ab5bba1a80b03c3a547708acd`  
		Last Modified: Tue, 09 Jul 2024 17:23:28 GMT  
		Size: 587.8 MB (587809033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791880e316d70246454593cfb05bd68dd2b77e6314d6fea7f35f6dad3a0ddf06`  
		Last Modified: Wed, 10 Jul 2024 17:03:42 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39060024e553e3b771f4ae8c5729be08eef5d1e9e179512536b06b2cec67c659`  
		Last Modified: Wed, 10 Jul 2024 17:03:41 GMT  
		Size: 497.6 KB (497607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4af4b5600671a6a579764200ff5ce1c86d5236afc958a6fb24bbed73dc5329d`  
		Last Modified: Wed, 10 Jul 2024 17:03:40 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:031447ffc974f2f40a662d082efb2196781fa5783c94db6500a2d69f5e894928`  
		Last Modified: Wed, 10 Jul 2024 17:03:40 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5a77c1d9a37711acc39ca2289bcf1918b4295d63e4f6d988295e325bf0611f`  
		Last Modified: Wed, 10 Jul 2024 17:03:41 GMT  
		Size: 17.5 MB (17548425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d752c363ad08143099fb43b393a940d72c64d74e92c3545519f5c99c69c869b`  
		Last Modified: Wed, 10 Jul 2024 17:03:38 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7da6681708cd02dc91f2aa1b0b2de39cea762f790aed674e65ba8eee4732f4e`  
		Last Modified: Wed, 10 Jul 2024 17:03:37 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ad5abde98946a576a0279d6eb89e8347ffd448116981b56521c1066bbe7702`  
		Last Modified: Wed, 10 Jul 2024 17:03:38 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f957a7ea90b60df6bbf7a0b999b5fc6150ef533b75014236daedab58b0236f3f`  
		Last Modified: Wed, 10 Jul 2024 17:03:38 GMT  
		Size: 19.0 MB (19037539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f270231c0e4fca77d7c2246773c61fd44b008a5ffdf8d6652a78533cb5a8594`  
		Last Modified: Wed, 10 Jul 2024 17:03:36 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c8c741dcbb9892b592b6f6f89127067f5c2225b3b50943d4902bd94fdde9d8e`  
		Last Modified: Wed, 10 Jul 2024 17:03:36 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:677dfd1d1cf0664dc6eb47e9f9acf9c1960c26b398750d103759956f94775708`  
		Last Modified: Wed, 10 Jul 2024 17:03:36 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9204510faa3c94fc400f42a25ffd526701c3ebded8971bac54dc8c8d2893fb40`  
		Last Modified: Wed, 10 Jul 2024 17:03:38 GMT  
		Size: 19.7 MB (19671826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
