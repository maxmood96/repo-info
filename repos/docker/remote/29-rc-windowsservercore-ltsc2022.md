## `docker:29-rc-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:f4ac9709310a1a11cfd630f530eb4e80f8b3b528357f100b0a3df1b00dfcd3e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `docker:29-rc-windowsservercore-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull docker@sha256:78cb309c19669d6f5e38c05edc365fb94d05805f9361c3f1f0257a1cef514ae5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1643449970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:364cdedab7f2210856358997ab83ed9191b85064114b3e800dd8de082209fffb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:10:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:11:15 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 24 Oct 2025 18:11:16 GMT
ENV DOCKER_VERSION=29.0.0-rc.1
# Fri, 24 Oct 2025 18:11:17 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-29.0.0-rc.1.zip
# Fri, 24 Oct 2025 18:11:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 24 Oct 2025 18:11:35 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Fri, 24 Oct 2025 18:11:36 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Fri, 24 Oct 2025 18:11:37 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Fri, 24 Oct 2025 18:11:49 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 24 Oct 2025 18:11:49 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Fri, 24 Oct 2025 18:11:50 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-windows-x86_64.exe
# Fri, 24 Oct 2025 18:11:51 GMT
ENV DOCKER_COMPOSE_SHA256=835b6a7150d12e128fa9fd902abff6212ff3e55398683d57e213956558ead5df
# Fri, 24 Oct 2025 18:12:13 GMT
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
	-	`sha256:116a61045287ead6d3e96e549433b65e0cd74ce2180f5ec4df258d66b09b85a4`  
		Last Modified: Fri, 24 Oct 2025 18:20:52 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:005edd3b53379366a6670815f1b8928b2515942ffbdfc323f3045bd40ef8253e`  
		Last Modified: Fri, 24 Oct 2025 18:20:53 GMT  
		Size: 497.0 KB (496983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19247ff6b0fe81d2d0c19200f1494a767d2df8d95375b076f98f93018b9919d5`  
		Last Modified: Fri, 24 Oct 2025 18:20:52 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e138ccf8606b516db59f39851d5d083361399bec5f9546128f49a6d290fc37`  
		Last Modified: Fri, 24 Oct 2025 18:20:53 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba9b2b83ff3679a3c7924b1e81c81676fd7204f71867607e06ec872c1a55f79`  
		Last Modified: Fri, 24 Oct 2025 18:20:54 GMT  
		Size: 20.1 MB (20052330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99c04a081102152ea2be916a50deb609b20d25d9db7cb54874ca55e529c6c095`  
		Last Modified: Fri, 24 Oct 2025 18:20:53 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e120f57a8309ee9a7d0bdd2be1fe26f2493184b363718ac655b305b08026c053`  
		Last Modified: Fri, 24 Oct 2025 18:20:53 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd1a7bd099cbfe86fe4808ec12a569e79ddba74fe9947fb29dd311eeb41eb0d5`  
		Last Modified: Fri, 24 Oct 2025 18:20:53 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e91d7f77a7c3231e8e7e676b336e03f2965f5a71a598be49eb1822ab0644d94`  
		Last Modified: Fri, 24 Oct 2025 18:21:09 GMT  
		Size: 23.1 MB (23149760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:940ca6ecbd9bc65b5b9f63884ce8d8598559d97cbe24d8dded0002d947ebc892`  
		Last Modified: Fri, 24 Oct 2025 18:20:54 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbfc56c1ef9d9726920dbc1a12522fa2e2b55669ca9653f41e431119ac74a1fd`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9744d7d8408906848f1e0b5b555efbda6962652f1f3fe9d051153585605b5b`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19a1daab0d61f92d2ffea37e4025f570e2bbbda9fd3e2204d5aecf0539f2485`  
		Last Modified: Fri, 24 Oct 2025 18:20:55 GMT  
		Size: 22.5 MB (22546194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
