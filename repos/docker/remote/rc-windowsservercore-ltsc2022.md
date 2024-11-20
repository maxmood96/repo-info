## `docker:rc-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:e58465e5b2c0f7e44b7396791c1be8a340f40d6796787a5de0d324be211a17e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2849; amd64

### `docker:rc-windowsservercore-ltsc2022` - windows version 10.0.20348.2849; amd64

```console
$ docker pull docker@sha256:fb4d9047bed4bf9ceb8b6fc881e05f576898919782d5a973e7b22d23daee2fc7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2311255877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5540ecb36fdf249bfd2a96f304710810e9e35ef701c0a72751f87ac38c13458`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Wed, 20 Nov 2024 00:36:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 20 Nov 2024 00:36:25 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 20 Nov 2024 00:36:26 GMT
ENV DOCKER_VERSION=27.4.0-rc.2
# Wed, 20 Nov 2024 00:36:27 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-27.4.0-rc.2.zip
# Wed, 20 Nov 2024 00:36:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 20 Nov 2024 00:36:39 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Wed, 20 Nov 2024 00:36:39 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Wed, 20 Nov 2024 00:36:40 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Wed, 20 Nov 2024 00:36:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 20 Nov 2024 00:36:47 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.3
# Wed, 20 Nov 2024 00:36:48 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-windows-x86_64.exe
# Wed, 20 Nov 2024 00:36:48 GMT
ENV DOCKER_COMPOSE_SHA256=30be0d2d5df4d032ffeee3f8c5e6dccc2ef1b2911732055778c3584e9e69bb4b
# Wed, 20 Nov 2024 00:36:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be68c275fbf52323d6158bd7d95561a357315b3ff54ba1f7890eca61609a5d53`  
		Last Modified: Wed, 20 Nov 2024 00:37:02 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18999337d98c45d527ce3204e22784f757e2cdf59e61e68e5e0a276a58abee16`  
		Last Modified: Wed, 20 Nov 2024 00:37:01 GMT  
		Size: 359.3 KB (359302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e0351d48ea00ffe242770b45ea4bb2d3303235fe366b13377c40e2630793cc`  
		Last Modified: Wed, 20 Nov 2024 00:37:00 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9daa6f6e65d56c95c63030bc70bb70cb937616f5147214147ac99ab8c7277b53`  
		Last Modified: Wed, 20 Nov 2024 00:37:04 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:221a5e4c2fc15048553987afa3d0f0bf3ab229b3db007996112fd46302d2c922`  
		Last Modified: Wed, 20 Nov 2024 00:37:01 GMT  
		Size: 19.0 MB (18995146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756403d765a854b20f801f86af8c80a2c7cc4bd666e92aaea4477813bae04f4a`  
		Last Modified: Wed, 20 Nov 2024 00:36:59 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79efbc7a86b716eb43cf5f3601e3c8ce7a4acd9f3f293144bd90f5e5ee77a3b9`  
		Last Modified: Wed, 20 Nov 2024 00:36:59 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c5f56a95327d47b8f712b4e3d1485e6eaf66b8ffa06b40b9c9cd2d704fd12f`  
		Last Modified: Wed, 20 Nov 2024 00:36:59 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1da1ce4e381209bd909892e0a70ed4e5e854a8057cb5c2f721d7008cf7d6aef`  
		Last Modified: Wed, 20 Nov 2024 00:37:00 GMT  
		Size: 19.4 MB (19412070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8ddfe355cb7fe2ec598296ec0f870756406e89e288bb756ed7613b47a13368`  
		Last Modified: Wed, 20 Nov 2024 00:36:58 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36bad091aeb9f1dab1c92b58146851f69600ee5050e5b1d05efdfd3a4be2e8c`  
		Last Modified: Wed, 20 Nov 2024 00:36:58 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:182c8b2e5132cbcf2ee4df8a6e5b1479215cd9da33726ef1ab2dc2db91448a52`  
		Last Modified: Wed, 20 Nov 2024 00:36:58 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b48c74b9f914f73518d8e078680e07a4bff873ca4578451e139ebcc215511f`  
		Last Modified: Wed, 20 Nov 2024 00:37:01 GMT  
		Size: 20.0 MB (19993580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
