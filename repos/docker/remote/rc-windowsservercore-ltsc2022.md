## `docker:rc-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:938c22259a36fc1175cc01634964f79fc7808a64c6791ebe335c53caea1636fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `docker:rc-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:e4183d1631eb241188f37e6a3d773e954570aa143455688cded978c4ed67a683
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1890968166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:640c270ead5a61d318f08b5aa0bb13245e68bb4c7bd66e686f63caffb41a4522`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Tue, 20 Jan 2026 18:49:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 20 Jan 2026 19:08:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 20 Jan 2026 19:08:42 GMT
ENV DOCKER_VERSION=29.2.0-rc.2
# Tue, 20 Jan 2026 19:08:43 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-29.2.0-rc.2.zip
# Tue, 20 Jan 2026 19:08:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 20 Jan 2026 19:08:53 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 20 Jan 2026 19:08:54 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Tue, 20 Jan 2026 19:08:55 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Tue, 20 Jan 2026 19:09:04 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 20 Jan 2026 19:09:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.1
# Tue, 20 Jan 2026 19:09:05 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-windows-x86_64.exe
# Tue, 20 Jan 2026 19:09:05 GMT
ENV DOCKER_COMPOSE_SHA256=2ae341f9152b4d90f561f84b8f2e263d5b60e1613c6841c804447819290c4119
# Tue, 20 Jan 2026 19:09:12 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3380b620c58c596f1609e5dfd5ce2eb7bb472a207cd9fee48adb79d268f61ebb`  
		Last Modified: Tue, 20 Jan 2026 18:52:00 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675d3fbde35486e81e57bbe8c91e8665a2dc5046d4fafed8b6030f8eb8991bf9`  
		Last Modified: Tue, 20 Jan 2026 21:08:10 GMT  
		Size: 500.3 KB (500323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a0c145340521a54fedf72bd982eecd72120c8a7778650097c43fc6e6803a27`  
		Last Modified: Tue, 20 Jan 2026 19:09:37 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f535e21023d2ac8b0983451c2330771fc1b1ecc29fca1a2f6b6ca8956ad36c31`  
		Last Modified: Tue, 20 Jan 2026 19:09:37 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20791914f6f8068b046e4ad3e5693dcc99ecb7caae4781f52b9dbfb3513f4325`  
		Last Modified: Tue, 20 Jan 2026 19:11:46 GMT  
		Size: 19.4 MB (19428014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0927a69f584e8d247c0aee49b610bcede78db6662cc3e6a03ac58f49d276bde`  
		Last Modified: Tue, 20 Jan 2026 19:09:18 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cfbaf866fd999cc40f5c8bd143949aecab02d2b0f3a9e5a48376cac7951ac1e`  
		Last Modified: Tue, 20 Jan 2026 19:09:37 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:063344afb49ed12d85dc845f13f644cd7c2bcbcb4a980e5e347e04d844524a19`  
		Last Modified: Tue, 20 Jan 2026 19:09:18 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6026efc4ce426c358e30a8a995e4099cafc5e9e92a02e1a7d38c48a3bf1ee24`  
		Last Modified: Tue, 20 Jan 2026 19:09:40 GMT  
		Size: 23.9 MB (23924784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9d7bfe8cea82e5d266477c2c3890c9eb1f826457de364f66af031ed1c18405`  
		Last Modified: Tue, 20 Jan 2026 19:09:37 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f32cbb1d9f40711e1c75b8367cbebc35a1bfeed2218039f6236d6f997040aa`  
		Last Modified: Tue, 20 Jan 2026 21:08:34 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3f38cf7931d1604a798b66b332877e808dbd770dc65ba5a0c401fb4bb5f55b`  
		Last Modified: Tue, 20 Jan 2026 19:09:37 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f399303ce30e44d3532b226c2192ec82d8e19a1221c62f17d677898835b7bb7e`  
		Last Modified: Tue, 20 Jan 2026 19:11:56 GMT  
		Size: 11.4 MB (11443990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
