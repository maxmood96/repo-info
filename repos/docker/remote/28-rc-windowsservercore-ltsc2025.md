## `docker:28-rc-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:297b74ce86d8b83a188359185120cc3c21bddc22e74f6687c4938e12821c080f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `docker:28-rc-windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull docker@sha256:e7eb01ef30763b05a7ab89bf0a5bcc4539771c7c514afa24e79d90aa8171ebf2
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2563581224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6fe1521e8e50230a21cee4b8ad0b577601270fb338550c21606a4197e7596b9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Wed, 19 Feb 2025 19:30:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 19 Feb 2025 19:30:57 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 19 Feb 2025 19:30:58 GMT
ENV DOCKER_VERSION=28.0.0-rc.3
# Wed, 19 Feb 2025 19:30:58 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.0.0-rc.3.zip
# Wed, 19 Feb 2025 19:31:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 19 Feb 2025 19:31:08 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Wed, 19 Feb 2025 19:31:09 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.windows-amd64.exe
# Wed, 19 Feb 2025 19:31:09 GMT
ENV DOCKER_BUILDX_SHA256=39f53ec70c6ce37beca6898809e8eb89a77a1651be35ea50b51629c7a5d3b1f2
# Wed, 19 Feb 2025 19:31:18 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 19 Feb 2025 19:31:18 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Wed, 19 Feb 2025 19:31:19 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-windows-x86_64.exe
# Wed, 19 Feb 2025 19:31:19 GMT
ENV DOCKER_COMPOSE_SHA256=1324e382e1a79efaee4be288aae847f8a2862acf270d5621c17dff3a10d5ee83
# Wed, 19 Feb 2025 19:31:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13aeeafa3c5b42e6eb09139ab522e7a14d41786c0c99fa02b55aca9e4cd20ce2`  
		Last Modified: Wed, 19 Feb 2025 19:31:37 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fd549b1fe1ee27cb87fe1b9622e787e30b13bb3cfec19c3f9a1befe4d75765f`  
		Last Modified: Wed, 19 Feb 2025 19:31:37 GMT  
		Size: 390.9 KB (390880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c445df674b950f7616f8e60d3da321647d6d4195e795ff9281bd6b2f3c0ede28`  
		Last Modified: Wed, 19 Feb 2025 19:31:36 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac8040f490f22fb01107e6a33b0ad4cc73509d47874da947540ec8579c221b2`  
		Last Modified: Wed, 19 Feb 2025 19:31:36 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b449893f0384191cc7841a4e0bfac5903455b5132a945f437696c4f9c1fe916e`  
		Last Modified: Wed, 19 Feb 2025 19:31:37 GMT  
		Size: 19.8 MB (19848978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9785a550ce7713b968adba3c60cfaf5cfe2bd2f10d09616a23c583e2aeead9`  
		Last Modified: Wed, 19 Feb 2025 19:31:34 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4d1cac9d41dcba3bea041e105ff475e6135c8bbc52fa03c0882ad6ca4a082e1`  
		Last Modified: Wed, 19 Feb 2025 19:31:34 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13da6cc0a7cc76f93a324b53c601c4c609d3b78ec14b5709be6efc27d3a1ed9e`  
		Last Modified: Wed, 19 Feb 2025 19:31:34 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b078868ef9418575cb339b53e5609e28f2a085b39c8cb10b9827ea50467139`  
		Last Modified: Wed, 19 Feb 2025 19:31:35 GMT  
		Size: 21.2 MB (21184986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc82f3d526f1224549ab1894f1308a191f3739526ad39b48dddb38ad9d0f632e`  
		Last Modified: Wed, 19 Feb 2025 19:31:32 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d27e24e5e8c293f3608eb471c78e0e546beeec06fe598761c3971ff2f66f9a3`  
		Last Modified: Wed, 19 Feb 2025 19:31:32 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c2062f18320a75fd3b9f64196e285eb6974d6244f19d841917df94adb49009`  
		Last Modified: Wed, 19 Feb 2025 19:31:32 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d41a82dc97e577936dcf36037d36f79a829971ac46424bda579c18f0a0a0a35`  
		Last Modified: Wed, 19 Feb 2025 19:31:35 GMT  
		Size: 21.9 MB (21867026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
