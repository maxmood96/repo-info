## `docker:24-windowsservercore-1809`

```console
$ docker pull docker@sha256:a4bf93e7c13696917cbd8d90353a8041bb0d6793281d4b93150a31839ec83ca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `docker:24-windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull docker@sha256:eeb5d5cf6f1a4f2fc29550cbc61db70a5a375a73ffcbe8196a9b4f3045e4f7ac
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2135556869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:223e6ed32b6e0178709ebccb23549b566940d81dc163b7e5b3ff03ef689a08e8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 19:58:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 19:59:38 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 14 Feb 2024 19:59:39 GMT
ENV DOCKER_VERSION=24.0.9
# Wed, 14 Feb 2024 19:59:40 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.9.zip
# Wed, 14 Feb 2024 20:00:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 20:00:07 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Wed, 14 Feb 2024 20:00:08 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.windows-amd64.exe
# Wed, 14 Feb 2024 20:00:08 GMT
ENV DOCKER_BUILDX_SHA256=0ff0853a09960ff8f454d5db7253d5d935f5538856ea4985a276cbd1b28a96a5
# Wed, 14 Feb 2024 20:00:33 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 20:00:33 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.5
# Wed, 14 Feb 2024 20:00:34 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.24.5/docker-compose-windows-x86_64.exe
# Wed, 14 Feb 2024 20:00:34 GMT
ENV DOCKER_COMPOSE_SHA256=eb60363d21a5c85eff2d2e18a4ed94d84d5016be59471d77d520046fdd888aa9
# Wed, 14 Feb 2024 20:00:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8765950f7b3a43a58ddbb276100844d7bfa46522ab79851e54a70328e1418e61`  
		Last Modified: Wed, 14 Feb 2024 20:01:08 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f614cc1316387b426583a97f4cd4fb0a3cd9ffc202bee2b8c58e43752d88bcd1`  
		Last Modified: Wed, 14 Feb 2024 20:01:08 GMT  
		Size: 493.3 KB (493300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abbcf8f65684b031ad758fe412a89e4015162c7d118bb8e9bf5be7f82bc7ebfd`  
		Last Modified: Wed, 14 Feb 2024 20:01:08 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0fb775e79f3657c2ab273ceebb9ff032f0365865b507055d986b524e0bc7911`  
		Last Modified: Wed, 14 Feb 2024 20:01:07 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9089b6fa523acb7694fcff2eb482458d053a7daca5e1365201c97d789156a946`  
		Last Modified: Wed, 14 Feb 2024 20:01:09 GMT  
		Size: 17.5 MB (17539014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2477fa9594a9fe8eaaae4e8a5a60afd0a8a39bf2de9c2fdd221da5b297572a8f`  
		Last Modified: Wed, 14 Feb 2024 20:01:06 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce4d97edef3da413670e3e5f23d8805ba7446f2071d4a8f3bc00527516543859`  
		Last Modified: Wed, 14 Feb 2024 20:01:05 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7a3191e676af4210f45f8772b6a66b868d915843de2988c8a00401f9379c27`  
		Last Modified: Wed, 14 Feb 2024 20:01:05 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b9d238f7a45492f0ab07468170cfa4ce97a7055c908d696fcd454d2d74d9f98`  
		Last Modified: Wed, 14 Feb 2024 20:01:05 GMT  
		Size: 18.0 MB (18019890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a5059817fae4c396889412b41aa5e0c34fe20e7da55ed2d251997295732f972`  
		Last Modified: Wed, 14 Feb 2024 20:01:03 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1998cdb075674ada87ba2df65f67f3068476914a339c410d431ae8d5e1fcdd`  
		Last Modified: Wed, 14 Feb 2024 20:01:03 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ab851fe821136e8cba3acc05b78234a369e197fc2e3a81f15890f6febff337`  
		Last Modified: Wed, 14 Feb 2024 20:01:03 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80af44d08cb548cc260cb6f18822fd6c684c25051e51ad457d23f9e8873d5f08`  
		Last Modified: Wed, 14 Feb 2024 20:01:06 GMT  
		Size: 19.0 MB (19044219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
