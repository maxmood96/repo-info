## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:ba6a72db8c28e44c4ab93c65fa3767832632cb0c3e8205fd1dea88f399b24817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2582; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.2582; amd64

```console
$ docker pull docker@sha256:7dc77761f3d7850b3738413bcc16de7cef20d54946747c5637648c779a5716f7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2198112296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d98b5b8fcf4d301cf14531dd4b8aa36f2b3d88ebcde7934fcd94bfd779e50729`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 03 Jul 2024 10:07:02 GMT
RUN Install update 10.0.20348.2582
# Mon, 22 Jul 2024 22:08:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 22 Jul 2024 22:09:18 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 22 Jul 2024 22:09:19 GMT
ENV DOCKER_VERSION=27.1.0
# Mon, 22 Jul 2024 22:09:20 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.1.0.zip
# Mon, 22 Jul 2024 22:09:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 22 Jul 2024 22:09:42 GMT
ENV DOCKER_BUILDX_VERSION=0.16.1
# Mon, 22 Jul 2024 22:09:43 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.windows-amd64.exe
# Mon, 22 Jul 2024 22:09:45 GMT
ENV DOCKER_BUILDX_SHA256=34b8bd302364e9df99ebcd86658eae6ade175baf8baf6e74123ae04fcb2675c3
# Mon, 22 Jul 2024 22:09:55 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 22 Jul 2024 22:09:56 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.0
# Mon, 22 Jul 2024 22:09:57 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-windows-x86_64.exe
# Mon, 22 Jul 2024 22:09:58 GMT
ENV DOCKER_COMPOSE_SHA256=3dc98cacf0e0a05d8a714cc729827c062ff7ec13ffcd626e7b3767b362ce9b65
# Mon, 22 Jul 2024 22:10:12 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0206d135152eb909f50159d6ca348a5aead199afacbafc000b770c1b0720f6`  
		Last Modified: Tue, 09 Jul 2024 18:30:31 GMT  
		Size: 751.0 MB (751001543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7606422d7e4e8f03b537de3ed2a9944972621129a77b94e56734dfffa9d0fa69`  
		Last Modified: Mon, 22 Jul 2024 22:10:17 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af2cdbd39c43a7ecb7d8ecea60aebddc3aeb0a01e19e67943656193c1910cf3`  
		Last Modified: Mon, 22 Jul 2024 22:10:17 GMT  
		Size: 360.2 KB (360178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d630c7c9e9d67cbe2f3626a9a62c4e5a935caa131a79f61119e0d37bdfe45ad`  
		Last Modified: Mon, 22 Jul 2024 22:10:16 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a5f3034ce22f680b28095b77741b6442dfff0da5717eb513afc935ea7faa52`  
		Last Modified: Mon, 22 Jul 2024 22:10:16 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c884f58e8645d97f2afad377da9f3b997a8ece1399339736be8121234269a97`  
		Last Modified: Mon, 22 Jul 2024 22:10:18 GMT  
		Size: 19.3 MB (19258242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0bd37a62f68c78b340f0bc98ecdcfc00a9e58564df2a70c9143e0d98300dc0`  
		Last Modified: Mon, 22 Jul 2024 22:10:15 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d12d1ab561447da15353ef210acf3f904c6f56a659af417bf53e38725ed3454`  
		Last Modified: Mon, 22 Jul 2024 22:10:15 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb9bfef3f8a3001e3f69bdf7ff31d2e4280b9df7b4989b4a506033ea574c595`  
		Last Modified: Mon, 22 Jul 2024 22:10:15 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854704c5d35d0b10dbfac14fb52ba001e527e13712e5e5b1dd699637919e92ea`  
		Last Modified: Mon, 22 Jul 2024 22:10:17 GMT  
		Size: 19.2 MB (19223781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97166d4d20454cc93121a4ef3ea03592678570b61caef1221cfaad42feedbe4f`  
		Last Modified: Mon, 22 Jul 2024 22:10:14 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af3ce2cb1823f6337a5faafd97d60f4630b5f391f78a8fc8d500f3f47ce2ae7`  
		Last Modified: Mon, 22 Jul 2024 22:10:14 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c76b9c4a4bd1656be0774bd3c4928eb7982bc6b4f357e52f559e7f5a8c1e5d`  
		Last Modified: Mon, 22 Jul 2024 22:10:14 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc16a8e5eaf376a934ac3933c861d5824e85929038eac714b27bb2fe55ed405f`  
		Last Modified: Mon, 22 Jul 2024 22:10:17 GMT  
		Size: 19.7 MB (19657911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
