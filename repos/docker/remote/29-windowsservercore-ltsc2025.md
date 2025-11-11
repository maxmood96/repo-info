## `docker:29-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:529e79f77f256c18d3449ee2b3afe778b7ac252226391cfcf83a54e16b1f83c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `docker:29-windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull docker@sha256:f837bce39539584466c46e594b9f0c81b35795836721c08982a0f91d997200ea
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3301029232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fde49f87e1cd7da85aad033b1d1565aebb9dbefd76b70cd81c19b094a439b94`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:11:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:44 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 11 Nov 2025 19:11:46 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 19:11:46 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.0.zip
# Tue, 11 Nov 2025 19:11:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 19:11:56 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 19:11:57 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Tue, 11 Nov 2025 19:11:57 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Tue, 11 Nov 2025 19:12:05 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 19:12:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 19:12:06 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Tue, 11 Nov 2025 19:12:06 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Tue, 11 Nov 2025 19:12:15 GMT
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
	-	`sha256:a77d76091b7aac8a391dc15a412eec8b3ee40fe1bc86700413bb69bf1114e676`  
		Last Modified: Tue, 11 Nov 2025 19:22:17 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57705bc4aa1e453e214669340c20ec44256db4da801f3106104ec20b93a80c6f`  
		Last Modified: Tue, 11 Nov 2025 19:22:17 GMT  
		Size: 339.3 KB (339255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e61534cc65875c590fe7e13a58c5f1c9f383d3df204ef1521b2c0e5978b459`  
		Last Modified: Tue, 11 Nov 2025 19:22:17 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:569dbb4820f686d3922f9c91d52b813af356bd690ae149348371d6e4caca4a5f`  
		Last Modified: Tue, 11 Nov 2025 19:22:17 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096d3c32f2105107d2ec689004dccd74709d115af77d5eafda417975a32ec423`  
		Last Modified: Tue, 11 Nov 2025 19:22:19 GMT  
		Size: 19.4 MB (19407554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f5caf299e5f728ab68863aa2a83d98bab228edde6131d35105563a6d6e5402`  
		Last Modified: Tue, 11 Nov 2025 19:22:17 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ac53906e4375308fd4355425554c6e38107ad3d406848d4de359fba65c86b2`  
		Last Modified: Tue, 11 Nov 2025 19:22:18 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a69edd0f0500bed085e20dec378ea3173a1ea772a5f0f13b29c2ce48881e7b0`  
		Last Modified: Tue, 11 Nov 2025 19:22:19 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58cbe51dd737e36d3aede4692a695eccfecb33dd785265e7db9b103940127341`  
		Last Modified: Tue, 11 Nov 2025 19:22:21 GMT  
		Size: 23.2 MB (23150833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a45652de8491119468d0f7b6191c70a97ab841b0f1aaf118d7979de6132670e`  
		Last Modified: Tue, 11 Nov 2025 19:22:18 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6e7c49ef5aecb14f6ff4eb109d9465851171bc3328322ab7e18302b62e1a593`  
		Last Modified: Tue, 11 Nov 2025 19:22:14 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daee60478741bde59ff4678f7189b7e2b89236f4df16b5c63ead8be0b3db8023`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e7271db460caf1303e74ff32ba6f1d3f45b3626177d4c5b119ccbfa96cf584`  
		Last Modified: Tue, 11 Nov 2025 19:22:17 GMT  
		Size: 22.7 MB (22663991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
