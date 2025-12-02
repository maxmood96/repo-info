## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:5e399dd5dd0dfe81579a2bca9462ce91fd0af47c6c1f7a6b73ffbc942907f790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull docker@sha256:edb55a55a9709f716094eff0d619f5cccfbe7ab9c820d4cd94316a3dc80f85b0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3301942510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd431f71a41f9ca0d66fa3490028ce3378094dc608e876e5a5e01d5f1c00a85`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 02 Dec 2025 00:02:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Dec 2025 00:03:17 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 02 Dec 2025 00:03:18 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:03:19 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.1.zip
# Tue, 02 Dec 2025 00:03:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 02 Dec 2025 00:03:37 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:03:37 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Tue, 02 Dec 2025 00:03:38 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Tue, 02 Dec 2025 00:03:49 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 02 Dec 2025 00:03:49 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:03:50 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Tue, 02 Dec 2025 00:03:50 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Tue, 02 Dec 2025 00:03:59 GMT
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
	-	`sha256:1274f6d3b6ceaa195acd16a17546b93878ef3c76e6b0c0ea475532ae81138829`  
		Last Modified: Tue, 02 Dec 2025 00:29:21 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea18719cadfdf416a79dc2e3958aaaa04ba5f00625ff6e93ab3dec72cf2f51da`  
		Last Modified: Tue, 02 Dec 2025 00:29:25 GMT  
		Size: 394.4 KB (394389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bacb90f7314fdc946208b5f3ff65f6c72d6649551c978d26418bda8d9e5a6890`  
		Last Modified: Tue, 02 Dec 2025 00:29:30 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad66afc50aa529e50d970dea5d3e8f437aab69ad9cb3882a256d4319b5b42d15`  
		Last Modified: Tue, 02 Dec 2025 00:29:33 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7b85b05963e8f44359d0370018251cb0af969ffdbeeb8b5a7d16e32fa4e6e0`  
		Last Modified: Tue, 02 Dec 2025 01:01:49 GMT  
		Size: 19.4 MB (19445634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4369b8ed94ba65d95a6942b0a54d8302024faae5688bd932577bcc256abefee3`  
		Last Modified: Tue, 02 Dec 2025 00:29:37 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a49cd2f3d1017e97f6ed405d89cd3d09949977cd4e8b5b34fdb146b8da04a3`  
		Last Modified: Tue, 02 Dec 2025 00:29:41 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f583f8eec952d8c1f2b32d817e3b14c51c57780bc726d9eb1c393555075ba3c7`  
		Last Modified: Tue, 02 Dec 2025 00:29:45 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9def44a99f4bab2dcc70f25abcf502cbafd84b76181171949b51aa186814cce8`  
		Last Modified: Tue, 02 Dec 2025 01:01:52 GMT  
		Size: 23.9 MB (23942612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a46335ebb4377421068829028c4feca1ce21bb336ddc77ffaff4cf2fdd07669d`  
		Last Modified: Tue, 02 Dec 2025 00:29:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6700c7401706484942b62f39837e732625ea2eae796316fd97da557c97d9a2bd`  
		Last Modified: Tue, 02 Dec 2025 00:29:51 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54fcde18a4abb110b9720f6357dc8098af919dc2247e1fcb902d2dbce1dc2bbb`  
		Last Modified: Tue, 02 Dec 2025 00:29:54 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a17a06df7c12fbd246e254cc1c5ccda1ea8a3064c55627e865f6c813204a155a`  
		Last Modified: Tue, 02 Dec 2025 01:01:55 GMT  
		Size: 22.7 MB (22692302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
