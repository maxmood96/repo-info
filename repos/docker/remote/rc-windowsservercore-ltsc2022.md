## `docker:rc-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:3e5c46e08fcc80b8bc820346ee373b2c57fb1a0e61cc0ff41dd8eb1da47d41b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `docker:rc-windowsservercore-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull docker@sha256:fa974a1f672b380caf9e5df5dd19f3fa2687f520c7af4c451bac3d848d3c442a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1643669972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e26e5806ceb487871bb39bfe7bba630405f3998313ec37d48a284f42dd37c00`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 31 Oct 2025 23:56:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Oct 2025 23:57:46 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 31 Oct 2025 23:57:47 GMT
ENV DOCKER_VERSION=29.0.0-rc.2
# Fri, 31 Oct 2025 23:57:48 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-29.0.0-rc.2.zip
# Fri, 31 Oct 2025 23:58:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 31 Oct 2025 23:58:08 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Fri, 31 Oct 2025 23:58:09 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Fri, 31 Oct 2025 23:58:09 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Fri, 31 Oct 2025 23:58:30 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 31 Oct 2025 23:58:31 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 31 Oct 2025 23:58:32 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Fri, 31 Oct 2025 23:58:32 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Fri, 31 Oct 2025 23:58:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d511a81139dc467e97154c610f34166211c2eddc675f4be98e565e8ba952429f`  
		Last Modified: Sat, 01 Nov 2025 00:09:54 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf022d0e6ab65b99eb8a85cb6c4d8db6282cd400cfe8da6e0302096bb9ac1d6f`  
		Last Modified: Sat, 01 Nov 2025 00:09:55 GMT  
		Size: 509.7 KB (509726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed216d7fa3d0b0e3c20d530f9fb41755c5b5e96775742db7c868bd4374a282c`  
		Last Modified: Sat, 01 Nov 2025 00:09:54 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449504a1cdb8a2408210770c0100ce6e42c8b4c4b77664d3731e756e1dcc49fc`  
		Last Modified: Sat, 01 Nov 2025 00:09:54 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d81eb943ee59a47bc3ba7e24addd7592941febd8e554a6a991163c43375918e`  
		Last Modified: Sat, 01 Nov 2025 00:09:57 GMT  
		Size: 20.1 MB (20122358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c72090d76905afe62cc48045f0544613c3c5c418c5656d5569cf116348a140`  
		Last Modified: Sat, 01 Nov 2025 00:09:54 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1723117c7506f38b1c158789a459e2fc6aa85b6da0bdb60b4d39c47d43348089`  
		Last Modified: Sat, 01 Nov 2025 00:09:55 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeabb688581d7b0d93930553574789d831bfb9f92b0bee10f67891de0090b72f`  
		Last Modified: Sat, 01 Nov 2025 00:09:54 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053741eb883221805d3cba3ac6dca5e8f358a41331a5f02224ff912f79323294`  
		Last Modified: Sat, 01 Nov 2025 00:09:56 GMT  
		Size: 23.2 MB (23159716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a027b1334ffc16be22bee2db47a72be2b3232b93645338ed88deafb98318a6d7`  
		Last Modified: Sat, 01 Nov 2025 00:09:55 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d2417e1de7baddae7dca09407454aca40aa5491941fe195fbfd24c35d428f0`  
		Last Modified: Sat, 01 Nov 2025 00:09:54 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b5d865386f23d7a02297c0525566c4bf0042839c1c4d8862499d8a0eebad72`  
		Last Modified: Sat, 01 Nov 2025 00:09:54 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a4f340984d456b335cdb23c49bc0cf907f457351c15a2d65c119906c9fc04e`  
		Last Modified: Sat, 01 Nov 2025 00:09:56 GMT  
		Size: 22.7 MB (22673422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
