## `docker:26-rc-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:37e198be1af601425777375503cd899a7b8a7e70410dc30d3b13b41d4507e88a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2322; amd64

### `docker:26-rc-windowsservercore-ltsc2022` - windows version 10.0.20348.2322; amd64

```console
$ docker pull docker@sha256:431271c0ff49e91f10ece061322688fa11746f2a68fdea747fb8223afc6ac43f
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1967086328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b018e28a42d113cbae2e12ef8ac9ccbf9c7efe328b790e8ce782bce70b3d9f39`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Fri, 08 Mar 2024 16:55:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 08 Mar 2024 16:56:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 08 Mar 2024 16:56:14 GMT
ENV DOCKER_VERSION=26.0.0-rc2
# Fri, 08 Mar 2024 16:56:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-26.0.0-rc2.zip
# Fri, 08 Mar 2024 16:56:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 08 Mar 2024 16:56:38 GMT
ENV DOCKER_BUILDX_VERSION=0.13.0
# Fri, 08 Mar 2024 16:56:38 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.windows-amd64.exe
# Fri, 08 Mar 2024 16:56:39 GMT
ENV DOCKER_BUILDX_SHA256=001dd8c707862d7c7a7bc17ebb024922ee304bddad1bca11da5b3b3ff18effa6
# Fri, 08 Mar 2024 16:56:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 08 Mar 2024 16:56:48 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.7
# Fri, 08 Mar 2024 16:56:49 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-windows-x86_64.exe
# Fri, 08 Mar 2024 16:56:50 GMT
ENV DOCKER_COMPOSE_SHA256=1a5ffa12cff51a65f4e5e8874ed46b0783cfbc8f5ef837f5b9523decf1afd1d0
# Fri, 08 Mar 2024 16:57:00 GMT
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
	-	`sha256:ddfde95ede1dc6de6cb745233fd6ed9e51e4830c9a14690549c478175a65adf6`  
		Last Modified: Fri, 08 Mar 2024 16:57:06 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b2c02f98f651f76c15d4a2b9de0813a29b37494ecfe519bb2ae004b86a8946`  
		Last Modified: Fri, 08 Mar 2024 16:57:06 GMT  
		Size: 499.3 KB (499303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de770192b1d717c935674c1b69256d326dfa0843bfa4801a0b02294e11d3dd78`  
		Last Modified: Fri, 08 Mar 2024 16:57:05 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:404b5629c38c09aeac220d63e0f55c4be615d33ecd8164b4f0db274234fbdbe6`  
		Last Modified: Fri, 08 Mar 2024 16:57:05 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca06a6a73888e687bfda752549efc5c710836d89c8faa27235c6c10d9e533a0`  
		Last Modified: Fri, 08 Mar 2024 16:57:06 GMT  
		Size: 18.1 MB (18070267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add51a0951516609c63f1486fef178dea58668324fd3ea119e182a7c015e900d`  
		Last Modified: Fri, 08 Mar 2024 16:57:04 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37fc35828ae60ce028576cf1e34c4487f38b9f9273db9c1cbb6622f5b60814c`  
		Last Modified: Fri, 08 Mar 2024 16:57:04 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d20cee403a1d4f6b79b988148cbafb35792323d3d9103b5fe2d4dde18f09c38`  
		Last Modified: Fri, 08 Mar 2024 16:57:04 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de7c236431188f1fc17390fab0ef7b5a883fc8431e66942ecf2eeb3ec0cfd15`  
		Last Modified: Fri, 08 Mar 2024 16:57:06 GMT  
		Size: 18.8 MB (18801736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac135bf965549a628a84afac15af1eb2a1aeab5b0e686ff37ff33d056281e860`  
		Last Modified: Fri, 08 Mar 2024 16:57:03 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05656ef0b98b449df2499353b2c7ffe9230a0a1d111b320d730be5a171e8fff6`  
		Last Modified: Fri, 08 Mar 2024 16:57:03 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820fc89209582c1dc11d47e25108a371b3c4f22881bffc93d257ec95dba92a8e`  
		Last Modified: Fri, 08 Mar 2024 16:57:03 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e6b30431a455acbdcde70fc41056748a9ad3dbb6a221be7855bd68900f767e`  
		Last Modified: Fri, 08 Mar 2024 16:57:05 GMT  
		Size: 19.0 MB (19049235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
