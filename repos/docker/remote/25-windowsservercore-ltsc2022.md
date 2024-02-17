## `docker:25-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:365bf51fd2ff1de50bd11962a235b900400f1abad2f5e72136e38ec89755cd65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2322; amd64

### `docker:25-windowsservercore-ltsc2022` - windows version 10.0.20348.2322; amd64

```console
$ docker pull docker@sha256:4d29a4b31129389662599816a2639079237a008d0596b9322cac7fe9f4df60fd
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1966278753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d9473363b20b662a86a75039a2f7a19e81576ead9ef32dc64edd19e846f16ef`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Fri, 16 Feb 2024 20:04:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 16 Feb 2024 20:04:30 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 16 Feb 2024 20:04:31 GMT
ENV DOCKER_VERSION=25.0.3
# Fri, 16 Feb 2024 20:04:32 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-25.0.3.zip
# Fri, 16 Feb 2024 20:04:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 16 Feb 2024 20:04:44 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Fri, 16 Feb 2024 20:04:45 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.windows-amd64.exe
# Fri, 16 Feb 2024 20:04:46 GMT
ENV DOCKER_BUILDX_SHA256=0ff0853a09960ff8f454d5db7253d5d935f5538856ea4985a276cbd1b28a96a5
# Fri, 16 Feb 2024 20:04:55 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 16 Feb 2024 20:04:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.6
# Fri, 16 Feb 2024 20:04:56 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-windows-x86_64.exe
# Fri, 16 Feb 2024 20:04:58 GMT
ENV DOCKER_COMPOSE_SHA256=7a25ec49a53320fbe218c59ac7aafb05440725894322d396d4b353ad198b9dff
# Fri, 16 Feb 2024 20:05:07 GMT
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
	-	`sha256:6ba1528d101a6563653e0b43f5603388a91c220902b334b485da640c35284459`  
		Last Modified: Fri, 16 Feb 2024 20:05:17 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c2e46c6f40f9c4e65d2c067155355926d95dbc5fb80dc6bf3b9232525649d29`  
		Last Modified: Fri, 16 Feb 2024 20:05:16 GMT  
		Size: 490.3 KB (490321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdda12728b9ef42f0c7ab317876b103e479adef457e8f128639f38e4bff52492`  
		Last Modified: Fri, 16 Feb 2024 20:05:15 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b9b9bf92805f0a7b75a446f70fc5ad03c0f6a551260aa2df6d0c17bb307088b`  
		Last Modified: Fri, 16 Feb 2024 20:05:15 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d2dbf386f0f7b2d8f5439cb1142b381b6142b57a4572daa8bcd8b448b70a474`  
		Last Modified: Fri, 16 Feb 2024 20:05:17 GMT  
		Size: 18.1 MB (18061796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a6f85ebc1b3476845f5a3a60fd3d8715c9ca5744a20d1f8b403068c8358556`  
		Last Modified: Fri, 16 Feb 2024 20:05:13 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5d83b6f54a280476ccf72759dc91ae7c8c2933836abcb0511adc1ca4fa596d`  
		Last Modified: Fri, 16 Feb 2024 20:05:13 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf3b0ff6742b4b988096f6e6c3b7bf5c8a1547efbcbbd19b73531cb96f620bf`  
		Last Modified: Fri, 16 Feb 2024 20:05:13 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50669ab6faab60100fd6b8c29d1a6e93ea80c457729f854f3ff69e7ab938e115`  
		Last Modified: Fri, 16 Feb 2024 20:05:14 GMT  
		Size: 18.0 MB (18007729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd523904d67bead603538822a626743ef274c56e9d6b61a796bab1ff6ab7009`  
		Last Modified: Fri, 16 Feb 2024 20:05:11 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed6c9579baa647e4085a496ced842d4411a0c0912a5d578099f79277259be30`  
		Last Modified: Fri, 16 Feb 2024 20:05:11 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded67a67226bfb4772ceddcb712fd5ed4be1b7a6910a71582205ba3f974fc56f`  
		Last Modified: Fri, 16 Feb 2024 20:05:11 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cc9fa6e1930567b2c7cb49e511303b28041cf8f3192e3226b16051be169c44d`  
		Last Modified: Fri, 16 Feb 2024 20:05:14 GMT  
		Size: 19.1 MB (19053037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
