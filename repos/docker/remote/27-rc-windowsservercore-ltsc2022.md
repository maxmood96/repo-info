## `docker:27-rc-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:b551f29dbb2978ce0f343fdcbc737726b67dbbe49417bd38cd742afe6eab8574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2529; amd64

### `docker:27-rc-windowsservercore-ltsc2022` - windows version 10.0.20348.2529; amd64

```console
$ docker pull docker@sha256:21ab5cff190d3d5eac429b931d7f3fe3513984e48a4661b48167aaa511b062dc
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2176439624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f84e035dacb602a5077febc1c3e694f6f60eabe2e6ff5e6ebfd6b98b26cc42`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 19 Jun 2024 19:58:05 GMT
RUN Install update 10.0.20348.2529
# Sat, 22 Jun 2024 00:05:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 22 Jun 2024 00:05:56 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 22 Jun 2024 00:05:57 GMT
ENV DOCKER_VERSION=27.0.0-rc.2
# Sat, 22 Jun 2024 00:05:58 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-27.0.0-rc.2.zip
# Sat, 22 Jun 2024 00:06:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 22 Jun 2024 00:06:08 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Sat, 22 Jun 2024 00:06:09 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.windows-amd64.exe
# Sat, 22 Jun 2024 00:06:09 GMT
ENV DOCKER_BUILDX_SHA256=d28cff3df9fdbb37aa7434edb09d8befe5e90e5ef5887807569b694f25bebd33
# Sat, 22 Jun 2024 00:06:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 22 Jun 2024 00:06:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.2
# Sat, 22 Jun 2024 00:06:18 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-windows-x86_64.exe
# Sat, 22 Jun 2024 00:06:19 GMT
ENV DOCKER_COMPOSE_SHA256=b9878421deeff63bb4685a0ee502fc737429123f68ee40de326cdc9fab800c1d
# Sat, 22 Jun 2024 00:06:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb373ec9afdfc5f09b9380d981e0c61f9c7b48537b887135c7c66810086e705e`  
		Last Modified: Fri, 21 Jun 2024 00:27:54 GMT  
		Size: 729.6 MB (729591500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61be00b302fdff89dfd3e9cc8a540cb432a1a97ea21d55e193d024b12edb0b03`  
		Last Modified: Sat, 22 Jun 2024 00:06:31 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0200d60cc2f4e9bc463ab37346e734caa230abf6f6b60551149e5189f44282f9`  
		Last Modified: Sat, 22 Jun 2024 00:06:31 GMT  
		Size: 348.3 KB (348321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894884c965493599fc7717883c25e8722e528c2a057aaedda11aab379689b0a6`  
		Last Modified: Sat, 22 Jun 2024 00:06:30 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e730370db370364ebc23c12f88019c6dbe4401b730b4015f2456f5f295b1142`  
		Last Modified: Sat, 22 Jun 2024 00:06:30 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e3b068ea9393b3d75ebb94c2ffe16a6cb6ddb9ae6801602c6c5b436c355b6a`  
		Last Modified: Sat, 22 Jun 2024 00:06:33 GMT  
		Size: 19.3 MB (19255899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9696092ae4a4c9b82e368cbd2a0d485ec6392168da6a29cc67166062f0dc9d5b`  
		Last Modified: Sat, 22 Jun 2024 00:06:29 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52d1415ab1b68bbb388fd08d454d2b91ac11e1e9e9ea81e216e06065e8509ee6`  
		Last Modified: Sat, 22 Jun 2024 00:06:29 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06b2eb554009761ba6e50fcd4a72a4ad1b12be7d0fcfe620add04b2d08648ff`  
		Last Modified: Sat, 22 Jun 2024 00:06:29 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a657d088b204df64e07685da9139fc6427a77d2acaa8e4f713401a0c6d565095`  
		Last Modified: Sat, 22 Jun 2024 00:06:31 GMT  
		Size: 19.0 MB (19012006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b878026ff126e677e7b4f964d73a262caeabc013da15cd3da67f102e13f03873`  
		Last Modified: Sat, 22 Jun 2024 00:06:28 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e84ceabf629c73debcd2748c2aa16cbe2207b6907907b388182e9b3a0e16abcb`  
		Last Modified: Sat, 22 Jun 2024 00:06:28 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:917ef098b52d338c6b293fe5e426d0734982d38205df70861516a70aa36ea54c`  
		Last Modified: Sat, 22 Jun 2024 00:06:28 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10a2827efd1f26c7408de06cf9ff914af8fe60db2f77909aa3f8008bf700cfb`  
		Last Modified: Sat, 22 Jun 2024 00:06:31 GMT  
		Size: 19.6 MB (19621490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
