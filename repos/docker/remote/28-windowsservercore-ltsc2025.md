## `docker:28-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:b25d93a59fbdb43e27ccd5ff42b9a530d1c07616c048664e2a9858300a0817ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `docker:28-windowsservercore-ltsc2025` - windows version 10.0.26100.3476; amd64

```console
$ docker pull docker@sha256:37fbf58c618a1e257ff62a5c17597a58c612390d9b8248b12de620ff0dc27116
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2974098228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d876f863caff9ced5d2166306316ea67c3e8f29ecd77f820b472be5e597514de`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Tue, 25 Mar 2025 21:35:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 25 Mar 2025 21:36:01 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 25 Mar 2025 21:36:02 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 21:36:03 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Tue, 25 Mar 2025 21:36:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:36:14 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 21:36:15 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Tue, 25 Mar 2025 21:36:16 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Tue, 25 Mar 2025 21:36:25 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:36:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 21:36:26 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 25 Mar 2025 21:36:26 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 25 Mar 2025 21:36:36 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230d8f91a46ec72be09fa76d5ed5c5c953b39e08a445f5dc09dacc9ee44eb74a`  
		Last Modified: Tue, 25 Mar 2025 21:36:46 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4497744dd92652df503964233d52071afe6b6da69fcc9d699ecdef8a81132716`  
		Last Modified: Tue, 25 Mar 2025 21:36:46 GMT  
		Size: 393.8 KB (393794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1bbe029cc51bac0aa9cdd3ec3325e113f38f3632cef853c3d488b1b1641adae`  
		Last Modified: Tue, 25 Mar 2025 21:36:44 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e6465d36bb7dd3cbd69b2e9a38b3544b7eab714dd64a6c38788e616627500b`  
		Last Modified: Tue, 25 Mar 2025 21:36:44 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9179050a0c68ba8475bf29ed21dd34e7d54d5f314a7ac42b2fca85710f90f32`  
		Last Modified: Tue, 25 Mar 2025 21:36:46 GMT  
		Size: 19.9 MB (19904481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3871cbf913d4865bf43a87c7cbf2227b2705afa74b1281dba34fe25af1a73e5b`  
		Last Modified: Tue, 25 Mar 2025 21:36:42 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae86510368ad79d177019fd99371ebda2255844ae98eed60c771294d11b158db`  
		Last Modified: Tue, 25 Mar 2025 21:36:42 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1c6e4bc9abf47f577d2fea496c8dd7cd245ef59f6342b8274eb1e1bfe3deb3`  
		Last Modified: Tue, 25 Mar 2025 21:36:41 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944b89a3759e186bd3d1e0373910a72d0c398b453c235e4e3859f193aafb6f7d`  
		Last Modified: Tue, 25 Mar 2025 21:36:43 GMT  
		Size: 22.8 MB (22807812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16d3fe3114e244b2f87a8272a1e53a7be89778c0f0609da78972fa83adf80028`  
		Last Modified: Tue, 25 Mar 2025 21:36:40 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3bb7f5e52b615856b2468cacce7cfda132ef42d917ec6c7b1ed45144fd6574`  
		Last Modified: Tue, 25 Mar 2025 21:36:40 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:711261a97010fbb377d12b5a0adc589d06fbb8b0d5fe5b15131e5124210a14d5`  
		Last Modified: Tue, 25 Mar 2025 21:36:40 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0375e49eb81a62ee6208594c9fd6c9c2faede214b7a1c4d4a263bd1908edb436`  
		Last Modified: Tue, 25 Mar 2025 21:36:43 GMT  
		Size: 22.3 MB (22332711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
