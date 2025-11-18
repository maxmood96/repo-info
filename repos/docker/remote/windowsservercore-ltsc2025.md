## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:bdc0c4b3cdaffcb62ab6a75247d0d42866b92c3531b102815def4676ea26debc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull docker@sha256:934abd3549928ea7b2a1e723689932978981e4437b623680d3f20d63274e9384
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3301957431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1adbb0187dfe84f467ea1c8bedaa808bbf5a2d50600a754857296d0341c2c547`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 18 Nov 2025 00:19:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Nov 2025 00:19:31 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 18 Nov 2025 00:19:33 GMT
ENV DOCKER_VERSION=29.0.2
# Tue, 18 Nov 2025 00:19:34 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.2.zip
# Tue, 18 Nov 2025 00:19:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 18 Nov 2025 00:19:46 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 18 Nov 2025 00:19:46 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Tue, 18 Nov 2025 00:19:47 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Tue, 18 Nov 2025 00:19:55 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 18 Nov 2025 00:19:56 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 18 Nov 2025 00:19:56 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Tue, 18 Nov 2025 00:19:57 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Tue, 18 Nov 2025 00:20:05 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e7cef4a3415e4a64bcfbd4e853e4a6f58af113e4c2fe90d11e7cbba12594bc6`  
		Last Modified: Tue, 18 Nov 2025 00:41:21 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed06b4a3f1f41e47163ce23777474f55955d7a9c58cfe32956ca99dbc76636e7`  
		Last Modified: Tue, 18 Nov 2025 00:41:21 GMT  
		Size: 398.3 KB (398261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67553f4fa23300c4020ac2b70f3ba2ec21a2e0c8998c982ffb0e76e13866eb69`  
		Last Modified: Tue, 18 Nov 2025 00:41:21 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f6eb7a315e170e1eb60174f22fc4ae1ae955a53a825c8c04da213ee81840cb`  
		Last Modified: Tue, 18 Nov 2025 00:41:21 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1c531039ae1417a09a1f0578508d166140ac2d43c08e3ef9f28b8f2cb5f80d`  
		Last Modified: Tue, 18 Nov 2025 00:41:23 GMT  
		Size: 19.4 MB (19445556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca808fe84649e3ef31e6fc229b4fce64b8557567040ea939c983da532e2c2b3b`  
		Last Modified: Tue, 18 Nov 2025 00:41:21 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4aeabf3e1056b854b253d77d3499f76afe2eca8aedbad5cc34a329a323046bc`  
		Last Modified: Tue, 18 Nov 2025 00:41:21 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e9724dd5054fb82b4ff6b1dcc33887839f1326abe09264b476daa801123b72f`  
		Last Modified: Tue, 18 Nov 2025 00:41:21 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3aa490c7e1923580055244a94ae68dbfa6632d128c666eb31b80646f5deb9a8`  
		Last Modified: Tue, 18 Nov 2025 00:41:24 GMT  
		Size: 23.9 MB (23947929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:797fcf7ef67d61b3b0bb3aa2856a1be3fc4e4634693ca6a3931395e4c500f903`  
		Last Modified: Tue, 18 Nov 2025 00:41:21 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2fd98eb31c8cb4c58e65bae6ec86f00da81c0dc898686fc7852f95c1a37545c`  
		Last Modified: Tue, 18 Nov 2025 00:41:21 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d55c8b9cc249c7351353019b8836cd0923acedc0ea5d01c0bf0248096b700d1`  
		Last Modified: Tue, 18 Nov 2025 00:41:21 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5e9c94859b6864f9aec716da8bbe93edd2d7e2ffa89f053548c74dd78df4e7`  
		Last Modified: Tue, 18 Nov 2025 00:41:23 GMT  
		Size: 22.7 MB (22698164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
