## `docker:28-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:2d99acb3911040c398b54e203664f1bb3f30d631567e6c22f94471cd2a07bf2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `docker:28-windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull docker@sha256:c6af21ade2208ca9d20fe8457b12b16b37eefb5cb8e1eab3b7a6fb6cb29a0850
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2565153977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee3a63716a70a26977e6804b01e6ad4007ab5c7e2a0e11c9187c3ff3d4c63dc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Thu, 20 Feb 2025 23:31:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2025 23:31:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 20 Feb 2025 23:31:52 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 23:31:53 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Thu, 20 Feb 2025 23:32:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:32:02 GMT
ENV DOCKER_BUILDX_VERSION=0.21.0
# Thu, 20 Feb 2025 23:32:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.windows-amd64.exe
# Thu, 20 Feb 2025 23:32:03 GMT
ENV DOCKER_BUILDX_SHA256=a8e63d104cfb4b1441d6eb429639851758902c6caf1ef5e3d4dfb3964683a26d
# Thu, 20 Feb 2025 23:32:12 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2025 23:32:12 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Thu, 20 Feb 2025 23:32:13 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-windows-x86_64.exe
# Thu, 20 Feb 2025 23:32:13 GMT
ENV DOCKER_COMPOSE_SHA256=1324e382e1a79efaee4be288aae847f8a2862acf270d5621c17dff3a10d5ee83
# Thu, 20 Feb 2025 23:32:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0abc4fcc716cb3612e21277a1d5e347ab084efa34aa1506026d976ac740669a`  
		Last Modified: Thu, 20 Feb 2025 23:32:31 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44143bd449ed2ddb12cc185866e9ffaf170c9dd65a47343a0b26ba0e0ff635f`  
		Last Modified: Thu, 20 Feb 2025 23:32:32 GMT  
		Size: 381.9 KB (381862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28fe44f3a93de078d2e55f2449169d17571aa58102c4bec0cc14ea54a64b3cab`  
		Last Modified: Thu, 20 Feb 2025 23:32:30 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b5616553b212171c81c9af672c68ced9462fa220ee7be1368d9daebbceb4fe4`  
		Last Modified: Thu, 20 Feb 2025 23:32:30 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d486eb75b4840fd967627654b66a5679f6365de540165faba1cd667408dec628`  
		Last Modified: Thu, 20 Feb 2025 23:32:32 GMT  
		Size: 19.8 MB (19840865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a58c75cbfd9331326a90d78126319ff6e3243d78bd7040c036ff1196845ffa6`  
		Last Modified: Thu, 20 Feb 2025 23:32:28 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1b98ad10aa2f0a3e34e7b65d860cf5625ac0be1880c7cd0559f055492f790d`  
		Last Modified: Thu, 20 Feb 2025 23:32:28 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1bbbce321843ab282459c96da80563b79844a123d4f1137e40098dbda90805`  
		Last Modified: Thu, 20 Feb 2025 23:32:28 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2c35f98977d7e6c2d5c424b574ada5a43f2e7f281bef877502876164e52cba`  
		Last Modified: Thu, 20 Feb 2025 23:32:29 GMT  
		Size: 22.8 MB (22779749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f3fd507d9981a362a4e755014278dbcf5d9afb190f7831a18974ae90fdae9d`  
		Last Modified: Thu, 20 Feb 2025 23:32:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac71939f6efc0646836df52799338120fc0833faeaf99ef2766dcc98f8d4360`  
		Last Modified: Thu, 20 Feb 2025 23:32:26 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6d1aa6872befa667df3f2d57be253749a7fcb43ac2c4bb48ab388e35a06ac8`  
		Last Modified: Thu, 20 Feb 2025 23:32:26 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9cfe66c021ab64a0700db9296f95a38d99c55b122a2f644ab606cf512b66842`  
		Last Modified: Thu, 20 Feb 2025 23:32:29 GMT  
		Size: 21.9 MB (21862166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
