## `docker:25-windowsservercore`

```console
$ docker pull docker@sha256:1d20338de94c65505bc56d3b2bce41f23cd488bdcd421378d39344461cce8bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2582; amd64
	-	windows version 10.0.17763.6054; amd64

### `docker:25-windowsservercore` - windows version 10.0.20348.2582; amd64

```console
$ docker pull docker@sha256:91ffe0c34e34e0a551d939f11407dd6cc2c04eee3c5b481a9a69221cec7f7bad
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2196910024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a22df06b3f6339ea936a45f66d3609be4ec918c50fa60a38f46aa0485ec7e957`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 03 Jul 2024 10:07:02 GMT
RUN Install update 10.0.20348.2582
# Fri, 19 Jul 2024 17:58:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 19 Jul 2024 18:00:56 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 19 Jul 2024 18:00:57 GMT
ENV DOCKER_VERSION=25.0.5
# Fri, 19 Jul 2024 18:00:58 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-25.0.5.zip
# Fri, 19 Jul 2024 18:01:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 19 Jul 2024 18:01:23 GMT
ENV DOCKER_BUILDX_VERSION=0.16.1
# Fri, 19 Jul 2024 18:01:23 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.windows-amd64.exe
# Fri, 19 Jul 2024 18:01:24 GMT
ENV DOCKER_BUILDX_SHA256=34b8bd302364e9df99ebcd86658eae6ade175baf8baf6e74123ae04fcb2675c3
# Fri, 19 Jul 2024 18:01:35 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 19 Jul 2024 18:01:36 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.0
# Fri, 19 Jul 2024 18:01:37 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-windows-x86_64.exe
# Fri, 19 Jul 2024 18:01:37 GMT
ENV DOCKER_COMPOSE_SHA256=3dc98cacf0e0a05d8a714cc729827c062ff7ec13ffcd626e7b3767b362ce9b65
# Fri, 19 Jul 2024 18:01:46 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0206d135152eb909f50159d6ca348a5aead199afacbafc000b770c1b0720f6`  
		Last Modified: Tue, 09 Jul 2024 18:30:31 GMT  
		Size: 751.0 MB (751001543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b6f54531419e8a80008c54e0986c49f9783f9c9161be28ebc6f0214eddf5ee`  
		Last Modified: Fri, 19 Jul 2024 18:01:52 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8346fdc4f0adb02fed4917743fda8aa23a13b608ea3b12c80bce2fef2dd0e28`  
		Last Modified: Fri, 19 Jul 2024 18:01:52 GMT  
		Size: 370.1 KB (370139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e29b1d0ac79d5c7ab64beb17af5e0083610e248afdf8406bf292283e0b2fb84`  
		Last Modified: Fri, 19 Jul 2024 18:01:51 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2185462b74f344b26c5c00ba15418bab33e3b6ca434132b700329b19f40126`  
		Last Modified: Fri, 19 Jul 2024 18:01:51 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c08bdc3ba26252a2d3aa3be8842e0c12f5f168d4ac9956dbb4ec1fe90627dc3`  
		Last Modified: Fri, 19 Jul 2024 18:01:52 GMT  
		Size: 18.0 MB (18045800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20db6037fa79b5f2bda5828485d1e56c71d1463e149b6f408d69edd33fdd5bbb`  
		Last Modified: Fri, 19 Jul 2024 18:01:50 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255418fbc26936ee7f92c5aaf43b4aa9246b792cf0273908daeb81c662cbfe80`  
		Last Modified: Fri, 19 Jul 2024 18:01:50 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5aa17ad84634f2e317899df19cd69aba80f32c0d957b4f3f286072c68f6461`  
		Last Modified: Fri, 19 Jul 2024 18:01:50 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fb5a15328a2c74797ef0479c6fdc425080d49c10785d6ec94fcea64448e2308`  
		Last Modified: Fri, 19 Jul 2024 18:01:51 GMT  
		Size: 19.2 MB (19224115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03d18347e41557ed65f45cb39e18afbe1a43bddaaa2cd19d605a07460c4bcf17`  
		Last Modified: Fri, 19 Jul 2024 18:01:49 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dff7fd7b52608996d80f38df3851cc651832072299b6c649146fdb7120049a0`  
		Last Modified: Fri, 19 Jul 2024 18:01:49 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3612cbe504f568e21a845aa183b4aa1e7d2acfc4ae329fe20fb6dfe28e4292`  
		Last Modified: Fri, 19 Jul 2024 18:01:49 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a32b61fb02e2bfac9f3819b6a8b8dd682fcb8b2635dd5349a4738df8e72affe2`  
		Last Modified: Fri, 19 Jul 2024 18:01:52 GMT  
		Size: 19.7 MB (19658078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:25-windowsservercore` - windows version 10.0.17763.6054; amd64

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
