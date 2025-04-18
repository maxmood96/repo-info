## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:757bdd18ef8d0145fc31b04d9efa6b342e995c5730ae87cca24b09fe386eca03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull docker@sha256:fa4a5252403dada4d6667b31a2328102469c39978fc15e9d5230b9b57bdf57cb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2229951734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f07da4ca3fc3f4ab1b4902f294ef8e4bd3ed8a5fa69b614deeab1aecc414afe`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 18 Apr 2025 18:27:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 18:27:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 18 Apr 2025 18:27:56 GMT
ENV DOCKER_VERSION=28.1.1
# Fri, 18 Apr 2025 18:27:57 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.1.zip
# Fri, 18 Apr 2025 18:28:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 18:28:10 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Fri, 18 Apr 2025 18:28:11 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Fri, 18 Apr 2025 18:28:11 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Fri, 18 Apr 2025 18:28:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 18:28:20 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.1
# Fri, 18 Apr 2025 18:28:21 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-windows-x86_64.exe
# Fri, 18 Apr 2025 18:28:21 GMT
ENV DOCKER_COMPOSE_SHA256=971d6000e2c70da19c20f8264330a7ec3962b1fd59601afeb7e3636bad89b8c9
# Fri, 18 Apr 2025 18:28:30 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Fri, 18 Apr 2025 03:13:03 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77750cb2037c4c15c0a984f708a6e1eb3c64b41518569ebc07fcdcbfc5354e93`  
		Last Modified: Fri, 18 Apr 2025 18:28:35 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2840416346c6e36f9a79772ad2b67e522fad5eb4a68ee6ace4a208a2f85aa978`  
		Last Modified: Fri, 18 Apr 2025 18:28:35 GMT  
		Size: 347.6 KB (347588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e21fc1bf59e0f98f712c70844dfc96e8ee6b41849aa2598e49c3f54538ad2fd4`  
		Last Modified: Fri, 18 Apr 2025 18:28:34 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d115c110a9ac94ed19f5cede2415659895eeca1d3522e3491ed125179cedbf8`  
		Last Modified: Fri, 18 Apr 2025 18:28:34 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43395fdb4efc72c45c12813f3fe0074f9848951858b68b3b04140fe1df70684a`  
		Last Modified: Fri, 18 Apr 2025 18:28:36 GMT  
		Size: 19.9 MB (19888317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43ac641b009f14f9894c868e1a3d677933a58fddea1653aff4497db721d896e`  
		Last Modified: Fri, 18 Apr 2025 18:28:33 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4669876a07b458ddb211da924f5e5fb84e180198e748fb10863d55f18871f8b7`  
		Last Modified: Fri, 18 Apr 2025 18:28:33 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91cff0ccb3afa1be5504ab4990f29475076dc9e5a49d62855192bd2c60e12f4d`  
		Last Modified: Fri, 18 Apr 2025 18:28:33 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3a729e6501812c1529e54ea60d0fd2e4421d4a7203e7000a8555d8e2f62c15`  
		Last Modified: Fri, 18 Apr 2025 18:28:35 GMT  
		Size: 22.3 MB (22348494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:717eb7c17e60eb2bb1787c1a5c0b4a1a7f12a275fd0e0f0af401f9653d298e08`  
		Last Modified: Fri, 18 Apr 2025 18:28:32 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3df88de9c4e5098ce3c9512001f7eb08e07fb4bb314be9272906321a0ec45c`  
		Last Modified: Fri, 18 Apr 2025 18:28:32 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5331ddad4fd7495b4a3d08138c7c5d36f71c2280ca3c95819392d30e90a70791`  
		Last Modified: Fri, 18 Apr 2025 18:28:32 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e355d203c9eb8a7dfc7749e3e4d8195c28676de98a3bebfda8578b75e8a64ab`  
		Last Modified: Fri, 18 Apr 2025 18:28:35 GMT  
		Size: 21.8 MB (21829906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
