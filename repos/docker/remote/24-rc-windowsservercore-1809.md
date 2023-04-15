## `docker:24-rc-windowsservercore-1809`

```console
$ docker pull docker@sha256:7f93c9f15685a3605daec4ff82c6a6d7cc987801327febb5e3e047eaef6d94ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4252; amd64

### `docker:24-rc-windowsservercore-1809` - windows version 10.0.17763.4252; amd64

```console
$ docker pull docker@sha256:864a50dbde87bad3450be30eec3cfbae8df461a6942595f7d98b1bb61d367174
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2122702372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db33983c0a1103d93d92c847aca1e43fd817578d7d262f766398506b667ac8d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Wed, 05 Apr 2023 00:41:54 GMT
RUN Install update 10.0.17763.4252
# Tue, 11 Apr 2023 23:40:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Apr 2023 03:25:51 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 15 Apr 2023 00:16:45 GMT
ENV DOCKER_VERSION=24.0.0-beta.2
# Sat, 15 Apr 2023 00:16:46 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-24.0.0-beta.2.zip
# Sat, 15 Apr 2023 00:18:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 15 Apr 2023 00:18:01 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Sat, 15 Apr 2023 00:18:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.windows-amd64.exe
# Sat, 15 Apr 2023 00:18:02 GMT
ENV DOCKER_BUILDX_SHA256=e4bb5f70d98be80421bb26b78dd71fe9184a5f94315a6712f487e9eb252ad4f1
# Sat, 15 Apr 2023 00:19:13 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 15 Apr 2023 00:19:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.2
# Sat, 15 Apr 2023 00:19:14 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-windows-x86_64.exe
# Sat, 15 Apr 2023 00:19:15 GMT
ENV DOCKER_COMPOSE_SHA256=0869cfe9d799d511e4eaf87029ed08ea256e7000f312023c062d7ddcadc385db
# Sat, 15 Apr 2023 00:20:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9094c39c4b36a86359abb3da9e9d0d9c69b6930e9c7b308120310d43d63f693`  
		Last Modified: Wed, 12 Apr 2023 00:52:10 GMT  
		Size: 363.3 MB (363347289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9103f1e2cdefe8f16dae9619b88e38aa659abb17276d2362d435ad0721d3bf41`  
		Last Modified: Wed, 12 Apr 2023 00:50:55 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f180306e9d61cdf6a72f401f1f32a79e350f22b096e8dd7910d6afe20e3e23e9`  
		Last Modified: Wed, 12 Apr 2023 04:07:41 GMT  
		Size: 500.1 KB (500143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b65593919d4e9e01a114769c6645f4e7b462bea3769de6ddd209023bfafce8`  
		Last Modified: Sat, 15 Apr 2023 00:21:58 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fe07eedcad3c91a5d706dbaf58f146ee02c67d07bc702a124fec310b46508a`  
		Last Modified: Sat, 15 Apr 2023 00:21:57 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71fad1dcddff9cc4c0c2f8e7faaa14048980f35b69019f08991c35d17a60a20b`  
		Last Modified: Sat, 15 Apr 2023 00:22:00 GMT  
		Size: 17.5 MB (17505264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:178b101af38d008cace3e95c97cf0c7e721cb106de983c51868eeccc2cb3a02c`  
		Last Modified: Sat, 15 Apr 2023 00:21:55 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0388a75fd0f71ca4fc1a872330759b04caaa6e5517462a6a911a5185547e357`  
		Last Modified: Sat, 15 Apr 2023 00:21:55 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a299758752fa19b9eca6c3ea571ffd6f45d30bce36e1d35ed9f58431f354ce`  
		Last Modified: Sat, 15 Apr 2023 00:21:55 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e31ba40ef0433006bce70e16d2fe564c43e2a7031e4e957542e45e7d3a87eb`  
		Last Modified: Sat, 15 Apr 2023 00:21:57 GMT  
		Size: 16.5 MB (16513734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f30cd9ad8bbffaadf928c461a5e1d0ee6f7d1636786e4c5202aaee8d103d2a`  
		Last Modified: Sat, 15 Apr 2023 00:21:53 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ac6840f880f95f48a1526a4e4201c0c5461e84c3469a015c983748ec2b0eb4`  
		Last Modified: Sat, 15 Apr 2023 00:21:53 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c8b2368484cae4746f313702be7070b8e519b68bcca70e23be38e3f15c6d630`  
		Last Modified: Sat, 15 Apr 2023 00:21:53 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956a5289c4dd925043f6297ce8b79318122ec3178ecb39a4c4d79804dcf2b500`  
		Last Modified: Sat, 15 Apr 2023 00:21:57 GMT  
		Size: 16.9 MB (16879345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
