## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:8d0835ed32e5cc7f3f9e6b68cd2d4cac29c38876898c089fd59830787eb4337b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull docker@sha256:a0b1d9fb195f66785738c01d6c62b1a51a81f24f998e140e62d685ce5bc3312e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2279094300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d1b5c5b23aa6a526b0deedcb75f0b86bef204be5fdbaca9177e1539c044c3b4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Thu, 27 Jun 2024 01:03:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 27 Jun 2024 01:03:58 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 27 Jun 2024 01:03:59 GMT
ENV DOCKER_VERSION=27.0.2
# Thu, 27 Jun 2024 01:04:00 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.0.2.zip
# Thu, 27 Jun 2024 01:04:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 27 Jun 2024 01:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Thu, 27 Jun 2024 01:04:23 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.windows-amd64.exe
# Thu, 27 Jun 2024 01:04:24 GMT
ENV DOCKER_BUILDX_SHA256=d28cff3df9fdbb37aa7434edb09d8befe5e90e5ef5887807569b694f25bebd33
# Thu, 27 Jun 2024 01:04:45 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 27 Jun 2024 01:04:45 GMT
ENV DOCKER_COMPOSE_VERSION=2.28.1
# Thu, 27 Jun 2024 01:04:46 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-windows-x86_64.exe
# Thu, 27 Jun 2024 01:04:46 GMT
ENV DOCKER_COMPOSE_SHA256=7dbd8848d9b8dce489c4d2ce1bb4f4b7a3dccb07a08596ae98b85091e1645bcc
# Thu, 27 Jun 2024 01:05:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb60f1f279085c8975699ac98ad55390174a3182d366ffb9735bd167febfb64b`  
		Last Modified: Thu, 27 Jun 2024 01:05:16 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e50dd6ee6c7e2372fb0ac02d03b6df21d2131427a3ffaac1b255e7e4df26e0e`  
		Last Modified: Thu, 27 Jun 2024 01:05:16 GMT  
		Size: 481.0 KB (480983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3eda9aa4684950b5d0e56f410debcc8e7e25fdf37d1a0704d0d01695842a235`  
		Last Modified: Thu, 27 Jun 2024 01:05:15 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b470aae016a4e0f295cf47fb5fb62e21874084cb2a9464f9517229afbed928`  
		Last Modified: Thu, 27 Jun 2024 01:05:15 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0e48f836b015addcf17586a3a74bfb9ea55d844be0ed21924c9222438d3d05`  
		Last Modified: Thu, 27 Jun 2024 01:05:17 GMT  
		Size: 19.3 MB (19259334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46cd9999d1a0edbdddab9da18ae9579756f8724ac0de7549066774f6987e3198`  
		Last Modified: Thu, 27 Jun 2024 01:05:13 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b39c70e1fd84289c611c8329c68d5910d8252e92c7aa1f7e4d209cff9bd7ba`  
		Last Modified: Thu, 27 Jun 2024 01:05:13 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa24887152330797202e25a72ff49df071e2e06c702ca17482e8b694522f219a`  
		Last Modified: Thu, 27 Jun 2024 01:05:13 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcda61c65b2028acd26b71d0dc5122871ea886a6647593969b502baa51c1764f`  
		Last Modified: Thu, 27 Jun 2024 01:05:14 GMT  
		Size: 19.0 MB (19016401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e9739913466e997c8359d3b6baaa04ead36d3567c53ecbe3041b1e4ed3e9c8`  
		Last Modified: Thu, 27 Jun 2024 01:05:11 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d54b3a34de892715b0791f9d06d1732735758114262572b4fbec940dd4b2a5`  
		Last Modified: Thu, 27 Jun 2024 01:05:11 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe5ee12631088270a5400d37b18365f519a85d8a3b137aef478d123fa488300`  
		Last Modified: Thu, 27 Jun 2024 01:05:11 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6651b31ae4c14fc636755d5ce1ee0d34e3b4788613704b6d7b5985053c7d2fd4`  
		Last Modified: Thu, 27 Jun 2024 01:05:14 GMT  
		Size: 19.6 MB (19644583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
