## `docker:28-windowsservercore`

```console
$ docker pull docker@sha256:d310dcc104666bdc130f204f4b9d1fb7341508a9710b53a056e440710d60c667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `docker:28-windowsservercore` - windows version 10.0.26100.4946; amd64

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

### `docker:28-windowsservercore` - windows version 10.0.20348.4052; amd64

```console
$ docker pull docker@sha256:eb6f5bdee0b917a0166dd09697ebf7523a47bbb9eedff9c3fcd94f6da9229515
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2348315302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:862156614f9b71954f5eb537a6e0666c4aa6f92cc9bee96f43dd5670b4d0ad2e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Thu, 04 Sep 2025 16:37:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 04 Sep 2025 16:37:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 04 Sep 2025 16:37:44 GMT
ENV DOCKER_VERSION=28.4.0
# Thu, 04 Sep 2025 16:37:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.4.0.zip
# Thu, 04 Sep 2025 16:37:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 04 Sep 2025 16:37:59 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Thu, 04 Sep 2025 16:37:59 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.windows-amd64.exe
# Thu, 04 Sep 2025 16:38:00 GMT
ENV DOCKER_BUILDX_SHA256=0e8d520269cbd3401de6fee5c5fe48d5a9750805aa0a04d5443eba6b33ba63ee
# Thu, 04 Sep 2025 16:38:12 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 04 Sep 2025 16:38:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Thu, 04 Sep 2025 16:38:14 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-windows-x86_64.exe
# Thu, 04 Sep 2025 16:38:15 GMT
ENV DOCKER_COMPOSE_SHA256=6580793b1f612150646a9f8d02148c8d226a0033ed6e2e3273c0229b25e2f158
# Thu, 04 Sep 2025 16:38:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094e686abb50ed610efa2d2119b8b47ec7d084a26bdef14981602cc13c310d52`  
		Last Modified: Thu, 04 Sep 2025 16:39:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de315b89123744d0a2c35f049f2ab57abb3ff0fffbed4c0e5e8a84b11ceaaeb`  
		Last Modified: Thu, 04 Sep 2025 16:39:16 GMT  
		Size: 346.2 KB (346221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa5913f6f133abe4fe39aa61eca9f36d9668ad1c6b526689e637ba691aca603b`  
		Last Modified: Thu, 04 Sep 2025 16:39:18 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71641ae48932e5c912d5d030ea7e887af1fa1788e30d40431ceae695b4862b7`  
		Last Modified: Thu, 04 Sep 2025 16:39:19 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ccf004a39758d6680d4e9616dd62ed6b444714f57993e7da88ea78dab9990da`  
		Last Modified: Thu, 04 Sep 2025 16:39:22 GMT  
		Size: 20.8 MB (20774154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc22e1fbb5d926272d1d3776bcedfc49aaf40325a4db88f573416af531e0065`  
		Last Modified: Thu, 04 Sep 2025 16:39:22 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080429cbd76c321c5eee6bf8a41980d51e38247d36872d9aa12d05df4caab074`  
		Last Modified: Thu, 04 Sep 2025 16:39:24 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f261d4e587132106031cc78b1ca97192d48e7517756741928b9f299288b127`  
		Last Modified: Thu, 04 Sep 2025 16:39:24 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a3cfb7a91eed39c2d18fb330ff069eb01bbf9d75be384c0af725841100e33`  
		Last Modified: Thu, 04 Sep 2025 16:39:28 GMT  
		Size: 23.1 MB (23115790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaa0629f86f001c85171b8b9f62ab9fea873f048f8e29c0000b31dcf9e1f0ce`  
		Last Modified: Thu, 04 Sep 2025 16:39:28 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664c1c32e8b0e01bfdbf6c0fa1346a8a3110e7eff0136c584f14c60b1b6cdfbf`  
		Last Modified: Thu, 04 Sep 2025 16:39:28 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dbadfce131a1e248f8826a1f5b7dc97a54653345cd1d831d2350ed9dc260430`  
		Last Modified: Thu, 04 Sep 2025 16:39:30 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6608c0b462ef63fb87222b883b5afdb0a3a55ca8b63bc2d2e1d7ef3397faf737`  
		Last Modified: Thu, 04 Sep 2025 16:39:32 GMT  
		Size: 22.4 MB (22375579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
