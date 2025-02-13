## `docker:28-rc-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:7e7957c19d2ea1762fae953d5ac44e2bfed8582886daf576396967c23258e5ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `docker:28-rc-windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull docker@sha256:d8d1cda89556f2cc63184602e800980cc333f81ab9790534179e76c4bb8221cb
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2561876106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90884cfafcbab44a38222da25c11198d7e14c35f286c197b066bad904bc60cee`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Mon, 10 Feb 2025 19:31:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 10 Feb 2025 19:31:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 10 Feb 2025 19:31:43 GMT
ENV DOCKER_VERSION=28.0.0-rc.1
# Mon, 10 Feb 2025 19:31:43 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.0.0-rc.1.zip
# Mon, 10 Feb 2025 19:31:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 10 Feb 2025 19:31:53 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Mon, 10 Feb 2025 19:31:54 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.windows-amd64.exe
# Mon, 10 Feb 2025 19:31:55 GMT
ENV DOCKER_BUILDX_SHA256=39f53ec70c6ce37beca6898809e8eb89a77a1651be35ea50b51629c7a5d3b1f2
# Mon, 10 Feb 2025 19:32:03 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 10 Feb 2025 19:32:03 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 10 Feb 2025 19:32:04 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Mon, 10 Feb 2025 19:32:05 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Mon, 10 Feb 2025 19:32:13 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Wed, 22 Jan 2025 06:04:03 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e8bb6d67e66867cd26dd75571a9921560ae7549a83cb7ffaf49c9b5cf8de8c`  
		Last Modified: Mon, 10 Feb 2025 21:10:09 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e146419bf0cafabd7c95cca7223b7fd2709fff5a9922c8a6eedb4dda9ac553f`  
		Last Modified: Tue, 11 Feb 2025 00:33:01 GMT  
		Size: 384.5 KB (384533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00befedf094078094ad0364ed2bad0c1b198a4c30a7e14f4164f24e370965b46`  
		Last Modified: Mon, 10 Feb 2025 21:10:09 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8452cd101f395a2a1a97e508fa7b09ba624f9e5e149396acac0a93cd363f2342`  
		Last Modified: Mon, 10 Feb 2025 21:10:09 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b05d9d424f3d0c5658e6ef1c4310292395fd766b6a9baa37340632d38cfab5`  
		Last Modified: Mon, 10 Feb 2025 21:10:11 GMT  
		Size: 19.8 MB (19814358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4820b5ebef8471388ac91eb6031d458dc07676d70f181db8975e0564371ef929`  
		Last Modified: Tue, 11 Feb 2025 00:33:03 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3eafcbe41b227623f16607ad596c80e7a88a8fbb5285b14c4939e6b2a1bc141`  
		Last Modified: Mon, 10 Feb 2025 21:10:09 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab0399db27f2e68a02688db07e2fd58a8ef7d74fb806c6d369f24c541310b82`  
		Last Modified: Tue, 11 Feb 2025 00:33:03 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef904bc3954677d34b300350c39ea44bff65ab42be00a32b8465be45974a8b88`  
		Last Modified: Mon, 10 Feb 2025 21:10:10 GMT  
		Size: 21.2 MB (21179334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760d7f549a1ba08606bdadb13e9020d6fe8bd0d0b6a86ec459de63c4471d87ee`  
		Last Modified: Mon, 10 Feb 2025 21:10:09 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53133fd9219d43ca4ac2d464c67c795da883fd0d9af126788718ca96e67f6e59`  
		Last Modified: Mon, 10 Feb 2025 21:10:09 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:896fb6a29e0c8b0155e78f66f81983033dc44b3f831c05f27e33df46110b8024`  
		Last Modified: Mon, 10 Feb 2025 21:10:09 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e84e59864ba0ecea7a15bff7de6ee2e33783fb5c20d08073f0318d515eac73d`  
		Last Modified: Mon, 10 Feb 2025 21:10:10 GMT  
		Size: 20.2 MB (20208550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
