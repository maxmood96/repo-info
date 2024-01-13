## `docker:rc-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:e972c52020d6a2c0cdbde69e0130aa1bbf34b3a96290c88ea6e55297ee804cb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `docker:rc-windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull docker@sha256:78b1d22edba6f9351e670fcdb334802833a6778af0311bab6e7fdbd3d458b324
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1955867274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19390a0dc63f773a799c941f3dea4618e27d1c06d69adcedd3424314b84578f0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Sat, 13 Jan 2024 02:04:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 13 Jan 2024 02:04:18 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 13 Jan 2024 02:04:19 GMT
ENV DOCKER_VERSION=25.0.0-rc.2
# Sat, 13 Jan 2024 02:04:20 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-25.0.0-rc.2.zip
# Sat, 13 Jan 2024 02:04:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 13 Jan 2024 02:04:29 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Sat, 13 Jan 2024 02:04:30 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.windows-amd64.exe
# Sat, 13 Jan 2024 02:04:30 GMT
ENV DOCKER_BUILDX_SHA256=0ff0853a09960ff8f454d5db7253d5d935f5538856ea4985a276cbd1b28a96a5
# Sat, 13 Jan 2024 02:04:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 13 Jan 2024 02:04:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.0
# Sat, 13 Jan 2024 02:04:39 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-windows-x86_64.exe
# Sat, 13 Jan 2024 02:04:39 GMT
ENV DOCKER_COMPOSE_SHA256=4e0e387d67a65d92e3a7aca085f86b4b46ed5bd7a475f81921629e1d097178f0
# Sat, 13 Jan 2024 02:04:47 GMT
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
	-	`sha256:30b4be0c06b59bd26e09b7eb419ab1261c39dd86ddd620b3f927c1903e3688a0`  
		Last Modified: Sat, 13 Jan 2024 02:04:53 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061da9688c735d9a3d849d72935dd5f8267f922f1cdd7279d5860d8c5e8a11fd`  
		Last Modified: Sat, 13 Jan 2024 02:04:53 GMT  
		Size: 502.7 KB (502717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef9c302589d392764326192ae7f99ddd05e93a3e04c0946d2ef3e6651041d66`  
		Last Modified: Sat, 13 Jan 2024 02:04:52 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f8d9695994de0cca48cadedc9708c1b733774e0f242de34dc969971349a7d5`  
		Last Modified: Sat, 13 Jan 2024 02:04:52 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5c3efff107aa4e3f75362f8e5b0bdfdde2a253244f7c6c836c157df2c00b0b`  
		Last Modified: Sat, 13 Jan 2024 02:04:53 GMT  
		Size: 18.1 MB (18071592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f22cc1be54f7088015a62668f73120530733659d4e84c3adc4ffb30323465c`  
		Last Modified: Sat, 13 Jan 2024 02:04:51 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22710ba188afbbb360270787636546bec53a82c3ea6610894892fa5ce69d04b1`  
		Last Modified: Sat, 13 Jan 2024 02:04:50 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b43017f23f80c0b9d5cef12451f69b90c0da6cc451d1929882b73def6ee765e`  
		Last Modified: Sat, 13 Jan 2024 02:04:50 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623585982450f7b47d8b86e084c19b6e6c99451d1265782236d2a7ce110ca2b0`  
		Last Modified: Sat, 13 Jan 2024 02:04:52 GMT  
		Size: 18.0 MB (18029420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8929d8afe52391dfa6e42af22282e35dbecfef4a2daa88ae9c7b415c4f115f`  
		Last Modified: Sat, 13 Jan 2024 02:04:49 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7bf8fcbf4aa493e1b32194f5618e9ab23b0336d6b5701fc9816bc9c9716504`  
		Last Modified: Sat, 13 Jan 2024 02:04:49 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9cf2b51fee151d5c612746b7a69bef3c4962c84a2e55d371546ccf3705962e`  
		Last Modified: Sat, 13 Jan 2024 02:04:49 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb8da2d60eb597a917c67de8869eddd348b6c49c660f8f4677a8b57c71b9a493`  
		Last Modified: Sat, 13 Jan 2024 02:04:52 GMT  
		Size: 19.0 MB (19039235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
