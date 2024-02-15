## `docker:24-windowsservercore`

```console
$ docker pull docker@sha256:73d8397ff4ec80ef49f47c904a4762706f7171c234dd820da1e2d3f1adbb4259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2322; amd64
	-	windows version 10.0.17763.5458; amd64

### `docker:24-windowsservercore` - windows version 10.0.20348.2322; amd64

```console
$ docker pull docker@sha256:d1e8ee6f4611b4c428f1280550f6f4c8c27f78475a4987da9044a3b8b5cb9d20
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1965776739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0070c08fe8a7612bec7d6019b93395231f1c10a7182109865a7ecd99e138755`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Wed, 14 Feb 2024 20:00:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 20:01:07 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 14 Feb 2024 20:01:08 GMT
ENV DOCKER_VERSION=24.0.9
# Wed, 14 Feb 2024 20:01:08 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.9.zip
# Wed, 14 Feb 2024 20:01:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 20:01:19 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Wed, 14 Feb 2024 20:01:19 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.windows-amd64.exe
# Wed, 14 Feb 2024 20:01:20 GMT
ENV DOCKER_BUILDX_SHA256=0ff0853a09960ff8f454d5db7253d5d935f5538856ea4985a276cbd1b28a96a5
# Wed, 14 Feb 2024 20:01:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 20:01:28 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.5
# Wed, 14 Feb 2024 20:01:29 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.24.5/docker-compose-windows-x86_64.exe
# Wed, 14 Feb 2024 20:01:30 GMT
ENV DOCKER_COMPOSE_SHA256=eb60363d21a5c85eff2d2e18a4ed94d84d5016be59471d77d520046fdd888aa9
# Wed, 14 Feb 2024 20:01:37 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91d26084b3c455dcae070b284e7f9bad53a6ed7091d60b071650d24518444ed2`  
		Last Modified: Wed, 14 Feb 2024 20:01:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0d21efef9b3365eb10a350777ab9b92743cc1a3e04bfdf293873a598f0e7bb`  
		Last Modified: Wed, 14 Feb 2024 20:01:44 GMT  
		Size: 502.3 KB (502289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a0e6d8f57fad1a2aa958b8ca4017b6113f604900057dc30879016108379eda`  
		Last Modified: Wed, 14 Feb 2024 20:01:42 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71319fc52978d9c257d8e7185ce3740f163fbac992090bbc562480ab2aca734`  
		Last Modified: Wed, 14 Feb 2024 20:01:43 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1542cf396af0a9bdb8f70783c639f3159349d921d2ef424996244848b34067`  
		Last Modified: Wed, 14 Feb 2024 20:01:44 GMT  
		Size: 17.5 MB (17540331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51bc816455f9699583e1d8fe722a4f813b7afa101f9e40e7d73115976cab200a`  
		Last Modified: Wed, 14 Feb 2024 20:01:41 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca06f0ba2510a27cd0c2df817e899604738c7298c108139724002a174135b4b`  
		Last Modified: Wed, 14 Feb 2024 20:01:41 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceddac84a221ff6a1dda9fb497c7a3c873de5630e1e38621e85b26d1b769748a`  
		Last Modified: Wed, 14 Feb 2024 20:01:41 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5fcaa10038e1d587acf40ba853cace33e1989ca299e9771a1e7a43a680c34d`  
		Last Modified: Wed, 14 Feb 2024 20:01:43 GMT  
		Size: 18.0 MB (18018611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4c9e7a868abc0abf82791b8792942b6d22751ca8fa60cdaec2ec571ae5f3b9`  
		Last Modified: Wed, 14 Feb 2024 20:01:40 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf45220ecc7f9e25cd487d1c2e10bb0f2eb0660cd6dbcfc820beade8bd271e0`  
		Last Modified: Wed, 14 Feb 2024 20:01:40 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4343c66f59acb0bfffb3e7e77d3fe336b2cbc6213501e813ad1118ec30abcfb3`  
		Last Modified: Wed, 14 Feb 2024 20:01:40 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bdf2d00ba9c8ffd0274cb94d438d0025edc6a0c1a94bc873a15fa5397d6ef00`  
		Last Modified: Wed, 14 Feb 2024 20:01:42 GMT  
		Size: 19.0 MB (19049686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:24-windowsservercore` - windows version 10.0.17763.5458; amd64

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
