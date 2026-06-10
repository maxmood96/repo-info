## `docker:29-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:9df2b61e3220bc07763d0d46ea3ea7d312e1e012d5c746cf9686ca44cd8b59cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `docker:29-windowsservercore-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull docker@sha256:e1874ace86696dc406093e614d34ce6a6f07ed7187e25f029685911a711ccc40
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2188548521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d76e268d68e640ffd98a8af27bf187fba7876b6ac6253c294854ec499aed056`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Tue, 09 Jun 2026 22:09:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2026 22:09:40 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Jun 2026 22:09:41 GMT
ENV DOCKER_VERSION=29.5.3
# Tue, 09 Jun 2026 22:09:43 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.3.zip
# Tue, 09 Jun 2026 22:10:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:10:07 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Tue, 09 Jun 2026 22:10:08 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.windows-amd64.exe
# Tue, 09 Jun 2026 22:10:09 GMT
ENV DOCKER_BUILDX_SHA256=41e1b3fff6541d5f5febb18ff4c9108bec30afd7bf9133b82783735c2078eac1
# Tue, 09 Jun 2026 22:10:36 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:10:37 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Tue, 09 Jun 2026 22:10:38 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Tue, 09 Jun 2026 22:10:39 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Tue, 09 Jun 2026 22:10:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a21107eb392ad352a11d88add9657687384931e5d889cdcf2e9933b4421077`  
		Last Modified: Tue, 09 Jun 2026 22:10:57 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28b0d166672182721ce571506f9d6ffbdf3978263c1e98a8c7cb83d70e5ceb3`  
		Last Modified: Tue, 09 Jun 2026 22:10:56 GMT  
		Size: 487.8 KB (487761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b460336fce54b4157c40e9e971fab0f408aeda838dde55bcf5ea5de52f3fa3`  
		Last Modified: Tue, 09 Jun 2026 22:10:55 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea67caacc1b68dc837ec089a76c72de278a12c98986a9e7e27a6b4fa3f1f289`  
		Last Modified: Tue, 09 Jun 2026 22:10:55 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc9755d22906699b3ae49e1e7e643b80a71128ccb86715598896d101848d5074`  
		Last Modified: Tue, 09 Jun 2026 22:10:57 GMT  
		Size: 20.0 MB (19967046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa89af8ddf8470a85bb4691fdf78f932741c527c8b8f25d9cdb0ab957b72766`  
		Last Modified: Tue, 09 Jun 2026 22:10:53 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e31ea216b5955db20bf270de50921353f50fb244567aeffa9aec6a22bdf910`  
		Last Modified: Tue, 09 Jun 2026 22:10:53 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0473ee7061cd54cff9f36e7d95856e8a0ad754f1afd89c20cff85132b100c5f`  
		Last Modified: Tue, 09 Jun 2026 22:10:53 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd4d1bb31a8a58e6c19fa9476763d11417da6c9deccc5f3a25491e741f79611`  
		Last Modified: Tue, 09 Jun 2026 22:11:00 GMT  
		Size: 23.9 MB (23888859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299e4bdf749ee7ad62af795111680dbce48097a254a3d53ebee0f0feb07f3820`  
		Last Modified: Tue, 09 Jun 2026 22:10:52 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebdcd68b54960c0145901d3e97fbca29555cdd34359f1433932b88715f7ebd8a`  
		Last Modified: Tue, 09 Jun 2026 22:10:51 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcecc97fe08a6e5f535dbb042a7e39cee7fd26ff6b8f64f4b87657d71a9ca42`  
		Last Modified: Tue, 09 Jun 2026 22:10:51 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:057fa34c824943d81b41f22bf794e23e40378d1db98addd0261c1fc64a152f55`  
		Last Modified: Tue, 09 Jun 2026 22:10:54 GMT  
		Size: 12.1 MB (12067581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
