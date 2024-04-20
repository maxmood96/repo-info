## `docker:25-windowsservercore`

```console
$ docker pull docker@sha256:3054b021960b29b0730af42ee70ec748d73434b6ffe6b2e278838136ebb54205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

### `docker:25-windowsservercore` - windows version 10.0.20348.2402; amd64

```console
$ docker pull docker@sha256:834a1cba53e27a4e1c612bbbfd9dee925b5dc834c461c23be53fdeef31678f35
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2056423565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47bab11fff8032098f94944e244f0f22075e9bf1d73de329350b948d693a1ac8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Fri, 19 Apr 2024 22:50:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 19 Apr 2024 22:51:03 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 19 Apr 2024 22:51:04 GMT
ENV DOCKER_VERSION=25.0.5
# Fri, 19 Apr 2024 22:51:04 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-25.0.5.zip
# Fri, 19 Apr 2024 22:51:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 19 Apr 2024 22:51:22 GMT
ENV DOCKER_BUILDX_VERSION=0.14.0
# Fri, 19 Apr 2024 22:51:23 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.windows-amd64.exe
# Fri, 19 Apr 2024 22:51:23 GMT
ENV DOCKER_BUILDX_SHA256=d43f5008431fb4ffd438d14ea686ed0f9c7ef101f2dfd1f84a5670979aeb39a8
# Fri, 19 Apr 2024 22:51:33 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 19 Apr 2024 22:51:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.26.1
# Fri, 19 Apr 2024 22:51:34 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-windows-x86_64.exe
# Fri, 19 Apr 2024 22:51:35 GMT
ENV DOCKER_COMPOSE_SHA256=d8a386d375ef26a77be0bee97516b0287d93acafb3976806f42e2b76c6904125
# Fri, 19 Apr 2024 22:51:44 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:988efe6d694b22f29607c5edb7b2fde7b1c6783892c11c0f263dc7e024666819`  
		Last Modified: Fri, 19 Apr 2024 22:51:51 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538de3fd1834d7f4be288e4f0f1057bd513485ef0ea31f2392b513a53225590d`  
		Last Modified: Fri, 19 Apr 2024 22:51:51 GMT  
		Size: 495.6 KB (495578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ead6acd9eacad47439682fade01985f21d577bb400b54ee8352f1b35002f49`  
		Last Modified: Fri, 19 Apr 2024 22:51:50 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d5f36b0c3884c52077725af21adec22e5b9268ca17231a4dadb4f46861af461`  
		Last Modified: Fri, 19 Apr 2024 22:51:50 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd7c92952a96c37c66a0339361159d204ec71dcd0f49c818a3be3ddf98ab65b`  
		Last Modified: Fri, 19 Apr 2024 22:51:51 GMT  
		Size: 18.1 MB (18077051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62e52772f9a23bb284484c493cf889837e3d2858714a8701ae9b61c10d17de87`  
		Last Modified: Fri, 19 Apr 2024 22:51:48 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24aeee3cbcdab981b031552b607915d082b8284beea5cdea83bee616c6729827`  
		Last Modified: Fri, 19 Apr 2024 22:51:49 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68eff5ada4267bc3bc5c9fe22b1d741496b013b843db3481df34071ec18b628b`  
		Last Modified: Fri, 19 Apr 2024 22:51:48 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fab41585e8fa939270bc4e8d470b36cbb47e4076d05184c0006f2fb08998a70`  
		Last Modified: Fri, 19 Apr 2024 22:51:50 GMT  
		Size: 18.9 MB (18926977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53415e17e285e61385073c7597ca879094a0a052e8f16dbd1d1cccf018ec6961`  
		Last Modified: Fri, 19 Apr 2024 22:51:47 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff11412ec664eb66145448d9f969bfd7d17c64dc28460040bd02725dbf42738`  
		Last Modified: Fri, 19 Apr 2024 22:51:47 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea5d218622eba1f3d0ff7d56247a0f2cb565eef433f17539d4aa7557cb2d019`  
		Last Modified: Fri, 19 Apr 2024 22:51:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f3a288d235679dd0f4d2d05d02bb0c71a3261459abe157bfe84de1c57950d3`  
		Last Modified: Fri, 19 Apr 2024 22:51:50 GMT  
		Size: 19.5 MB (19538705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:25-windowsservercore` - windows version 10.0.17763.5696; amd64

```console
$ docker pull docker@sha256:c7031f4d62ea0145440a44636ddf1bda8567a73a1a6f35424769785b5635eeaa
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2221511250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b31a524d33f9ec42d5de2593550e7cac9fcffa19f92c7b85c33e2f1d576e080b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Fri, 19 Apr 2024 22:50:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 19 Apr 2024 22:51:51 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 19 Apr 2024 22:51:51 GMT
ENV DOCKER_VERSION=25.0.5
# Fri, 19 Apr 2024 22:51:52 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-25.0.5.zip
# Fri, 19 Apr 2024 22:52:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 19 Apr 2024 22:52:27 GMT
ENV DOCKER_BUILDX_VERSION=0.14.0
# Fri, 19 Apr 2024 22:52:28 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.windows-amd64.exe
# Fri, 19 Apr 2024 22:52:28 GMT
ENV DOCKER_BUILDX_SHA256=d43f5008431fb4ffd438d14ea686ed0f9c7ef101f2dfd1f84a5670979aeb39a8
# Fri, 19 Apr 2024 22:53:01 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 19 Apr 2024 22:53:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.26.1
# Fri, 19 Apr 2024 22:53:02 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-windows-x86_64.exe
# Fri, 19 Apr 2024 22:53:03 GMT
ENV DOCKER_COMPOSE_SHA256=d8a386d375ef26a77be0bee97516b0287d93acafb3976806f42e2b76c6904125
# Fri, 19 Apr 2024 22:53:34 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ab17fec25193059862de403a08b02bc405dca6fd00c08d263efb684291f2b70`  
		Last Modified: Fri, 19 Apr 2024 22:53:40 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0045b6425acf03fa20e0591c5441feb4d9a38f674c571d88a352fc61c33fcdf9`  
		Last Modified: Fri, 19 Apr 2024 22:53:40 GMT  
		Size: 499.2 KB (499169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f217f8a33553b82545cf3d79978eb457ba8842b12bd170af3532681a9414cb90`  
		Last Modified: Fri, 19 Apr 2024 22:53:39 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4392a17da5af67f39d5708aac864b32f19092c46f83e5f467d84e1763e215204`  
		Last Modified: Fri, 19 Apr 2024 22:53:39 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13afe794ebb0b22e7604bc80bb12f89d4d7457b09afddae10a511c90ebfa168`  
		Last Modified: Fri, 19 Apr 2024 22:53:40 GMT  
		Size: 18.1 MB (18090837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c76ee78194b7b8e0a5adc361ce11c0d85b676ca7c95a1019861b6d03cac7f942`  
		Last Modified: Fri, 19 Apr 2024 22:53:38 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9183b76998334bfdf963f7428194afbf759d5cb6a6e776e2d3a19b31d2cd18f3`  
		Last Modified: Fri, 19 Apr 2024 22:53:38 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59df3c950226aea91e855e5138dc546f341eff1509a5d806c103d7d198fe2f3b`  
		Last Modified: Fri, 19 Apr 2024 22:53:37 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a8d453f24d3d471c67434472599aa5f1b5bdca60d3b0eab7b6233d5ff710336`  
		Last Modified: Fri, 19 Apr 2024 22:53:39 GMT  
		Size: 18.9 MB (18935335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de95cf61d16bc2383e07587df2601b47bb87343ed8df63da4df985a2d5761f7`  
		Last Modified: Fri, 19 Apr 2024 22:53:36 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274d3ef5d00bed71b9ef9ba5f0e76c432417a4456b3a229489bf6eaf4d6dc918`  
		Last Modified: Fri, 19 Apr 2024 22:53:36 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee032cb455bd50c83dfb859d61810ce720dc7ac2409b883de220e567a2b88ed`  
		Last Modified: Fri, 19 Apr 2024 22:53:36 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0b02ea82eb0aa8ed735395b5510d09958c60024ced7e143c40735d6f137325`  
		Last Modified: Fri, 19 Apr 2024 22:53:39 GMT  
		Size: 19.5 MB (19546285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
