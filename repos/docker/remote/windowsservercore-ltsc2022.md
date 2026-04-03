## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:7544ccc6e4ea00729bf7d28604a8b6fb4315bdf05d8f441f01793865f20046a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull docker@sha256:ab04187c13089ceac6c8818c2cee7ecaa4e2bcd39577cfe00552451287b6b504
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2037474662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e24418c7a3a82d1da61a8aa6cd06b4a3d16a6fd1812578771b1d9af9cd36f32`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Fri, 03 Apr 2026 16:47:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 03 Apr 2026 16:49:07 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 03 Apr 2026 16:49:08 GMT
ENV DOCKER_VERSION=29.3.1
# Fri, 03 Apr 2026 16:49:09 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.3.1.zip
# Fri, 03 Apr 2026 16:49:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 03 Apr 2026 16:49:34 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 03 Apr 2026 16:49:35 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Fri, 03 Apr 2026 16:49:36 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Fri, 03 Apr 2026 16:50:03 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 03 Apr 2026 16:50:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Fri, 03 Apr 2026 16:50:05 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Fri, 03 Apr 2026 16:50:06 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Fri, 03 Apr 2026 16:50:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ebc372135025e6455cdea33dd82b8909666f97ad0f0b8089e919cf8b924f91`  
		Last Modified: Fri, 03 Apr 2026 16:50:29 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a0847e4437ba3ef85e9d7047c62200d08f8b3a8a0324073b8c84df7f3f7ebd`  
		Last Modified: Fri, 03 Apr 2026 16:50:28 GMT  
		Size: 506.6 KB (506574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb834b3ffd73d9ed8159b55a49c6253d1c85f02ffac59225e3b9079a78dfd48c`  
		Last Modified: Fri, 03 Apr 2026 16:50:27 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78b00d43926aab381c0a1e819e40df628b0aaea20b0bed307acf7ada3e0d982`  
		Last Modified: Fri, 03 Apr 2026 16:50:28 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cad0814bf145decf1ec3cb79bec86b593fb57d01ebee80ac54f51a6af6fc720`  
		Last Modified: Fri, 03 Apr 2026 16:50:29 GMT  
		Size: 19.6 MB (19590099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270311dfd8f5531d6c32b37406f2b41b3e7ff9507a8bb14652d73535bfdd3441`  
		Last Modified: Fri, 03 Apr 2026 16:50:26 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ae99ac7ec1d7ab5a58d53f31b9a42850062421eaec71a4d870507a0c5807dcc`  
		Last Modified: Fri, 03 Apr 2026 16:50:26 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8314d29cc08fe7941d705655bf4b8147b9260ef4948d41c42e276fb722d25291`  
		Last Modified: Fri, 03 Apr 2026 16:50:26 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f0a73598ec6395d9181e8c1b347790635350d4747fb0470ce9362ba194a633`  
		Last Modified: Fri, 03 Apr 2026 16:50:39 GMT  
		Size: 23.4 MB (23437302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2085add922e64596325b1d712784edd2e4140f08996288115cef8e3a9124e354`  
		Last Modified: Fri, 03 Apr 2026 16:50:24 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d126d916f3b83dd6f3e9b0c72322b5aea0fd8dca636eb24a8fcb310d246056`  
		Last Modified: Fri, 03 Apr 2026 16:50:24 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:842d24a00195d53f2b7a645e88c31a5b96671f836f2bfd39d06c6c3227a83d92`  
		Last Modified: Fri, 03 Apr 2026 16:50:24 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c989b6a66281fbd8d67f03b69e1f471e216f3155c0a8bd5119b79c41ee8fab5`  
		Last Modified: Fri, 03 Apr 2026 16:50:26 GMT  
		Size: 11.6 MB (11647528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
