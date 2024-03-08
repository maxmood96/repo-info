## `docker:rc-windowsservercore-1809`

```console
$ docker pull docker@sha256:61cb9bb84ea8367ee51ba9ff2e054c36a67cd73101fe5b71ba42528f68b6ef53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `docker:rc-windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull docker@sha256:30f3b15a96f56fcea080dcc50ad0e1640c80e59ea694eb40270b1df2725a4833
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2137050346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54abc4ffd402355d984244a9c3e61d697308d177fbe8aeb12a82356f1df98ab3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Fri, 08 Mar 2024 16:55:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 08 Mar 2024 16:57:19 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 08 Mar 2024 16:57:19 GMT
ENV DOCKER_VERSION=26.0.0-rc2
# Fri, 08 Mar 2024 16:57:20 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-26.0.0-rc2.zip
# Fri, 08 Mar 2024 16:57:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 08 Mar 2024 16:57:58 GMT
ENV DOCKER_BUILDX_VERSION=0.13.0
# Fri, 08 Mar 2024 16:57:59 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.windows-amd64.exe
# Fri, 08 Mar 2024 16:58:00 GMT
ENV DOCKER_BUILDX_SHA256=001dd8c707862d7c7a7bc17ebb024922ee304bddad1bca11da5b3b3ff18effa6
# Fri, 08 Mar 2024 16:58:32 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 08 Mar 2024 16:58:33 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.7
# Fri, 08 Mar 2024 16:58:33 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-windows-x86_64.exe
# Fri, 08 Mar 2024 16:58:34 GMT
ENV DOCKER_COMPOSE_SHA256=1a5ffa12cff51a65f4e5e8874ed46b0783cfbc8f5ef837f5b9523decf1afd1d0
# Fri, 08 Mar 2024 16:59:02 GMT
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
	-	`sha256:dde18b6a751e9c41a722e841150e6b2181dca41f3ff9acd03ede3b278b9dbecf`  
		Last Modified: Fri, 08 Mar 2024 16:59:08 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e38543b094f2f28622600d2646b350f6157187c0c5da7d3e088df147b4b943`  
		Last Modified: Fri, 08 Mar 2024 16:59:08 GMT  
		Size: 509.2 KB (509244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57d26b90873ab6b11f7d32b5d6eaaf7b2455b3d0a4941f9ad7d461cb6ee80e7b`  
		Last Modified: Fri, 08 Mar 2024 16:59:07 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c7ec87e948fca7fcc106ef2165b96dfd7174c72bf93510ed5b2b5a96bb3cec`  
		Last Modified: Fri, 08 Mar 2024 16:59:07 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:024dcd3a432e4bcea2fd135cd8a1b7b0ce0ee8d6702714e978bf46b6cded80b1`  
		Last Modified: Fri, 08 Mar 2024 16:59:09 GMT  
		Size: 18.1 MB (18126512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ee9126f2de23a8fac15ea7bd03b42718846915c704a69f221a4cbd5d9635c0`  
		Last Modified: Fri, 08 Mar 2024 16:59:06 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd4a15e4a2598090d41fff89585359dc08cd3542d632d8ada6823bd55c570419`  
		Last Modified: Fri, 08 Mar 2024 16:59:06 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feb42077cd6165d0bff3191f50d90547a0d641e045677df05a085b3203142397`  
		Last Modified: Fri, 08 Mar 2024 16:59:06 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a456c292e397abb7d648023354a5e6573663a68d167814dde538fde343b423d`  
		Last Modified: Fri, 08 Mar 2024 16:59:07 GMT  
		Size: 18.9 MB (18853819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df69579361fa27574957b70626b329d2428896bbd1eb65c6622c4117ba7f554`  
		Last Modified: Fri, 08 Mar 2024 16:59:05 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d22dd87edd418f8105040b12c07d7d40e1d9b542005159a0c0f5300a96a636`  
		Last Modified: Fri, 08 Mar 2024 16:59:05 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c840126da9b72421d25be83e19daf10d56413f31892e9ac94e3caae3be075d7a`  
		Last Modified: Fri, 08 Mar 2024 16:59:05 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed2e0d7662f2043b523cd1ed3f9077217e0ee275ab095568589e72dd8d7f1c8`  
		Last Modified: Fri, 08 Mar 2024 16:59:08 GMT  
		Size: 19.1 MB (19100201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
