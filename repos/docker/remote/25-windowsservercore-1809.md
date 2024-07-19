## `docker:25-windowsservercore-1809`

```console
$ docker pull docker@sha256:3a9bdb3986baa4a1f937fadb6b3e7015046eb811b5de0145e433f991857926c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `docker:25-windowsservercore-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull docker@sha256:d81e80a8ddaf887b4e0bf09816391101e8ae80d24a1905034b119e4de15507ae
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2295995729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4efb7ab3e62402a9350c9bb038540f3e9407d50c0451f57f5195b79627760d19`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Fri, 19 Jul 2024 18:09:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 19 Jul 2024 18:10:19 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 19 Jul 2024 18:10:20 GMT
ENV DOCKER_VERSION=25.0.5
# Fri, 19 Jul 2024 18:10:20 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-25.0.5.zip
# Fri, 19 Jul 2024 18:10:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 19 Jul 2024 18:10:46 GMT
ENV DOCKER_BUILDX_VERSION=0.16.1
# Fri, 19 Jul 2024 18:10:47 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.windows-amd64.exe
# Fri, 19 Jul 2024 18:10:47 GMT
ENV DOCKER_BUILDX_SHA256=34b8bd302364e9df99ebcd86658eae6ade175baf8baf6e74123ae04fcb2675c3
# Fri, 19 Jul 2024 18:11:11 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 19 Jul 2024 18:11:12 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.0
# Fri, 19 Jul 2024 18:11:12 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-windows-x86_64.exe
# Fri, 19 Jul 2024 18:11:13 GMT
ENV DOCKER_COMPOSE_SHA256=3dc98cacf0e0a05d8a714cc729827c062ff7ec13ffcd626e7b3767b362ce9b65
# Fri, 19 Jul 2024 18:11:37 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f98e7fe87492b83d7775a348ae0c94412b638ab5bba1a80b03c3a547708acd`  
		Last Modified: Tue, 09 Jul 2024 17:23:28 GMT  
		Size: 587.8 MB (587809033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69bde4d7e630597b341b24c075f74087f2fba5d387a3c79be654991603bc644`  
		Last Modified: Fri, 19 Jul 2024 18:11:42 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d301d16d03c3693f404a96d3a55366bbad4136c98d868eecd715241dbb87b47b`  
		Last Modified: Fri, 19 Jul 2024 18:11:42 GMT  
		Size: 497.8 KB (497792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c22e67eeb887c31206d65f3a375bce8e8b088e4fc30e32f91187ff34780bdf`  
		Last Modified: Fri, 19 Jul 2024 18:11:41 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:349b90cfb5ab5149fd966183c044b7ee48ef986a2e0483542d4c54014e7266ef`  
		Last Modified: Fri, 19 Jul 2024 18:11:41 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f580ca13f3a91cb5058e94510a8f8c144cd387e35c169a13a7b1a148dc6c72`  
		Last Modified: Fri, 19 Jul 2024 18:11:42 GMT  
		Size: 18.1 MB (18087070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2048691d1d6595a013520ef51b53d5e60775829be1d7d9199d776d75aaf6a084`  
		Last Modified: Fri, 19 Jul 2024 18:11:40 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91989d66d3c8d4fa3fe2cc4865e343ea5539298c462b9921fd8a594dad9cb8fa`  
		Last Modified: Fri, 19 Jul 2024 18:11:40 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:470e3afea724ba02046672482cd6a33c0739e1703a615688533024fbf2aac9cd`  
		Last Modified: Fri, 19 Jul 2024 18:11:40 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e7dfd18c48c775422b9f12c592ac1d66454f6e246ab8ed20a24f5ee5816f60`  
		Last Modified: Fri, 19 Jul 2024 18:11:42 GMT  
		Size: 19.3 MB (19268406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e9ac73594dd83995bbc102ac6eaebe08c1662495a49bcb6ec791d9dc1f5d41`  
		Last Modified: Fri, 19 Jul 2024 18:11:39 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf6f1be5cda46001edc34da6981b4c7163183a5c9900c9b862a4bfc5200f85b6`  
		Last Modified: Fri, 19 Jul 2024 18:11:39 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93865f2e5c5ccd98078a8ca13cc7cc3186cd895524b109533d5d3f723f79276f`  
		Last Modified: Fri, 19 Jul 2024 18:11:39 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58daa65758112d01e18111112bed25f0700b732843b386053be6c07904bd2bcb`  
		Last Modified: Fri, 19 Jul 2024 18:11:42 GMT  
		Size: 19.7 MB (19701425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
