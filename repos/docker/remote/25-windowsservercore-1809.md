## `docker:25-windowsservercore-1809`

```console
$ docker pull docker@sha256:a60b0d73418f94bd6786fa52f8f82532add815e00ce6cdf083810eddc59e4ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `docker:25-windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull docker@sha256:d7c0bb72602262d5330a1b77f0b4404d2205c854de35261143338e81e8640cb5
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2136048849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91a61d476b6fc7a95a1f2f4879a12767812c1d8f02a43b6fca9f7de60971f830`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Fri, 16 Feb 2024 20:00:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 16 Feb 2024 20:01:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 16 Feb 2024 20:01:56 GMT
ENV DOCKER_VERSION=25.0.3
# Fri, 16 Feb 2024 20:01:56 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-25.0.3.zip
# Fri, 16 Feb 2024 20:02:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 16 Feb 2024 20:02:23 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Fri, 16 Feb 2024 20:02:23 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.windows-amd64.exe
# Fri, 16 Feb 2024 20:02:24 GMT
ENV DOCKER_BUILDX_SHA256=0ff0853a09960ff8f454d5db7253d5d935f5538856ea4985a276cbd1b28a96a5
# Fri, 16 Feb 2024 20:02:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 16 Feb 2024 20:02:48 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.6
# Fri, 16 Feb 2024 20:02:48 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-windows-x86_64.exe
# Fri, 16 Feb 2024 20:02:49 GMT
ENV DOCKER_COMPOSE_SHA256=7a25ec49a53320fbe218c59ac7aafb05440725894322d396d4b353ad198b9dff
# Fri, 16 Feb 2024 20:03:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:998aa414ce1eba4c4c875cff3890c7189edc0a4f0f76f842966d00697b69098f`  
		Last Modified: Fri, 16 Feb 2024 20:03:23 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afee02ea6cd2b152635c64ed5fe69cb5dcb2358d7224463a92e5d36effa9781a`  
		Last Modified: Fri, 16 Feb 2024 20:03:23 GMT  
		Size: 473.1 KB (473084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe68f4489f6d0df9303428eafc1dd799062a9e5062606216c67ceac3ad8ccc65`  
		Last Modified: Fri, 16 Feb 2024 20:03:22 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb169a83fc13c3375252139b39ee6a47e47871d9954f05c175cb5f05256379e`  
		Last Modified: Fri, 16 Feb 2024 20:03:22 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0390d3349d58fbc7decaf8168618152d31e7659539f0f6cf92cff2e521dcb1`  
		Last Modified: Fri, 16 Feb 2024 20:03:23 GMT  
		Size: 18.1 MB (18056703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66468abe3c19da402a99390f58eb9297dd7ec27bb70075e312f81136ef00cbf9`  
		Last Modified: Fri, 16 Feb 2024 20:03:20 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:257d236fb21946445bef9dc5f828cd9a1f217cf0849bd784f8abf3c267443daf`  
		Last Modified: Fri, 16 Feb 2024 20:03:20 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee618fcdf75a697a55bd6029753e515c9aed1646d729b629e879ac46a34bb12`  
		Last Modified: Fri, 16 Feb 2024 20:03:19 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d37b58b2a379423f16a4c0c7127322df10ca99fa7c67a3ca7fbce010e120a10`  
		Last Modified: Fri, 16 Feb 2024 20:03:20 GMT  
		Size: 18.0 MB (18008794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fed0e2309fcfb7c6276396dee9bd83dc5106e1dc0d09e50d174e09944995f7c`  
		Last Modified: Fri, 16 Feb 2024 20:03:18 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d35624ba99ea43bcbf6dcd4e7513d347ba74bf735ae747f7129c67d60616cc9`  
		Last Modified: Fri, 16 Feb 2024 20:03:18 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1d414cd1a064ae384fe874b6186da1466aaa78225746ab4ed1aaaf8d505f98`  
		Last Modified: Fri, 16 Feb 2024 20:03:18 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6475924a59af36ebad5f50954174b2209c6162eb3ec8463c7631f82400d9e7a2`  
		Last Modified: Fri, 16 Feb 2024 20:03:21 GMT  
		Size: 19.0 MB (19049826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
