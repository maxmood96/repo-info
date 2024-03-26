## `docker:24-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:e22d4eda8412be8836ec6ac8c4dedc1777ac7371960236209b71f419a30b4a7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `docker:24-windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull docker@sha256:c22852bc3ad353866ee030560efa47cdc8e4a0652fd49d62efb01959f2988a60
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2013865366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3fe8386603d2115c959bdf7114d2dfbbc87d38ddd359f659b3fd557f0c4e90`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Mon, 25 Mar 2024 19:12:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Mar 2024 19:12:41 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 25 Mar 2024 19:12:41 GMT
ENV DOCKER_VERSION=24.0.9
# Mon, 25 Mar 2024 19:12:42 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.9.zip
# Mon, 25 Mar 2024 19:12:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 25 Mar 2024 19:12:55 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Mon, 25 Mar 2024 19:12:55 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.windows-amd64.exe
# Mon, 25 Mar 2024 19:12:56 GMT
ENV DOCKER_BUILDX_SHA256=6b113e84cbc3cd645646aa82f00a7f7d3737cc10375b4341e0aca0de0c997c75
# Mon, 25 Mar 2024 19:13:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 25 Mar 2024 19:13:08 GMT
ENV DOCKER_COMPOSE_VERSION=2.26.0
# Mon, 25 Mar 2024 19:13:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-windows-x86_64.exe
# Mon, 25 Mar 2024 19:13:09 GMT
ENV DOCKER_COMPOSE_SHA256=0a9a63442f50b494e8c5b6b1af9da138d9dbbeab094e3076747a709a470bb9e9
# Mon, 25 Mar 2024 19:13:19 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:642dd40899ef03447ebdd7600fd873e9a2e62771376e2c042f1949b6d02bce5e`  
		Last Modified: Mon, 25 Mar 2024 19:13:28 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7de4d9db792b62c2c84804893ed5630a3a7763eb1844d95c3b3b6cad1625388`  
		Last Modified: Mon, 25 Mar 2024 19:13:29 GMT  
		Size: 499.5 KB (499515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b32bef399c684ff7aeeb12696797f51f8154c473a06f4e3a888c03c816310a9e`  
		Last Modified: Mon, 25 Mar 2024 19:13:28 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18bfd96c786bcd3bb2a2dabd30654fc2eb52b2857228fd95a9529e6d98070bbd`  
		Last Modified: Mon, 25 Mar 2024 19:13:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95d1444e9d01d27cc9d3c0507c2e49195b6e6fe903f4c2db20cbc7c42da08f8`  
		Last Modified: Mon, 25 Mar 2024 19:13:29 GMT  
		Size: 17.5 MB (17532328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d3564dcfdac482734b18f8ea02608568246462b273f4fad8a8a90d3d5a60265`  
		Last Modified: Mon, 25 Mar 2024 19:13:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ea763a7057b2161a62dc3e0de1967bace5f0053c0ceba62340dc761140d95a`  
		Last Modified: Mon, 25 Mar 2024 19:13:26 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21915704eca3534abf3d3ffcf0e1495726e0a94ef8647d36ea8d7ae8e66d864e`  
		Last Modified: Mon, 25 Mar 2024 19:13:25 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdb70cebc47969f07d676040fedf6e71c94732a46d0cb482d7a1d1686c6e3f7`  
		Last Modified: Mon, 25 Mar 2024 19:13:26 GMT  
		Size: 18.8 MB (18829243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d2b6e04662f71c9e9322ff737ed4da98fa3f352ce1884ec9d2366d48036295`  
		Last Modified: Mon, 25 Mar 2024 19:13:23 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1400f8bad44a7574ec31f5f8703f271b5e49ac8517497b053623f7af00dfa603`  
		Last Modified: Mon, 25 Mar 2024 19:13:23 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:003656648668a7ccaeab4f6e4309b1489f8a9bba5b013c613782d03b50b29f5e`  
		Last Modified: Mon, 25 Mar 2024 19:13:23 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e50a7c2b4ed775ceab9bfc45e0ef797119188e568225bf125a9a01c2e3486d`  
		Last Modified: Mon, 25 Mar 2024 19:13:26 GMT  
		Size: 19.5 MB (19533656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
