## `docker:29-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:65d69e478d154dcd1d17bbcf927c745a8848d18178f7e2f873218d4a680ea452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `docker:29-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:ee68e301a03e75079c01f22d7bdf250372fbf33cfbaba1fcd848fc97e6e8fe89
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1890899910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb2ec5e34aa8764996c2802af76e21daa199f224ee33313f7f3ff1b13e6af9d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Tue, 13 Jan 2026 22:52:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Jan 2026 22:52:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 13 Jan 2026 22:52:54 GMT
ENV DOCKER_VERSION=29.1.4
# Tue, 13 Jan 2026 22:52:55 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.4.zip
# Tue, 13 Jan 2026 22:53:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 13 Jan 2026 22:53:06 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 13 Jan 2026 22:53:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Tue, 13 Jan 2026 22:53:08 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Tue, 13 Jan 2026 22:53:29 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 13 Jan 2026 22:53:29 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.1
# Tue, 13 Jan 2026 22:53:30 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-windows-x86_64.exe
# Tue, 13 Jan 2026 22:53:31 GMT
ENV DOCKER_COMPOSE_SHA256=2ae341f9152b4d90f561f84b8f2e263d5b60e1613c6841c804447819290c4119
# Tue, 13 Jan 2026 22:53:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:28:58 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a0d275cb0351c261395acf080ca5b3e97a23bd3d8c039e16ca5ae8c7e28ac6`  
		Last Modified: Tue, 13 Jan 2026 23:01:24 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5074850d7c08ce585f28cf232f2e5ef1f287bf318c3d65f7c74fe1b241160a84`  
		Last Modified: Tue, 13 Jan 2026 23:01:24 GMT  
		Size: 480.5 KB (480490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc737c53518c3dab214c544245a0fe0edaeccd814fb2f98d42e969583e0325c`  
		Last Modified: Tue, 13 Jan 2026 23:01:24 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51e7bb3e21f1fb65e489168021729ca475b29318d2671857b9d245f27153658`  
		Last Modified: Tue, 13 Jan 2026 23:01:24 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14cecc523c71b4b7913f23e3f402d06be412af7c63217a9072cea5362dd69ecb`  
		Last Modified: Tue, 13 Jan 2026 23:01:33 GMT  
		Size: 19.4 MB (19409719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dab87f5c3cc4cbded8a1ceea8a5fa3a75d3fc7a14e66c7bc55286d52c407ae0`  
		Last Modified: Tue, 13 Jan 2026 22:53:50 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b85b00f5ab53752bd082ee311643e060980a478f508df24b81aed31c16779471`  
		Last Modified: Tue, 13 Jan 2026 23:01:25 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a9561b2687e13cac640e23a15b83f194e35bab617866c3f927d455873089dc0`  
		Last Modified: Tue, 13 Jan 2026 23:01:25 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f4976e6ca69582fd40cc1f2efe323050f9cb4d24f7a44efcf71d50f18bd26bb`  
		Last Modified: Tue, 13 Jan 2026 23:01:29 GMT  
		Size: 23.9 MB (23909311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2907fdc20ef864b02bc50b20d7f3edaa71edec6cdaabce5d7b41512e21fb4e21`  
		Last Modified: Tue, 13 Jan 2026 23:01:25 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:974d74880c54e030c32280ae27076f9e89e9cadec7f81e38ff86985392dd4d6d`  
		Last Modified: Tue, 13 Jan 2026 23:01:22 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b62e3a25deb6bb13ed5b2075438fce38d56861809331510916c7271080350d86`  
		Last Modified: Tue, 13 Jan 2026 23:01:24 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a703649241a6cba236c763d078750e29996a68ce02249abd1170c9bfffd35dae`  
		Last Modified: Tue, 13 Jan 2026 23:01:22 GMT  
		Size: 11.4 MB (11429367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
