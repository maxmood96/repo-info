## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:3b16a51f7b350f70417bf9bd061388412d4fe13605c264cd3965ad44c040b98f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull docker@sha256:0dfbb2cb73e0f119f7827c4294818bae9e2b593f4f499366be7ab74496416a06
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346334126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2405e622d57138fe3077ec39b9f3f42ebcd0cfdf09f47419ba243ae7fdd5b79`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Thu, 03 Jul 2025 17:22:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 03 Jul 2025 17:22:31 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 03 Jul 2025 17:22:33 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 17:22:34 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.1.zip
# Thu, 03 Jul 2025 17:22:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 03 Jul 2025 17:22:51 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 17:22:52 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Thu, 03 Jul 2025 17:22:53 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Thu, 03 Jul 2025 17:23:06 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 03 Jul 2025 17:23:08 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 17:23:09 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-windows-x86_64.exe
# Thu, 03 Jul 2025 17:23:11 GMT
ENV DOCKER_COMPOSE_SHA256=1f50233952bdcef70d4b753112363a67e9af0f56a2eabfc9ba60444879b81638
# Thu, 03 Jul 2025 17:23:24 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b61b501a45983587b82cbf3ec9a02d5dc816be481f91442c358c854092ae35f`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f44a2afa65d60b4bf8e64db5fe87206c5d6caea4df5f91ab8520f7775c6108`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 361.4 KB (361411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a33626ee108dfe569f1ac806973edaad156af082da5adb5cdc619d671c92af`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3415464cc927cf6550b8b02ab9a1c7d7076b523ce7f3eb3d6cb06af3cb0717cd`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ece6c486f7a91317125ee5a8a9703bd97ad6fe62ffa3eed7300b64d6dae5658c`  
		Last Modified: Thu, 03 Jul 2025 17:23:46 GMT  
		Size: 20.8 MB (20833794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7cca4e9c6c6042835085a7bec40bfedfff801d6a5bb1c55fd0d69f3cb4224c5`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e45039c40258e0ad1ddc66ea6789239b16daa6e4b25ad6133a2a0f9155e84e`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d056b131a087efcd1c66a659d7faab0e72b58a72df8d673e794b12df4133e2`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec084cd1ecfecc49f2aee4ece051aaf3b0e26d486dc4f206b8cdca3c459bbba3`  
		Last Modified: Thu, 03 Jul 2025 17:23:44 GMT  
		Size: 22.7 MB (22657606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746d4353372224213706d143dd92b6b6bb55a75ea19c08d8bf0a1831262fae78`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3131944c8f3aa2bfd1c82fa466a67d152080ddf612067169becafb202be3370`  
		Last Modified: Thu, 03 Jul 2025 17:23:42 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbcaf71c6e95bc4ab5d255abea93afd44db0486b886ce5701bced2305375566`  
		Last Modified: Thu, 03 Jul 2025 17:23:43 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67da6c0deee4b547055907682ae68fc855d99f2e93d43f6e5b6959c0dd55db5e`  
		Last Modified: Thu, 03 Jul 2025 17:23:45 GMT  
		Size: 22.2 MB (22218098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
