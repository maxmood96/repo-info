## `docker:27-rc-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:808688eaf4e4ae2ed79c4484acaea2e381f06c6108bd379fef08f3e8e9b3f882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2655; amd64

### `docker:27-rc-windowsservercore-ltsc2022` - windows version 10.0.20348.2655; amd64

```console
$ docker pull docker@sha256:e77a0997e6d76a476307829e7813eba2f8e475df5077dffd78f19c4020668358
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2199778652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed01614bfb43d6b8b9c40d15f5f4167c37ee468b8533b0798b0274f1f6cd973`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Mon, 19 Aug 2024 19:07:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 19 Aug 2024 19:08:00 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 19 Aug 2024 19:08:00 GMT
ENV DOCKER_VERSION=27.2.0-rc.1
# Mon, 19 Aug 2024 19:08:01 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-27.2.0-rc.1.zip
# Mon, 19 Aug 2024 19:08:16 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 19 Aug 2024 19:08:17 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Mon, 19 Aug 2024 19:08:17 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Mon, 19 Aug 2024 19:08:18 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Mon, 19 Aug 2024 19:08:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 19 Aug 2024 19:08:29 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 19 Aug 2024 19:08:29 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Mon, 19 Aug 2024 19:08:30 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Mon, 19 Aug 2024 19:08:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd649075383e8df03ea713dfe59e1205716fbaa14450c10ef0d0a24a7b63669`  
		Last Modified: Tue, 13 Aug 2024 17:49:18 GMT  
		Size: 753.2 MB (753166182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3801404cdc892635f65f6e905d96fb9a776751ac28ea27360e9b94c173eca1b`  
		Last Modified: Mon, 19 Aug 2024 19:08:47 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61200cd4117468daf5bf2c005679efdcb39ee4fcbaac77ef42e276358de2f34d`  
		Last Modified: Mon, 19 Aug 2024 19:08:47 GMT  
		Size: 372.6 KB (372611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89b54a6ed12c584940cf95d2f86ad0139b96eb495b74625392ba7fcedd2cc148`  
		Last Modified: Mon, 19 Aug 2024 19:08:46 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3b0e15c1cb27c0fe7cf785e9f1fd0e782822a1161c823c149b23510784a75e`  
		Last Modified: Mon, 19 Aug 2024 19:08:46 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1fcd27785bb5f9923ace3cc2cf0a1790e0c7f3e20ec5896ddf3ffe11aad087`  
		Last Modified: Mon, 19 Aug 2024 19:08:47 GMT  
		Size: 18.7 MB (18661452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bce235f5a6b99d4e61d059490faa1c8cea4d2d8fcf058f463bbb86c0eb3abf3`  
		Last Modified: Mon, 19 Aug 2024 19:08:44 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83250b81587715d8de91e4548fe509e2458eb95b8c6f57a39f6d295243f775fc`  
		Last Modified: Mon, 19 Aug 2024 19:08:44 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7e9e42d740362770702aef68cc906ff8a8dd1207a0c63ac30f5f23ce464743`  
		Last Modified: Mon, 19 Aug 2024 19:08:44 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9d46da6cf663840c59219b46b9ab79c857f975a503383a766f050aed1cbe60`  
		Last Modified: Mon, 19 Aug 2024 19:08:45 GMT  
		Size: 19.3 MB (19264787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e457ac888e1209c9ff4b617ad71638008b76d5a0533f1c1d5f459a2fa4ace34f`  
		Last Modified: Mon, 19 Aug 2024 19:08:42 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eef9aacecac44fff4ad004d90f82394f0cae2fbce5aa7ce94b9a789f981c219`  
		Last Modified: Mon, 19 Aug 2024 19:08:42 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4ac4416f15ccbadd940f1da3f197ab501cb9e30e948e26429216e47d9dc55b`  
		Last Modified: Mon, 19 Aug 2024 19:08:42 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acfbe2a6539715d2bde2de86d6798c6febd829d29a02da95da9efa3bd3aad75e`  
		Last Modified: Mon, 19 Aug 2024 19:08:45 GMT  
		Size: 19.7 MB (19703228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
