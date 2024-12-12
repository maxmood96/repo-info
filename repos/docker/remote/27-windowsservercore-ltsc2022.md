## `docker:27-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:45c22851cf72f61a4e547a3f463bbda654e522e65cba15b4247ede09604aa839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `docker:27-windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull docker@sha256:d730d8d6c3dbd7df9f2b9d32b691f882bb43eb0b2d2c2f494bd3c4714fba4ca1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2312881317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b8092038cb643cfa233747b9b88e672db1b648151527359d717c12393598c3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:37:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:37:30 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Dec 2024 20:37:31 GMT
ENV DOCKER_VERSION=27.4.0
# Wed, 11 Dec 2024 20:37:31 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.4.0.zip
# Wed, 11 Dec 2024 20:37:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 11 Dec 2024 20:37:42 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Wed, 11 Dec 2024 20:37:42 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.windows-amd64.exe
# Wed, 11 Dec 2024 20:37:43 GMT
ENV DOCKER_BUILDX_SHA256=6b13e5bdd8a40548886b69cc94716ff2f9a06db513983a0f158f80a3f2486432
# Wed, 11 Dec 2024 20:37:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 11 Dec 2024 20:37:52 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Wed, 11 Dec 2024 20:37:52 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-windows-x86_64.exe
# Wed, 11 Dec 2024 20:37:53 GMT
ENV DOCKER_COMPOSE_SHA256=93fa851954c19e0e19b753817eca37c81c9f4394b0db1853ebc66cd62230ea75
# Wed, 11 Dec 2024 20:38:01 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c09883867ef5aa72f43e5eaa93c715ab38d9ad59499f13350b429f8a6a125fc3`  
		Last Modified: Wed, 11 Dec 2024 20:38:10 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d37ff27f932a659579ee294e7861f17e9a454fc081e204734869f99edebee39`  
		Last Modified: Wed, 11 Dec 2024 20:38:10 GMT  
		Size: 336.0 KB (336029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d30e509b25298b1c7a765b8b5e77d08d72b8cd91078ba9f96784ba8757657e5e`  
		Last Modified: Wed, 11 Dec 2024 20:38:09 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:487d59e3d2421346ae47c67cf3d01f4ce3ee18c1cfcf4cd6fa0df004a8ea6366`  
		Last Modified: Wed, 11 Dec 2024 20:38:09 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982f674be6bdc85d4a7b2bbc01a90205a6759554b73cf796ba432f3dcc2a4e12`  
		Last Modified: Wed, 11 Dec 2024 20:38:10 GMT  
		Size: 19.0 MB (18981905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a86cd30b24c56735a1c64ca9fb910b2318793e29024949328e243d03c0e7f9`  
		Last Modified: Wed, 11 Dec 2024 20:38:07 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804dc38056184bf564a960d4633679e43bc77808a147e89b89e355d2c21c952a`  
		Last Modified: Wed, 11 Dec 2024 20:38:07 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e96d53bdf227707cf69ea9dd513fb6e191c803852e1b57fb5020a29efa65d2`  
		Last Modified: Wed, 11 Dec 2024 20:38:07 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3a6c189585d120ff74a2187178678391fe856218194dcb665b9bf0ee48afe06`  
		Last Modified: Wed, 11 Dec 2024 20:38:08 GMT  
		Size: 19.6 MB (19633895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59110b27cc11a3b5f936e220d61ff5fec746f769280133a0cd03d8f3c330732a`  
		Last Modified: Wed, 11 Dec 2024 20:38:05 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832cbabb807105c95934d086b134ab6486d58e0c77f22da000c3857edfdde7e3`  
		Last Modified: Wed, 11 Dec 2024 20:38:05 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a8da44ddd9d566fd49ccda36f82d34c500a90672665560f299899bb4ffff14`  
		Last Modified: Wed, 11 Dec 2024 20:38:05 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b8095d0156b1f384e4d815f41ed05a2814ba13969e64af888b20aa1daabbe6`  
		Last Modified: Wed, 11 Dec 2024 20:38:08 GMT  
		Size: 20.0 MB (20044302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
