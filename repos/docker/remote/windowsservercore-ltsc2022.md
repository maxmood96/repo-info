## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:a6d1d903e18bd7a6159ffff76b4e620446f5ba9b556a53635d8768660bfd33e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull docker@sha256:9335748761ce6d7d5f0a3eab408769b56669201b4547e40a21961ab86595c5ee
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1955861580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b837f63ca548e1fb6614c1e7d0f1738a8f93d07e518f821e3a41dfb13c84813`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Tue, 30 Jan 2024 22:51:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 30 Jan 2024 22:52:27 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 30 Jan 2024 22:52:28 GMT
ENV DOCKER_VERSION=25.0.1
# Tue, 30 Jan 2024 22:52:28 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-25.0.1.zip
# Tue, 30 Jan 2024 22:52:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 30 Jan 2024 22:52:44 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Tue, 30 Jan 2024 22:52:45 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.windows-amd64.exe
# Tue, 30 Jan 2024 22:52:45 GMT
ENV DOCKER_BUILDX_SHA256=0ff0853a09960ff8f454d5db7253d5d935f5538856ea4985a276cbd1b28a96a5
# Tue, 30 Jan 2024 22:52:55 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 30 Jan 2024 22:52:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.4
# Tue, 30 Jan 2024 22:52:56 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-windows-x86_64.exe
# Tue, 30 Jan 2024 22:52:57 GMT
ENV DOCKER_COMPOSE_SHA256=e68c6eb31cc0aff2d9eb0f11d48e709888f25c0c204ce74bfbe69e33af3bbcbb
# Tue, 30 Jan 2024 22:53:07 GMT
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
	-	`sha256:ece89c7ae3a6eefa1a0618c5f55cb752d106386f99b250e79c73dc06b9a01e11`  
		Last Modified: Tue, 30 Jan 2024 22:53:17 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bd8f90fb5fc9bee6769521e6c1ad6261c591ee1c71f873c91c412a798a30299`  
		Last Modified: Tue, 30 Jan 2024 22:53:17 GMT  
		Size: 494.1 KB (494118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a68bbf65c7a639b9744c0d1cd27a649b6283270647e80aedb14c4a4908bc230`  
		Last Modified: Tue, 30 Jan 2024 22:53:15 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9afa0cf72417b3747e53ed8ab0ff28d28f110eed4ef19dbfb6d851fcfb1fb76`  
		Last Modified: Tue, 30 Jan 2024 22:53:15 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9117726719d4fc477583f66a59631ee147353556637893aa188966e3b30f583a`  
		Last Modified: Tue, 30 Jan 2024 22:53:17 GMT  
		Size: 18.1 MB (18067389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b154002cd990e3605dfd599d8c7e5764fc111040bb658699ce70ab1dbaac033`  
		Last Modified: Tue, 30 Jan 2024 22:53:13 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b009991e73eb4aaec066727e54fec50bf9c8f6597ff4fc3fa3e8e5b9d0f06dad`  
		Last Modified: Tue, 30 Jan 2024 22:53:13 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8519161b23a12d61f106f7e220b0e938fbfe980847b803850b83e026a8f6fa4f`  
		Last Modified: Tue, 30 Jan 2024 22:53:13 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6866b81f70775d255134d98897247793815432abec003b4b763bf3d5648744`  
		Last Modified: Tue, 30 Jan 2024 22:53:14 GMT  
		Size: 18.0 MB (18019463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b19565598d375cf3fa5e7fd851ea165430038caa45a6d6ae6c06f0bd4a702775`  
		Last Modified: Tue, 30 Jan 2024 22:53:11 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a39d87f34875f99e38c5e814c1adea07477829dad0528c8c770d4fb3e38240ed`  
		Last Modified: Tue, 30 Jan 2024 22:53:11 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce6002c79d0a33f063938a8865d5c608a7a609468d12be95f0fd45be1bfe2ac`  
		Last Modified: Tue, 30 Jan 2024 22:53:11 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:028eb27c1505f0d71cce338fa8e52301732e3f95c816256688c15b8676ba0f9d`  
		Last Modified: Tue, 30 Jan 2024 22:53:14 GMT  
		Size: 19.1 MB (19056363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
