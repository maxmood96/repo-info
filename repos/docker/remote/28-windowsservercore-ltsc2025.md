## `docker:28-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:00efa870cb48d2587069580480eec0b1dbf1481faa14c899a74fc786b18562cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `docker:28-windowsservercore-ltsc2025` - windows version 10.0.26100.4946; amd64

```console
$ docker pull docker@sha256:fc1d6bad286c2196deac451802cd23d47b94df11471c3f5aa45c0451aa144c23
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3565687349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd86967abc969619cf15cb316b4655852b26bfc78b595290036aa0dd0be9ab8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Thu, 04 Sep 2025 16:43:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 04 Sep 2025 16:43:18 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 04 Sep 2025 16:43:19 GMT
ENV DOCKER_VERSION=28.4.0
# Thu, 04 Sep 2025 16:43:20 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.4.0.zip
# Thu, 04 Sep 2025 16:43:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 04 Sep 2025 16:43:32 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Thu, 04 Sep 2025 16:43:33 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.windows-amd64.exe
# Thu, 04 Sep 2025 16:43:34 GMT
ENV DOCKER_BUILDX_SHA256=0e8d520269cbd3401de6fee5c5fe48d5a9750805aa0a04d5443eba6b33ba63ee
# Thu, 04 Sep 2025 16:43:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 04 Sep 2025 16:43:45 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Thu, 04 Sep 2025 16:43:46 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-windows-x86_64.exe
# Thu, 04 Sep 2025 16:43:46 GMT
ENV DOCKER_COMPOSE_SHA256=6580793b1f612150646a9f8d02148c8d226a0033ed6e2e3273c0229b25e2f158
# Thu, 04 Sep 2025 16:43:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2898e6004f49e597b695d0c53804e527ec4793460bd0fb31919840fb602eac1f`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f980581ec82cfd499a9b882fab07566f097108af3c395ec53d21d84f2d4f16`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 409.6 KB (409626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3637f5a05e9bd3c6fab37cd60d3aebc6bb8c8baa9d0af2ed5265721b466d51d4`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefb774cbd620af5732ba60e9735037f0ea44c36b3043058573e7fe624b3b760`  
		Last Modified: Thu, 04 Sep 2025 16:47:45 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a893a2ffa36e8727431a764f47f1e19ec08d586dcd4552fa26b4957cbf5fc1`  
		Last Modified: Thu, 04 Sep 2025 16:47:46 GMT  
		Size: 20.8 MB (20830914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f6c55ed8ead9c441357463a56923afa9ddf576805aa38088fc647cc5fdd749`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20df657bca87688f70f0e6fd540efd9e57aae577340ad34ac278037940e96906`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c313824fb8e112f8238d34fa7fef1355d68e3509de5bd5503f7b1e841ca59119`  
		Last Modified: Thu, 04 Sep 2025 16:47:45 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0e1669c94883277151466c7021efb3fcfb06743c95e16f4c6cc23bf9c7c96b`  
		Last Modified: Thu, 04 Sep 2025 16:47:47 GMT  
		Size: 23.2 MB (23172252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b26d01d1eec0619079e96b29826040aeb561198ac789a3b25d2d4435b0d9da`  
		Last Modified: Thu, 04 Sep 2025 16:47:44 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c70ed5069c6f4288552a987cdaf316232b3436f7b290c4f0b6947c4f7ebbfe4`  
		Last Modified: Thu, 04 Sep 2025 16:47:45 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91f979a2a1b0cc06ab6cadf7355e5440d0c898703737c700d2f483fa8b60893`  
		Last Modified: Thu, 04 Sep 2025 16:47:45 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32eb3b2c4200cf3eab578e5386699f03e78491f8cccb194606cb968f5faf6328`  
		Last Modified: Thu, 04 Sep 2025 16:47:47 GMT  
		Size: 22.4 MB (22432260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
