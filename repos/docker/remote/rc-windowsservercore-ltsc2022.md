## `docker:rc-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:fabef936a13b60535e618b61abd2c496958ebfbaa8889511f16821ec50140ad4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2849; amd64

### `docker:rc-windowsservercore-ltsc2022` - windows version 10.0.20348.2849; amd64

```console
$ docker pull docker@sha256:1ff2799ac09b4ce75e4f1dfe67f311113c7a76e35b269c780a51d58b0112d6c8
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2311333450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d54eab817dfb2319f089cc69d7d12ffbbdef92d3a2322480d569013d44443f9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Fri, 15 Nov 2024 23:13:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 15 Nov 2024 23:13:54 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 15 Nov 2024 23:13:54 GMT
ENV DOCKER_VERSION=27.4.0-rc.1
# Fri, 15 Nov 2024 23:13:55 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-27.4.0-rc.1.zip
# Fri, 15 Nov 2024 23:14:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 15 Nov 2024 23:14:06 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 15 Nov 2024 23:14:06 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Fri, 15 Nov 2024 23:14:07 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Fri, 15 Nov 2024 23:14:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 15 Nov 2024 23:14:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.3
# Fri, 15 Nov 2024 23:14:15 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-windows-x86_64.exe
# Fri, 15 Nov 2024 23:14:16 GMT
ENV DOCKER_COMPOSE_SHA256=30be0d2d5df4d032ffeee3f8c5e6dccc2ef1b2911732055778c3584e9e69bb4b
# Fri, 15 Nov 2024 23:14:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb30caa48a9b2b5fa6d0bb3777d8155b72ab29f399513addb0159ad150c9916`  
		Last Modified: Fri, 15 Nov 2024 23:14:28 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa522ccafa7da6f922233a2ac19431c1ec29fc2a2126d8aa9c5c54e0c23f66ab`  
		Last Modified: Fri, 15 Nov 2024 23:14:28 GMT  
		Size: 380.0 KB (380026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef8135fa404f989254520a006e57f758bd7970fa5e9b47776f584aa69ddc22a`  
		Last Modified: Fri, 15 Nov 2024 23:14:27 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7b4077c55730183c3957e3bfe669d2c45ee66053b16a8a7d65341c7a3700edc`  
		Last Modified: Fri, 15 Nov 2024 23:14:27 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a07515161205f3db76f0ee8f7b920e52e16b9bbf6bde72f9dcd008aec72e4bb`  
		Last Modified: Fri, 15 Nov 2024 23:14:28 GMT  
		Size: 19.0 MB (19013790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8664628100841bdf760e1bc0d78fedce1559305950e28939cebdff9d5122afba`  
		Last Modified: Fri, 15 Nov 2024 23:14:26 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b4b274f725c4daa3a130e26821c826d5e09266aaf064e44701e1700c7e1d00`  
		Last Modified: Fri, 15 Nov 2024 23:14:26 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac20bdb4d034818d752e4f42aa67131e4d6ac1b9e6beb1ff3eca51849a5fb0f5`  
		Last Modified: Fri, 15 Nov 2024 23:14:26 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35d67062f6cb5ecbd3d60a04b8970bfa0eaa64b716b25907f4dcefc96a895f9`  
		Last Modified: Fri, 15 Nov 2024 23:14:28 GMT  
		Size: 19.4 MB (19431153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e79af436c60c00fe07a8c94cf2f5328637aa209d3ac713ff30aa102abc50672`  
		Last Modified: Fri, 15 Nov 2024 23:14:25 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c16a585f449c5a954123b095672ce9d057fdf601db84cab9ee49c2b926937e7a`  
		Last Modified: Fri, 15 Nov 2024 23:14:25 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3bc8c0a533d661c7872a0942ae62eee1ee0b354c933fe118924c381cef9b17`  
		Last Modified: Fri, 15 Nov 2024 23:14:25 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:352b173d3d28ba219a083811aa890f38d58e4223e621c0b1d447cb04420ec9b4`  
		Last Modified: Fri, 15 Nov 2024 23:14:28 GMT  
		Size: 20.0 MB (20012643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
