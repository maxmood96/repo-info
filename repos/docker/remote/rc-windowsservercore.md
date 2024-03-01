## `docker:rc-windowsservercore`

```console
$ docker pull docker@sha256:d959639c417f8634f111718b9d71f8e7f1a9a7acc3efa5af655e1d396fb39868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2322; amd64
	-	windows version 10.0.17763.5458; amd64

### `docker:rc-windowsservercore` - windows version 10.0.20348.2322; amd64

```console
$ docker pull docker@sha256:5e0ab4e78cc0275ee93933bdb34c269cd34e789eb976ea74df0cd39fc9988b01
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1966314026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6005074a70c9f3aca6c58791ed3b97f6d609692e61018c208d989cc56c60dfac`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Thu, 29 Feb 2024 19:48:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 29 Feb 2024 19:49:41 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 29 Feb 2024 19:49:41 GMT
ENV DOCKER_VERSION=26.0.0-rc1
# Thu, 29 Feb 2024 19:49:42 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-26.0.0-rc1.zip
# Thu, 29 Feb 2024 19:49:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 29 Feb 2024 19:49:57 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Thu, 29 Feb 2024 19:49:58 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.windows-amd64.exe
# Thu, 29 Feb 2024 19:49:59 GMT
ENV DOCKER_BUILDX_SHA256=0ff0853a09960ff8f454d5db7253d5d935f5538856ea4985a276cbd1b28a96a5
# Thu, 29 Feb 2024 19:50:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 29 Feb 2024 19:50:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.6
# Thu, 29 Feb 2024 19:50:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-windows-x86_64.exe
# Thu, 29 Feb 2024 19:50:12 GMT
ENV DOCKER_COMPOSE_SHA256=7a25ec49a53320fbe218c59ac7aafb05440725894322d396d4b353ad198b9dff
# Thu, 29 Feb 2024 19:50:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01493a47527a31a425308ebef0402822d7d60621a25761a8b0611100079d2573`  
		Last Modified: Thu, 29 Feb 2024 19:50:31 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e761b34278b9ed76b88a6cbf629e8c598cb05d1472eeb8d3749ef9e2f46f8cd8`  
		Last Modified: Thu, 29 Feb 2024 19:50:31 GMT  
		Size: 494.4 KB (494443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555cf6620c863deaf76b5b9ce72e2fd982eea36066e1e5821dd66dbed0d58545`  
		Last Modified: Thu, 29 Feb 2024 19:50:30 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56189aba926df825522adce56560460a5942adecc259c0943d2724b1609ce672`  
		Last Modified: Thu, 29 Feb 2024 19:50:30 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d972f5268dcced4a3879c131f84a39b5921d805532a448a6f83c105c83ce873a`  
		Last Modified: Thu, 29 Feb 2024 19:50:32 GMT  
		Size: 18.1 MB (18074231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e0f686e596a90ff48a0b03c776483636f845636d90f47bed0083aabf17ff51`  
		Last Modified: Thu, 29 Feb 2024 19:50:28 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c596d83be8070d7a821a081dbe0c46808456574c3982ade6260a12c6eb9d7b`  
		Last Modified: Thu, 29 Feb 2024 19:50:27 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8f4d7466f603f0b7bcdf5779c0b3da6628105d9944105502fc4a4d5f960f67`  
		Last Modified: Thu, 29 Feb 2024 19:50:28 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd59cc80524e1fb000d847e5eba79fb25ce0a02aaf8dc7e92280538d06f9712d`  
		Last Modified: Thu, 29 Feb 2024 19:50:28 GMT  
		Size: 18.0 MB (18017255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce9fdf42e19f50acb56d86fbfa6b5ae64e54e302c2743f792691ceaa7388a8fd`  
		Last Modified: Thu, 29 Feb 2024 19:50:26 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c97e061666294a96cbe2c6271f75b20ffbca9fb7a804b445b75960c5ca8e202`  
		Last Modified: Thu, 29 Feb 2024 19:50:26 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03d0f6de0df20478954708eebf0fcc3b130466ab5a766fe3f94d0db3890556d4`  
		Last Modified: Thu, 29 Feb 2024 19:50:26 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a66ee6c102909e542284916cb028ccf38d53740ad7b8d5fce42fa0a7643b4c`  
		Last Modified: Thu, 29 Feb 2024 19:50:28 GMT  
		Size: 19.1 MB (19062286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:rc-windowsservercore` - windows version 10.0.17763.5458; amd64

```console
$ docker pull docker@sha256:b9a6db8a939e75a309f69f715c08277e88eaae03d6fca652a53321496e3e9e58
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2136122417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:916975f1adcf2a6904c0742edb87a50bdf0459380c7d1df17816f61a6a4f664c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Thu, 29 Feb 2024 19:49:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 29 Feb 2024 19:51:11 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 29 Feb 2024 19:51:11 GMT
ENV DOCKER_VERSION=26.0.0-rc1
# Thu, 29 Feb 2024 19:51:12 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-26.0.0-rc1.zip
# Thu, 29 Feb 2024 19:51:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 29 Feb 2024 19:51:46 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Thu, 29 Feb 2024 19:51:46 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.windows-amd64.exe
# Thu, 29 Feb 2024 19:51:47 GMT
ENV DOCKER_BUILDX_SHA256=0ff0853a09960ff8f454d5db7253d5d935f5538856ea4985a276cbd1b28a96a5
# Thu, 29 Feb 2024 19:52:13 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 29 Feb 2024 19:52:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.6
# Thu, 29 Feb 2024 19:52:14 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-windows-x86_64.exe
# Thu, 29 Feb 2024 19:52:14 GMT
ENV DOCKER_COMPOSE_SHA256=7a25ec49a53320fbe218c59ac7aafb05440725894322d396d4b353ad198b9dff
# Thu, 29 Feb 2024 19:52:40 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f5408caf6edeb3611704fe433ccc4327f0a38044dedc14d8b06945131df249a`  
		Last Modified: Thu, 29 Feb 2024 19:52:46 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a6e7d06faa25cb45d77ac6ec3b70667b6c190fe45eed49f756e0c5f3234b646`  
		Last Modified: Thu, 29 Feb 2024 19:52:47 GMT  
		Size: 494.1 KB (494089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f30813434f55ad5b6ae89787c63f3d9561900040041e1a2f7547f54c457da8fc`  
		Last Modified: Thu, 29 Feb 2024 19:52:45 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9744edcf3c9c5306d48e521a1d0ecd15a2e104d08537cec764eb0442bd44135`  
		Last Modified: Thu, 29 Feb 2024 19:52:45 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed057cc64a8639acd7afd8355158c857880ce1a1766c16fe4bf826a21a5c53cf`  
		Last Modified: Thu, 29 Feb 2024 19:52:47 GMT  
		Size: 18.1 MB (18087839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b149241266254072ffc6cae56df1319daabd8665eb189dc554d02dc1164bf9`  
		Last Modified: Thu, 29 Feb 2024 19:52:44 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c3d4f97b37631d27ed2317a36b223e5bfd66fb63710d310f61343637585fa1`  
		Last Modified: Thu, 29 Feb 2024 19:52:44 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b299804d46a2afd563d5b0203905825b9788d80b41f18944404550281a5d7ae`  
		Last Modified: Thu, 29 Feb 2024 19:52:44 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb504cf0ef1133d49b3a27a8f9f3f8b5f26168e75a6ad32d839780b5ecc35b9`  
		Last Modified: Thu, 29 Feb 2024 19:52:45 GMT  
		Size: 18.0 MB (18020359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d38ad0c71f50267b25a5762442c555dc9ac1e802f74366188f9c01f6c660fa`  
		Last Modified: Thu, 29 Feb 2024 19:52:42 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f31d14e1d9358e528b2dbe5d93c0c2f66d12f657c397fe55a0fb7b4a1d7356b`  
		Last Modified: Thu, 29 Feb 2024 19:52:43 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9088d0e24002c5052498ab67495d7b8be247da9b9a8894286d57da25b2643c9`  
		Last Modified: Thu, 29 Feb 2024 19:52:42 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea433b3d121df242ae461687f4550ee42aec79d686b77b2731cd95795d82ba3`  
		Last Modified: Thu, 29 Feb 2024 19:52:45 GMT  
		Size: 19.1 MB (19059695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
