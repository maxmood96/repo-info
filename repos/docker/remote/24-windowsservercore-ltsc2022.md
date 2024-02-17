## `docker:24-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:2f352d0626a2f65da4fee4611f8b037e8f79cba6b7ff6612f8b603a78f710c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2322; amd64

### `docker:24-windowsservercore-ltsc2022` - windows version 10.0.20348.2322; amd64

```console
$ docker pull docker@sha256:92484f739bd6ff5fc55ccb56ad11aa071a56298620d03bd9cb8d9ab02bfd2251
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1965791850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e253c0c4d496fe1d315df035da87380e558f28a1a3d3528846118771a66d393`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Fri, 16 Feb 2024 19:59:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 16 Feb 2024 20:00:10 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 16 Feb 2024 20:00:10 GMT
ENV DOCKER_VERSION=24.0.9
# Fri, 16 Feb 2024 20:00:11 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.9.zip
# Fri, 16 Feb 2024 20:00:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 16 Feb 2024 20:00:21 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Fri, 16 Feb 2024 20:00:22 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.windows-amd64.exe
# Fri, 16 Feb 2024 20:00:22 GMT
ENV DOCKER_BUILDX_SHA256=0ff0853a09960ff8f454d5db7253d5d935f5538856ea4985a276cbd1b28a96a5
# Fri, 16 Feb 2024 20:00:30 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 16 Feb 2024 20:00:31 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.6
# Fri, 16 Feb 2024 20:00:32 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-windows-x86_64.exe
# Fri, 16 Feb 2024 20:00:32 GMT
ENV DOCKER_COMPOSE_SHA256=7a25ec49a53320fbe218c59ac7aafb05440725894322d396d4b353ad198b9dff
# Fri, 16 Feb 2024 20:00:40 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f1d9b8108e7b21446783f2fe2e43f67b6cf0da6f19aae1fb401ae7ac33c95e`  
		Last Modified: Fri, 16 Feb 2024 20:00:46 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a7cf809e4171818e5d454a237103349c59caa89177c170f5db2acf6015155a2`  
		Last Modified: Fri, 16 Feb 2024 20:00:46 GMT  
		Size: 501.0 KB (501048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:639204ad8eaa39d45914b46a2f06e221364fa6e4268d7c1abc39f9aa56e0aed6`  
		Last Modified: Fri, 16 Feb 2024 20:00:45 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8405a7ca182adb17907795cf6f6a206e4ba57a1db2e3e8fb2edcb21767eb78b9`  
		Last Modified: Fri, 16 Feb 2024 20:00:45 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1a9ddc2e943e369aca6c3330341515e0b2251802502ff849d141edbe7a7844`  
		Last Modified: Fri, 16 Feb 2024 20:00:47 GMT  
		Size: 17.5 MB (17540939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df864e6ead0e235db87283ebeecff45291db6962026f16045164dd19611061a1`  
		Last Modified: Fri, 16 Feb 2024 20:00:44 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53f6e2d0ac91464ed9b5d72d673e8022c87b2dbc2e99632d4d413c816c9512d`  
		Last Modified: Fri, 16 Feb 2024 20:00:44 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b9371b25c19626d7b4fc22c24a15da98bfda8a1e7dc07a960c4f5af27ab1a0d`  
		Last Modified: Fri, 16 Feb 2024 20:00:44 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b51db43017a32a3cc3792530ef815ed0852cef50a3299f99882e2bd26bc84f`  
		Last Modified: Fri, 16 Feb 2024 20:00:46 GMT  
		Size: 18.0 MB (18019530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b9567a257dae06703ad887c9c6e2d1d2328621011a7f14bef5d3fc298e7500`  
		Last Modified: Fri, 16 Feb 2024 20:00:43 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad75b2409b61a0e398ff3ada9a449eb75c109b19af402216f0614e39a540b613`  
		Last Modified: Fri, 16 Feb 2024 20:00:43 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205c98fbd41f6c243a27e39b2b1f38331ac2244d4245fe72258c4f8c4cdaa67b`  
		Last Modified: Fri, 16 Feb 2024 20:00:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe5ec6cb98ba8840bb52b795e11da81481489678777cdb94335108e6a547c7a`  
		Last Modified: Fri, 16 Feb 2024 20:00:45 GMT  
		Size: 19.1 MB (19064606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
