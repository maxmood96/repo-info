## `docker:28-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:06ab0dc167ff231631e9440452872f362a4becf65ff669f3b539aec0aeffaf4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3781; amd64

### `docker:28-windowsservercore-ltsc2025` - windows version 10.0.26100.3781; amd64

```console
$ docker pull docker@sha256:6829f90124da866f0530f60e7309ac3afe165ab5e8d3532a175fffcc8a927386
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3459661369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0fba3ec89fd58527201e3b21d8f77b8d37c036f7eb9ed1ab4f20b345f01344c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Tue, 15 Apr 2025 10:03:37 GMT
RUN Install update 10.0.26100.3781
# Fri, 18 Apr 2025 18:23:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 18:23:24 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 18 Apr 2025 18:23:24 GMT
ENV DOCKER_VERSION=28.1.1
# Fri, 18 Apr 2025 18:23:25 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.1.zip
# Fri, 18 Apr 2025 18:23:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 18:23:36 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Fri, 18 Apr 2025 18:23:37 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Fri, 18 Apr 2025 18:23:38 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Fri, 18 Apr 2025 18:23:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 18:23:48 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.1
# Fri, 18 Apr 2025 18:23:48 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-windows-x86_64.exe
# Fri, 18 Apr 2025 18:23:49 GMT
ENV DOCKER_COMPOSE_SHA256=971d6000e2c70da19c20f8264330a7ec3962b1fd59601afeb7e3636bad89b8c9
# Fri, 18 Apr 2025 18:23:58 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a55b9bd12cfb5d81d64963683e6d5d0ba9423233c85140eff135128a64f7ee`  
		Last Modified: Fri, 18 Apr 2025 03:15:41 GMT  
		Size: 1.2 GB (1179854238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c62eaedcaf35f1eaff9989553853025c2936d229c3d0f5cc50e602f5372f4df`  
		Last Modified: Fri, 18 Apr 2025 18:24:04 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6e72fcd5ebbf8530f47102730adac795759b8fb1408415987a5d1d4fde3c61`  
		Last Modified: Fri, 18 Apr 2025 18:24:04 GMT  
		Size: 369.3 KB (369311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e680bbdabbfb8e2db51183503be0b467f83cf6eb528a14c1da156d0464dc1c1`  
		Last Modified: Fri, 18 Apr 2025 18:24:03 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:728f2a276f94f8bab9ed143cd5048e6b74575224895de38f40b6d6451182cf0c`  
		Last Modified: Fri, 18 Apr 2025 18:24:03 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e654b8d6b0a1afe4c68f957dd17a865df8b0138cc0ddce63dc615cb4c6bb0e`  
		Last Modified: Fri, 18 Apr 2025 18:24:05 GMT  
		Size: 19.9 MB (19902316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5491c230eab033ae931edecc3591b67dd07e45262f88abcf4b3f2c96f0acab38`  
		Last Modified: Fri, 18 Apr 2025 18:24:02 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda3ea1e4d9dabb005cb86232a84c158d658e614eec654bedcb99d8cabb686ca`  
		Last Modified: Fri, 18 Apr 2025 18:24:02 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c76a6b6808f90af0b830e2805301599be481c06b6fcc7c1051ee137c4390dc9b`  
		Last Modified: Fri, 18 Apr 2025 18:24:02 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed0d823148196959e5eff3cb6eeaf9f3f6f4f5520e2456535d7121b7ff13ad1`  
		Last Modified: Fri, 18 Apr 2025 18:24:04 GMT  
		Size: 22.4 MB (22362152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa406d2ab9b559cfb725f9ba83fee9ddd6077963c4b08e110e60f5b2b0dd739`  
		Last Modified: Fri, 18 Apr 2025 18:24:01 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69470795af93868a47bae9e5eea39c5072b91f2874d4d4348694c13d115c0d2e`  
		Last Modified: Fri, 18 Apr 2025 18:24:01 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45dc9dd297409c858e53f06c1ae25afa5608ba977be88628a69fe654ecf5cea0`  
		Last Modified: Fri, 18 Apr 2025 18:24:01 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aa4dc2e1ecbd68e8b895b5494d4810bfa742b5f1d5cd6981f536c876e59d62c`  
		Last Modified: Fri, 18 Apr 2025 18:24:04 GMT  
		Size: 21.9 MB (21854369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
