## `docker:29-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:1f2d595a801c9e3dbe46c5d73cbe2c3641b91850c5d68b3b5d12bc2d16c00c0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `docker:29-windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:15a90036338c041a1e8300b00ef309858efbc486311e2e56acb8db48fc685093
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1550960494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f00807941763b5ba7c0d2bfacb1fa28c30e4232760ca2afcac3a4e0ef6f8066`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 13 Jan 2026 22:53:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Jan 2026 22:53:22 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 13 Jan 2026 22:53:23 GMT
ENV DOCKER_VERSION=29.1.4
# Tue, 13 Jan 2026 22:53:23 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.4.zip
# Tue, 13 Jan 2026 22:53:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 13 Jan 2026 22:53:35 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 13 Jan 2026 22:53:35 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Tue, 13 Jan 2026 22:53:35 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Tue, 13 Jan 2026 22:53:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 13 Jan 2026 22:53:44 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.1
# Tue, 13 Jan 2026 22:53:44 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-windows-x86_64.exe
# Tue, 13 Jan 2026 22:53:45 GMT
ENV DOCKER_COMPOSE_SHA256=2ae341f9152b4d90f561f84b8f2e263d5b60e1613c6841c804447819290c4119
# Tue, 13 Jan 2026 22:53:52 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:56:33 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed7aff12eed6d468fbfd98c5cdb643204448d37e6b4376b4863d715fe54870b`  
		Last Modified: Tue, 13 Jan 2026 22:57:56 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5258ae08575d51736dc838f18bc15c8a0e2cba443f2bc98b40d43f5df0661ac1`  
		Last Modified: Tue, 13 Jan 2026 22:57:56 GMT  
		Size: 369.1 KB (369103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:812df6dab5168720010e31894c187e3bde98a3e354436035338abd541b553479`  
		Last Modified: Tue, 13 Jan 2026 22:57:56 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d4644053807cef50793b0be91f1fe5086889375f5c1c1b0fabcfea1294069cf`  
		Last Modified: Tue, 13 Jan 2026 22:57:56 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e835287214cc0e69670880d6587eed5f51a058eef308eb3d9e067a9f490b6e7d`  
		Last Modified: Tue, 13 Jan 2026 22:57:58 GMT  
		Size: 19.4 MB (19437145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7f7e1f8b68d6c669bde19aab0eedcabaa91ed7ff02bec3cfbfd7378ed95cf3`  
		Last Modified: Tue, 13 Jan 2026 22:57:56 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5080b84067bc7c24ecb25e7ac770570674e6d9500f960fed66968848f7df337`  
		Last Modified: Tue, 13 Jan 2026 22:57:56 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f843a80e4d8f11a30dacdedbfac773de8a9abb5f1cc8378022ce018b0faad3`  
		Last Modified: Tue, 13 Jan 2026 22:57:56 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff8cf4f50401bd2530ebd0169c97f66841cf0f4319eda63dddccdbdbd6995a1`  
		Last Modified: Tue, 13 Jan 2026 22:57:59 GMT  
		Size: 23.9 MB (23927488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad868f2bb31423610e93f45a95abce412ccea534fc462cdcbdcc5fc2d85eb843`  
		Last Modified: Tue, 13 Jan 2026 22:57:57 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bcd35751b80c0cadbe3f5a006a484adb11f58247738b2bd04e03af0977cd81f`  
		Last Modified: Tue, 13 Jan 2026 22:57:57 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d7737eff72ff71a4f32d33170b2cd3c4b8db70d550f6dc963ee501b94d0b242`  
		Last Modified: Tue, 13 Jan 2026 22:53:57 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d16627dde4ed12bcb9a9f2e7f5e040a692cc63123aa70ab855199db85871af3`  
		Last Modified: Tue, 13 Jan 2026 22:57:58 GMT  
		Size: 11.5 MB (11454704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
