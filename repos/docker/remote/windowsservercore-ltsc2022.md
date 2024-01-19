## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:54ced1aafd1cf7070f735f49b8d69894d28358e4bf2ae22b7bf173ea6ebd0525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull docker@sha256:6b8259bd12ae50d4f3a4da8a20b6589a7bfc7dd1fb8191d0caf73a65631c8079
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1955834875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05dfc09b8c49d0e31dfc403ac3732c555e646188e96088e064e6cd7de3c363c5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Fri, 19 Jan 2024 19:56:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 19 Jan 2024 19:57:34 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 19 Jan 2024 19:57:35 GMT
ENV DOCKER_VERSION=25.0.0
# Fri, 19 Jan 2024 19:57:35 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-25.0.0.zip
# Fri, 19 Jan 2024 19:57:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 19 Jan 2024 19:57:51 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Fri, 19 Jan 2024 19:57:51 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.windows-amd64.exe
# Fri, 19 Jan 2024 19:57:52 GMT
ENV DOCKER_BUILDX_SHA256=0ff0853a09960ff8f454d5db7253d5d935f5538856ea4985a276cbd1b28a96a5
# Fri, 19 Jan 2024 19:58:01 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 19 Jan 2024 19:58:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.1
# Fri, 19 Jan 2024 19:58:02 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-windows-x86_64.exe
# Fri, 19 Jan 2024 19:58:03 GMT
ENV DOCKER_COMPOSE_SHA256=6c94193c282d5fba71563c617fe8ddf8dce9355fb1d0ae93609221c590d06fcb
# Fri, 19 Jan 2024 19:58:16 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7b29984406400e27422d66eceb0c590ece5b39a87c4e5e198311ccbcbd94905`  
		Last Modified: Fri, 19 Jan 2024 19:58:23 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d6a91c6e66e9ea719075f4b043af04f5d8c543f1ab831c38bf6970c8c3404a9`  
		Last Modified: Fri, 19 Jan 2024 19:58:23 GMT  
		Size: 493.3 KB (493283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0a8434832a1e0fdb2a905bb0d187da0a42c4bd9cc7379c552356e7b3ede583`  
		Last Modified: Fri, 19 Jan 2024 19:58:22 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432aacaad25117f5eb7008425104a53f5b9c6151bb7cef7a8a7e4b8ab80a65bf`  
		Last Modified: Fri, 19 Jan 2024 19:58:21 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75dc67f094334798d737642719dcc955348bdc9dc572e374ea6a7df4e5c25f11`  
		Last Modified: Fri, 19 Jan 2024 19:58:23 GMT  
		Size: 18.1 MB (18066911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b87c5a1213ab405c6a703b5699b89da7697fa96bbfc9ad3818c5a5b8cc45a834`  
		Last Modified: Fri, 19 Jan 2024 19:58:20 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a11bf92b0f5e0d7618bf2293a703b952c1673f345c16e3b3ce22ee73be111bf`  
		Last Modified: Fri, 19 Jan 2024 19:58:20 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b71e7fffc15d2cd15fcef7f69b1c7204451fa8a6b75e9a29b15348645ae560`  
		Last Modified: Fri, 19 Jan 2024 19:58:20 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30729ff3d893cf1f4c54e7442f6ff7a9d6958ad131757a063e28399d58542d3`  
		Last Modified: Fri, 19 Jan 2024 19:58:22 GMT  
		Size: 18.0 MB (18018659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c45bef06c4e46fd8f3f555c38eb5179617de9bb6216514409a999b7024a9e7`  
		Last Modified: Fri, 19 Jan 2024 19:58:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b3a105f9d0dc66f8fa508383fe9edfd94a1d81147f091fd8156ab134ebf302`  
		Last Modified: Fri, 19 Jan 2024 19:58:19 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a61cf7fea29a079742858c156e4e159540ae6a976dfaafd0a3a2c6484fe1970`  
		Last Modified: Fri, 19 Jan 2024 19:58:19 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c0df69284fc4b930691828bed9713e2c9c120910e6994e099c907444c34e96`  
		Last Modified: Fri, 19 Jan 2024 19:58:22 GMT  
		Size: 19.0 MB (19031605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
