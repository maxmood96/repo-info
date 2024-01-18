## `docker:rc-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:100e2e5d0eef2350dc3240aa28fa10dffdc427c1759b0b0c11d27d6ccea1c5de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `docker:rc-windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull docker@sha256:aa555b4b30b5e62948f27bda73e721e48426d0e4276eac78953ac929cab9e19b
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1955832779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbe13d02b3d66b2e9747f7563562717e7ea88c6f978e5adf722165a17ccd3e7d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Thu, 18 Jan 2024 00:09:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 18 Jan 2024 00:10:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 18 Jan 2024 00:10:14 GMT
ENV DOCKER_VERSION=25.0.0-rc.3
# Thu, 18 Jan 2024 00:10:14 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-25.0.0-rc.3.zip
# Thu, 18 Jan 2024 00:10:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 18 Jan 2024 00:10:25 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Thu, 18 Jan 2024 00:10:25 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.windows-amd64.exe
# Thu, 18 Jan 2024 00:10:26 GMT
ENV DOCKER_BUILDX_SHA256=0ff0853a09960ff8f454d5db7253d5d935f5538856ea4985a276cbd1b28a96a5
# Thu, 18 Jan 2024 00:10:34 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 18 Jan 2024 00:10:35 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.0
# Thu, 18 Jan 2024 00:10:35 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-windows-x86_64.exe
# Thu, 18 Jan 2024 00:10:36 GMT
ENV DOCKER_COMPOSE_SHA256=4e0e387d67a65d92e3a7aca085f86b4b46ed5bd7a475f81921629e1d097178f0
# Thu, 18 Jan 2024 00:10:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00a9f0a3e45908a147aa3807e7c1cacf20d4741ad7c512d575c30964167a433`  
		Last Modified: Thu, 18 Jan 2024 00:10:52 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec725c8096d88c13a146606b7266b70b6f0b7b7cffe2888927dd69bafa5cbe6`  
		Last Modified: Thu, 18 Jan 2024 00:10:52 GMT  
		Size: 493.0 KB (492983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:422cfd8024a2eb8d07312b95e0296fda25cf989a827cff634044e71c28221948`  
		Last Modified: Thu, 18 Jan 2024 00:10:51 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321c109f915f833f6916f2f6ded6adf50e888ec6d67ccaa5c6fc261f705cfd2c`  
		Last Modified: Thu, 18 Jan 2024 00:10:51 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ead3d1fd8cf9b636217b58aac66685827acc0a8edb0eac3dd6a91cdffe5d9d8`  
		Last Modified: Thu, 18 Jan 2024 00:10:53 GMT  
		Size: 18.1 MB (18066785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6df01a2d07ee30bf98c58486f4b6b04d5d26194c6338602f97c96cb74f5f49b`  
		Last Modified: Thu, 18 Jan 2024 00:10:49 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d29aeeeaba56e4516f490a59e4d73a9cf18573f7ea714aff5c1bd972320367`  
		Last Modified: Thu, 18 Jan 2024 00:10:49 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9437af81255be25211da496016a52e44365dfa430d41ce9272a6a5446f02c07e`  
		Last Modified: Thu, 18 Jan 2024 00:10:49 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843d466e370d52e3beefc415b3d70ce8fbd810524ff122ceb5c71c941ea0eb0f`  
		Last Modified: Thu, 18 Jan 2024 00:10:50 GMT  
		Size: 18.0 MB (18019156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6977d0531b000a9444838c019d36ee67fd31a587fa6abe852f16e569c78e1cee`  
		Last Modified: Thu, 18 Jan 2024 00:10:47 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18364a35cd9ecaafc7dc66394fd4c9dd59992eea7d16caa6df5e4c1d1a86de3`  
		Last Modified: Thu, 18 Jan 2024 00:10:47 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7423f0c2b16cdc81fe7cb47fdf8c0e2c5b9e6268e53e7c6e5ede8a759a7d347d`  
		Last Modified: Thu, 18 Jan 2024 00:10:47 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0360201f9ed387e4305bf188f2c6671187dcc1e73b5ba9a34145505533ae9561`  
		Last Modified: Thu, 18 Jan 2024 00:10:50 GMT  
		Size: 19.0 MB (19029553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
