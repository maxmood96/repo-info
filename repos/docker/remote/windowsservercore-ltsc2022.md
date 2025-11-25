## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:91412ff46badf31ce4699f5e9d82be8b02fbbca022548cb007503e26afab9365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull docker@sha256:7ae25d65fdc44f74dfcb42ac45cc95752a7e31bc1871b0f62d2dcb2e1be27de4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1836531699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63f71db32d3545e3ba27b3fa0660dd591083474c29c45da34fa08d509ab85cd5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Mon, 24 Nov 2025 21:54:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 24 Nov 2025 21:55:40 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 24 Nov 2025 21:55:41 GMT
ENV DOCKER_VERSION=29.0.3
# Mon, 24 Nov 2025 21:55:42 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.3.zip
# Mon, 24 Nov 2025 21:56:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 24 Nov 2025 21:56:07 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Mon, 24 Nov 2025 21:56:09 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Mon, 24 Nov 2025 21:56:09 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Mon, 24 Nov 2025 21:56:36 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 24 Nov 2025 21:56:36 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Mon, 24 Nov 2025 21:56:36 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Mon, 24 Nov 2025 21:56:37 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Mon, 24 Nov 2025 21:56:57 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aad132d44253f5455efa330566900fe031331917e6f95f4055d2072ead42290`  
		Last Modified: Mon, 24 Nov 2025 22:10:27 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a94d695b738baabcb36a9ee4dd2ae774a3d28346f99344190a638f7057c5b2`  
		Last Modified: Mon, 24 Nov 2025 22:10:26 GMT  
		Size: 511.1 KB (511143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b39c7f41162291e15ecef388e331bb737cf5fe8ea8184634d7a6f0488a18513`  
		Last Modified: Mon, 24 Nov 2025 22:10:26 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c503151d79205bb8c940a651a350f5eaf0056b5ed5ce1e4584f9730bb4a0ad8e`  
		Last Modified: Mon, 24 Nov 2025 22:10:27 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5dfd1d3c0c508848f1bb7b8fd2051812f194662bdef7170b56059918e928374`  
		Last Modified: Mon, 24 Nov 2025 22:10:28 GMT  
		Size: 19.4 MB (19428546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a2255ec3a2fab3c949ebdd35ce97c19b0fff1095684c41ff5385c6659bdd62`  
		Last Modified: Mon, 24 Nov 2025 22:10:26 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f1b96e3575e0b1046b77c87785ae5c12bb6fbb73381bfa2ff9369d46f68b790`  
		Last Modified: Mon, 24 Nov 2025 22:10:26 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d87b1063f0b429b5275b393879322365f835980bfeb07c88349eccfaaf5b4abd`  
		Last Modified: Mon, 24 Nov 2025 22:10:26 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba2f1364f034f19cce254b5e2dc75e1171c3f4d9f3412dee10f35309487dfe1`  
		Last Modified: Mon, 24 Nov 2025 22:10:28 GMT  
		Size: 23.9 MB (23934159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dad982c61a45cb5e840d821a9c5f04432f60cda5c4cd50848a8ccf36361c088`  
		Last Modified: Mon, 24 Nov 2025 22:10:26 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e7e882587e0a9e883a9bc7defea5d9406a3fe397c35759c5277f629e4f8582`  
		Last Modified: Mon, 24 Nov 2025 22:10:26 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d362dfd4907931b36e49c62ebeb74b74c1a663eb62d2ea46093a1ec206acc243`  
		Last Modified: Mon, 24 Nov 2025 22:10:26 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f7b61044f9a0b888a52b1ab90fd7e92332503843a81694ac4d24761d3ee078`  
		Last Modified: Mon, 24 Nov 2025 22:10:30 GMT  
		Size: 22.7 MB (22684532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
