## `docker:27-windowsservercore`

```console
$ docker pull docker@sha256:1b73107686e6a2535c6982f46ce868a759c4d68054d8c9672c406f00a00c62ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2529; amd64
	-	windows version 10.0.17763.5936; amd64

### `docker:27-windowsservercore` - windows version 10.0.20348.2529; amd64

```console
$ docker pull docker@sha256:7d27c6f62ccbc36566d155c5c42df1aa4d7ba1e0ed850456f789b28e3c17869b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2176544669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b40cb9da98a5610a6b6ec180d7ea7248609e6eadcaf9aea8387e484a24580658`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 19 Jun 2024 19:58:05 GMT
RUN Install update 10.0.20348.2529
# Thu, 27 Jun 2024 00:59:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 27 Jun 2024 01:00:08 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 27 Jun 2024 01:00:08 GMT
ENV DOCKER_VERSION=27.0.2
# Thu, 27 Jun 2024 01:00:09 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.0.2.zip
# Thu, 27 Jun 2024 01:00:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 27 Jun 2024 01:00:24 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Thu, 27 Jun 2024 01:00:24 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.windows-amd64.exe
# Thu, 27 Jun 2024 01:00:24 GMT
ENV DOCKER_BUILDX_SHA256=d28cff3df9fdbb37aa7434edb09d8befe5e90e5ef5887807569b694f25bebd33
# Thu, 27 Jun 2024 01:00:32 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 27 Jun 2024 01:00:32 GMT
ENV DOCKER_COMPOSE_VERSION=2.28.1
# Thu, 27 Jun 2024 01:00:33 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-windows-x86_64.exe
# Thu, 27 Jun 2024 01:00:33 GMT
ENV DOCKER_COMPOSE_SHA256=7dbd8848d9b8dce489c4d2ce1bb4f4b7a3dccb07a08596ae98b85091e1645bcc
# Thu, 27 Jun 2024 01:00:42 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb373ec9afdfc5f09b9380d981e0c61f9c7b48537b887135c7c66810086e705e`  
		Last Modified: Fri, 21 Jun 2024 00:27:54 GMT  
		Size: 729.6 MB (729591500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604843058c96dd7b322043c163375762b45b2a38b7c6201bae02fd3a0c139611`  
		Last Modified: Thu, 27 Jun 2024 01:00:50 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da0fc92e4446f5674bd86473d81dbf119a328439399c05745854f2826e946ddf`  
		Last Modified: Thu, 27 Jun 2024 01:00:50 GMT  
		Size: 366.7 KB (366676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852778aa5734adde5a493aa27c61c2bdd5ffc97eb645e2ce65615df9341d0ec1`  
		Last Modified: Thu, 27 Jun 2024 01:00:49 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9afea6bdd98098288ec355c1d9f6582d3359dbe84960b9fb7c62f3573d00012d`  
		Last Modified: Thu, 27 Jun 2024 01:00:48 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1e6644853ad41a46a636f2f297c487a17b6b3d8aac39525878af430224b723f`  
		Last Modified: Thu, 27 Jun 2024 01:00:50 GMT  
		Size: 19.3 MB (19275654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:762740b32cbee0fae2239adfe3aec568872c045694315bab527b77dec6764dea`  
		Last Modified: Thu, 27 Jun 2024 01:00:47 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2023527fc0e503fc8b0e103b09d0075bd1bd4a2c78a978358b337f3807369f0`  
		Last Modified: Thu, 27 Jun 2024 01:00:47 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8edc0bfe68bc0d1c789cd782c9fe20cefbf0bae8af00a880c716750955f6d056`  
		Last Modified: Thu, 27 Jun 2024 01:00:47 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e896901aa9786532e789b4eee539bbcb94b0612176b96f790e9e85883593fdfa`  
		Last Modified: Thu, 27 Jun 2024 01:00:49 GMT  
		Size: 19.0 MB (19032868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbed060b7dc422f09cc434ecdbcf8db685318d7fba9449490b5d57e70135f724`  
		Last Modified: Thu, 27 Jun 2024 01:00:45 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e18e59ba64fc9da412e33cfdfe4b06d4a821c8ecb177c023b083e423335477bf`  
		Last Modified: Thu, 27 Jun 2024 01:00:45 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340e991fbaeb3d6bd957e3bf0c766546346db1b17d2f2895c24e0a5f27ce1fa3`  
		Last Modified: Thu, 27 Jun 2024 01:00:45 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e65a3214e3b43870ba74675f64af0494cd1be7ddef11c5fbcf0935886ef78b0`  
		Last Modified: Thu, 27 Jun 2024 01:00:48 GMT  
		Size: 19.7 MB (19667632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27-windowsservercore` - windows version 10.0.17763.5936; amd64

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
