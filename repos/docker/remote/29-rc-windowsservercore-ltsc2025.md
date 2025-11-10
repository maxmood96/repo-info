## `docker:29-rc-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:61996ba3943fd58089479f359a25ed106d1aff4800dc4461bb45d3e936e28dc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `docker:29-rc-windowsservercore-ltsc2025` - windows version 10.0.26100.6905; amd64

```console
$ docker pull docker@sha256:6a65cd6a524741192fd36c4343b919e03f529b1f45af819acd55e52c7588a94d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3286027237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5444fb8e0b7ae31ce6da35b08640c4c0426abdad5a31c561f10ab73e3a1ead76`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Mon, 10 Nov 2025 19:46:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 10 Nov 2025 19:58:03 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 10 Nov 2025 19:58:03 GMT
ENV DOCKER_VERSION=29.0.0-rc.3
# Mon, 10 Nov 2025 19:58:04 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-29.0.0-rc.3.zip
# Mon, 10 Nov 2025 19:58:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 10 Nov 2025 19:58:14 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Mon, 10 Nov 2025 19:58:15 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Mon, 10 Nov 2025 19:58:16 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Mon, 10 Nov 2025 19:58:24 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 10 Nov 2025 19:58:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Mon, 10 Nov 2025 19:58:25 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Mon, 10 Nov 2025 19:58:25 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Mon, 10 Nov 2025 19:58:34 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdb4f820c244e1b1c141421c0709d2cf6df07421598eaec46bdb8b9e00226ee`  
		Last Modified: Mon, 10 Nov 2025 19:57:03 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e4b230c8b474a8f20b90c8957b19a34ede365dc050cb55cc7b09bc789e4366`  
		Last Modified: Mon, 10 Nov 2025 19:58:52 GMT  
		Size: 390.6 KB (390562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544b74ada335d74a92c8360bdff7e4f61eb2b87a1d3d8bb393ce57ffc082a3c4`  
		Last Modified: Mon, 10 Nov 2025 19:58:52 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e3190c214e15f6de32a65de66d4c36a3010516c30d820faabe926ac26e2698`  
		Last Modified: Mon, 10 Nov 2025 19:58:52 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea3f1068bc3723165e65180f1f0434b610e0cc4e936524dd2f4e80229a6df7c`  
		Last Modified: Mon, 10 Nov 2025 19:58:55 GMT  
		Size: 19.4 MB (19409507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:702c1eb7480a02cc770a960a56eec29683911af10eea78d12dfd263abac3843f`  
		Last Modified: Mon, 10 Nov 2025 19:58:52 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf86e31a33b1da7cee039db1677533cc6c762f6776763c12aeac7f0b07dbf0b`  
		Last Modified: Mon, 10 Nov 2025 19:58:53 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448bf0a4288eb8319efbf71b13730c7382a5fd7f02f67a4d58479a4361fcaa5a`  
		Last Modified: Mon, 10 Nov 2025 19:58:53 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec8c195c4ae27a5e6fc996c8878261f65a3d8498a6f9f0746aeab7a4c607f67`  
		Last Modified: Mon, 10 Nov 2025 19:58:56 GMT  
		Size: 23.2 MB (23178166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:247f6355d877947c76e78d32b0dee6c0e85185a9d22eae9640b7f7ac6536d24b`  
		Last Modified: Mon, 10 Nov 2025 19:58:53 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ffaeb533c627dc4da5f7b1d388685810aed401462dfb6bf9129f6e01d2d589d`  
		Last Modified: Mon, 10 Nov 2025 19:58:53 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4120858aa8be6d51ab5ec44d8faa958e1f3709fa890a7d897bc1a5db1a87e63`  
		Last Modified: Mon, 10 Nov 2025 19:58:53 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e55b2ce4633c6f1532bf524d78d746d30a6eb883380bb76973815ffb4e1d5e2`  
		Last Modified: Mon, 10 Nov 2025 19:58:58 GMT  
		Size: 22.7 MB (22690200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
