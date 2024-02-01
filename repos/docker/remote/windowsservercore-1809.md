## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:96eede3e26a9d6e100e249e8d39d3e98cfeb13e4285c00bee075a57e416242df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull docker@sha256:7afe55ee4d35f0ae937c9c0287fa354602c0f44abf2bc1ddc6973ade68bcf399
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2125369211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffa1de2e54c97ed14f1b5ff985aa06be99e04e8a82b43d0404bf11faee113c45`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 01 Feb 2024 18:57:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 01 Feb 2024 19:00:09 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 01 Feb 2024 19:00:09 GMT
ENV DOCKER_VERSION=25.0.2
# Thu, 01 Feb 2024 19:00:10 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-25.0.2.zip
# Thu, 01 Feb 2024 19:00:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 01 Feb 2024 19:00:51 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Thu, 01 Feb 2024 19:00:51 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.windows-amd64.exe
# Thu, 01 Feb 2024 19:00:52 GMT
ENV DOCKER_BUILDX_SHA256=0ff0853a09960ff8f454d5db7253d5d935f5538856ea4985a276cbd1b28a96a5
# Thu, 01 Feb 2024 19:01:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 01 Feb 2024 19:01:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.5
# Thu, 01 Feb 2024 19:01:22 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.24.5/docker-compose-windows-x86_64.exe
# Thu, 01 Feb 2024 19:01:24 GMT
ENV DOCKER_COMPOSE_SHA256=eb60363d21a5c85eff2d2e18a4ed94d84d5016be59471d77d520046fdd888aa9
# Thu, 01 Feb 2024 19:01:54 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478d6ecf0327e4279df746be8ab3190f6505346fd2dda8edcfa31241bba21863`  
		Last Modified: Thu, 01 Feb 2024 19:02:00 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9794702b0628b713ef65780f5e33940f12a1b13cf262429eee8242bcad2699b3`  
		Last Modified: Thu, 01 Feb 2024 19:02:00 GMT  
		Size: 495.6 KB (495560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e7b8f811ae50bab28256a63b57e7b7a247cbe20459a21a85a13134aaae26a6`  
		Last Modified: Thu, 01 Feb 2024 19:01:59 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49df1e247a4545fac48288c77950066fb988b82973a096408b665287fc14ce81`  
		Last Modified: Thu, 01 Feb 2024 19:01:59 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf04180ef5c2c26a6df737c4bbaa20babb2b2dba3e49fd6dfa78ae3a1bcfbb0`  
		Last Modified: Thu, 01 Feb 2024 19:02:00 GMT  
		Size: 18.1 MB (18072453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db9091486738c582ac624ee37dbe4ae8e7f5748af500e795169596e654a94b0`  
		Last Modified: Thu, 01 Feb 2024 19:01:58 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d9c3b425b9fc499dbcb82bf7896fd8c10ac3245c36530aaa640b249b381234`  
		Last Modified: Thu, 01 Feb 2024 19:01:58 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe202f562e490e704169e278cdce408461572f01c11942dec57fb5e23f956a87`  
		Last Modified: Thu, 01 Feb 2024 19:01:58 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfffdbd31d3a2737b599969e0b2c727e3bf097452718fc9fbc38bb1c7b0ce61e`  
		Last Modified: Thu, 01 Feb 2024 19:01:59 GMT  
		Size: 18.0 MB (18021006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764f2d247a5db5a3c189be7ddae514d0ceea4c30f4be1b8a313e2f6850932804`  
		Last Modified: Thu, 01 Feb 2024 19:01:57 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66489fdddea1b4551d7caf1a728eee6449f893113356193bf8d0ce950419085e`  
		Last Modified: Thu, 01 Feb 2024 19:01:57 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3df1ea5f869c49614d3ee5d2cd348b91476ceca2ac8f6ba7359e02ae2e25373`  
		Last Modified: Thu, 01 Feb 2024 19:01:57 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28e3c32d497859bb02d5f796467d7550afa6bb9813cea830f44065a135e34f3`  
		Last Modified: Thu, 01 Feb 2024 19:01:59 GMT  
		Size: 19.0 MB (19046018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
