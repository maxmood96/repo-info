## `docker:28-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:0bf48d9a532ee99590404446aa118456133cd1d185d833adbdc1651fc9775a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `docker:28-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull docker@sha256:9cfbbc0c47b3d74e2b4acbb2d1ecbf1b4c6aa1a081e36e83a298a24ef712e187
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2338728028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4d3bd2e5c31f2e53cb16c94c00ada54223e1d375e620f6d75a081386b5c8df`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Thu, 29 May 2025 21:25:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 29 May 2025 21:25:30 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 29 May 2025 21:25:31 GMT
ENV DOCKER_VERSION=28.2.1
# Thu, 29 May 2025 21:25:31 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.1.zip
# Thu, 29 May 2025 21:25:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:25:43 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 29 May 2025 21:25:44 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 29 May 2025 21:25:45 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 29 May 2025 21:25:52 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 29 May 2025 21:25:53 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Thu, 29 May 2025 21:25:54 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Thu, 29 May 2025 21:25:55 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Thu, 29 May 2025 21:26:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Tue, 13 May 2025 18:47:51 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9996051669ebc9f677525c2f9e3f3907b83d532458e7e458743e257b0653fe`  
		Last Modified: Thu, 29 May 2025 21:26:07 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ea772f3227a649c94df0b75d868575f27721903a8952f13cef20fc66408dff`  
		Last Modified: Thu, 29 May 2025 21:26:07 GMT  
		Size: 357.2 KB (357241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf95b219aa8166bdb0e94cc700997c85e89cbb0279d8ff5d490ffa3467e53ab`  
		Last Modified: Thu, 29 May 2025 21:26:06 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aafec18fc8fe985b0887f569f9f8018faadcb00268240ea9d81073d352873195`  
		Last Modified: Thu, 29 May 2025 21:26:06 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c258bfdce0fccaf645b84232ad6265812514fe1826f498ce55a3594a0ffbee1d`  
		Last Modified: Thu, 29 May 2025 21:26:08 GMT  
		Size: 20.5 MB (20453019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ebd1101e990c3ea686cbe2763e17b78ad84217d4a35f5e9bb5a41bcdf08651`  
		Last Modified: Thu, 29 May 2025 21:26:05 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1131d2a7c3b2637e2c8f0aa6d3ac739af178b70ac806f8f2c6ad36eb16aa000`  
		Last Modified: Thu, 29 May 2025 21:26:05 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8fc15b58d7a34308be08e2b75378bb2c00a20368f03643b0d9f771ae05af23`  
		Last Modified: Thu, 29 May 2025 21:26:05 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec094ce259f8b869dad0446d00ab9a4ba3bbecc473c19fda5e45c29110808ae`  
		Last Modified: Thu, 29 May 2025 21:26:07 GMT  
		Size: 22.3 MB (22264100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a563bda5736d13931960edbf446049db45c3eda9e2d95da2e8ea01a71fc8af`  
		Last Modified: Thu, 29 May 2025 21:26:05 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75581968b9da95c59e118c47aac6bcf26bd822c907b2fe2238d5d854fee2523c`  
		Last Modified: Thu, 29 May 2025 21:26:04 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e98811cf36a8c8bbab46082a419c5a94f94bae2a2bd156f2da2dda54024c06e`  
		Last Modified: Thu, 29 May 2025 21:26:04 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47475f6eeacadf030030e1795650ff74e6f1155a696cedd8a5bb350b9b66f9a3`  
		Last Modified: Thu, 29 May 2025 21:26:08 GMT  
		Size: 22.0 MB (22013985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
