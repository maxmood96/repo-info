## `docker:windowsservercore`

```console
$ docker pull docker@sha256:697cd746ecd91356a3625fe3d2374f27542f61a7c3b51b39de570b4893888314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1787; amd64
	-	windows version 10.0.17763.4499; amd64

### `docker:windowsservercore` - windows version 10.0.20348.1787; amd64

```console
$ docker pull docker@sha256:de358706a07bb41edc508e18f7952c5348ee9ff6c2d1553f48c469e157f09d4d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 GB (1442656485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b62bef66d9042234d979c0f10e4c004e9cf57d080383db101bd24be8d859576`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 14 Jun 2023 17:38:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jun 2023 20:51:51 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 14 Jun 2023 20:51:52 GMT
ENV DOCKER_VERSION=24.0.2
# Wed, 14 Jun 2023 20:51:52 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.2.zip
# Wed, 14 Jun 2023 20:52:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 14 Jun 2023 20:52:24 GMT
ENV DOCKER_BUILDX_VERSION=0.11.0
# Wed, 14 Jun 2023 20:52:25 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.11.0/buildx-v0.11.0.windows-amd64.exe
# Wed, 14 Jun 2023 20:52:25 GMT
ENV DOCKER_BUILDX_SHA256=e314569943a591a097fa9119bf786556a4eb5c710e8ddefa57e95cd95aa7cc7f
# Wed, 14 Jun 2023 20:52:55 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 22 Jun 2023 00:15:04 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.0
# Thu, 22 Jun 2023 00:15:05 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.19.0/docker-compose-windows-x86_64.exe
# Thu, 22 Jun 2023 00:15:06 GMT
ENV DOCKER_COMPOSE_SHA256=dc6bd9c2016bbf7564959249204af044edf57ea4ff40238c5ecb4541a9d41573
# Thu, 22 Jun 2023 00:15:35 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0972ddd233121a2afd2cf1a3eaec49d595cfe6b3ebe19ef3dd492d99784c370f`  
		Last Modified: Wed, 14 Jun 2023 18:17:55 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91e748fba47776a59c90f030f85ac47a68b36e81bfb09e869a091a006a4d557`  
		Last Modified: Wed, 14 Jun 2023 21:00:45 GMT  
		Size: 315.6 KB (315648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db3ca14bf3f078b2365c3212947d5ade77870808bb4878ca438e32df8a08272`  
		Last Modified: Wed, 14 Jun 2023 21:00:43 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0883b13095d9674ccaa537d9289cec947430bcdd7713143444ff38c5511ed80`  
		Last Modified: Wed, 14 Jun 2023 21:00:43 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0bc4ea91d700aa33030613e121c0657f127c5480fa7eb73e670cfd5a124f7e`  
		Last Modified: Wed, 14 Jun 2023 21:00:46 GMT  
		Size: 17.4 MB (17426561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f209514b7e8282cb83636d0c958c8271d5009c4d66f8accfe81052a7e923ae95`  
		Last Modified: Wed, 14 Jun 2023 21:00:41 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d5d5341ae73cf0f5b771e1c92ce23e1b749586783f2fc9819c7fa28dfb7ba8`  
		Last Modified: Wed, 14 Jun 2023 21:00:41 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adad07e16c150c14b154f271b6f786f2720fe2970924859681c0590c82d35891`  
		Last Modified: Wed, 14 Jun 2023 21:00:40 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228a0e91f39905f37c75e3251189d9c2cae6b2c4dd2724bcdccee0cfc16f6635`  
		Last Modified: Wed, 14 Jun 2023 21:00:43 GMT  
		Size: 17.9 MB (17859678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda92bd17e71514919d10c1247fb461d4454fba9996cb98d72ac326e36fb758a`  
		Last Modified: Thu, 22 Jun 2023 00:18:22 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc336f2bae2c4a628577330e0842ee0503fb18ae34eb69440f5b53f1bfdbf2bb`  
		Last Modified: Thu, 22 Jun 2023 00:18:22 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db729a1c75f6e54ca24f7903d49cb1fcb02fe2d2aeaa2335532cc4b8b000825`  
		Last Modified: Thu, 22 Jun 2023 00:18:22 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb84aabee6be0b66d519024923f5641f9e61acd1abd9c0dc4f609a1ab521a46`  
		Last Modified: Thu, 22 Jun 2023 00:18:27 GMT  
		Size: 18.4 MB (18443242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.4499; amd64

```console
$ docker pull docker@sha256:e01e6bcb78aef841405ec73be1359d565646335b1477a5df6b61d059938a2703
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1704673105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64361cb6937bc0f4bf390254bd23d2d0822b375bfde12fa35f765730d1131452`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 14 Jun 2023 17:39:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jun 2023 20:54:07 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 14 Jun 2023 20:54:08 GMT
ENV DOCKER_VERSION=24.0.2
# Wed, 14 Jun 2023 20:54:08 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.2.zip
# Wed, 14 Jun 2023 20:54:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 14 Jun 2023 20:54:43 GMT
ENV DOCKER_BUILDX_VERSION=0.11.0
# Wed, 14 Jun 2023 20:54:43 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.11.0/buildx-v0.11.0.windows-amd64.exe
# Wed, 14 Jun 2023 20:54:44 GMT
ENV DOCKER_BUILDX_SHA256=e314569943a591a097fa9119bf786556a4eb5c710e8ddefa57e95cd95aa7cc7f
# Wed, 14 Jun 2023 20:55:52 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 22 Jun 2023 00:15:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.0
# Thu, 22 Jun 2023 00:15:43 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.19.0/docker-compose-windows-x86_64.exe
# Thu, 22 Jun 2023 00:15:44 GMT
ENV DOCKER_COMPOSE_SHA256=dc6bd9c2016bbf7564959249204af044edf57ea4ff40238c5ecb4541a9d41573
# Thu, 22 Jun 2023 00:16:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b712a9a082fd391beaa9ca7c8e6c3fda37b0ad8d29cc4663173ed973b961d342`  
		Last Modified: Wed, 14 Jun 2023 18:21:55 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3400214c8a30c3d7483bf7ab4090f8ae083edde78c0ce1e4d8b00614681829ad`  
		Last Modified: Wed, 14 Jun 2023 21:01:07 GMT  
		Size: 303.3 KB (303272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2df2586bfcd266f0f9f5ab8fa4a278fefb8c565d46eeca43f700e2da9ed99f7`  
		Last Modified: Wed, 14 Jun 2023 21:01:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c75dd8e989a08fc1b7a19941c87632c5422ee1742f718aa566b24a54577a2e9b`  
		Last Modified: Wed, 14 Jun 2023 21:01:04 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5543def7c58dfd99a255facdae78d64efa60af5c6d8642ad20aeee21a77981d6`  
		Last Modified: Wed, 14 Jun 2023 21:01:07 GMT  
		Size: 17.4 MB (17426275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44010086bc1ca468f24db0f0b57258a4976d64df7ade83dc4175caba805929a4`  
		Last Modified: Wed, 14 Jun 2023 21:01:02 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c7f394ffa8285f0be37dc0057dfcefeacb017d83e15e842a437214d3ef24e4f`  
		Last Modified: Wed, 14 Jun 2023 21:01:02 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43b0d2b2d81afdfb09cff0fc00769a5051e1f5fe65d6e68429f94a790944d80`  
		Last Modified: Wed, 14 Jun 2023 21:01:02 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27125bbfb35df751800bccc72b2302954830e3bf47b4bcaa589551110ff420d8`  
		Last Modified: Wed, 14 Jun 2023 21:01:05 GMT  
		Size: 17.9 MB (17855911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4732afd1ae45c56c8350c75374c2954212589d748b969ad9abf3cc16b5bdbbf`  
		Last Modified: Thu, 22 Jun 2023 00:18:42 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b50c8502613ec3e1454f66f017a043dc05586fea637b760d13d6185aba538b`  
		Last Modified: Thu, 22 Jun 2023 00:18:42 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b32c6521af07fec7266134dc6e46cdbe6d9b4ba31bb30e34f00788355a2d59e1`  
		Last Modified: Thu, 22 Jun 2023 00:18:42 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158eabd384e338794e2d62757bff0a707747d6fa49753aa7eefad3d8700d5471`  
		Last Modified: Thu, 22 Jun 2023 00:18:47 GMT  
		Size: 18.5 MB (18454910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
