## `docker:26-windowsservercore`

```console
$ docker pull docker@sha256:1e7e1f7c635b9a5fda6d72b38c62b9f820490486ff9d60fbdfc1ab4d13b10bab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2582; amd64
	-	windows version 10.0.17763.6054; amd64

### `docker:26-windowsservercore` - windows version 10.0.20348.2582; amd64

```console
$ docker pull docker@sha256:e196433b46a4e70caea0a8f677985ffa2b17fa4d06da78d3b5cba3fb29723d1d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2198130713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83f34d9b19358fc31c724bf2186f4fee8302d26709726fe883dd6ec502eb39ec`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 03 Jul 2024 10:07:02 GMT
RUN Install update 10.0.20348.2582
# Fri, 19 Jul 2024 17:58:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 19 Jul 2024 17:58:37 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 19 Jul 2024 17:58:38 GMT
ENV DOCKER_VERSION=26.1.4
# Fri, 19 Jul 2024 17:58:39 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-26.1.4.zip
# Fri, 19 Jul 2024 17:58:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 19 Jul 2024 17:58:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.1
# Fri, 19 Jul 2024 17:58:51 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.windows-amd64.exe
# Fri, 19 Jul 2024 17:58:51 GMT
ENV DOCKER_BUILDX_SHA256=34b8bd302364e9df99ebcd86658eae6ade175baf8baf6e74123ae04fcb2675c3
# Fri, 19 Jul 2024 17:59:01 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 19 Jul 2024 17:59:02 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.0
# Fri, 19 Jul 2024 17:59:03 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-windows-x86_64.exe
# Fri, 19 Jul 2024 17:59:04 GMT
ENV DOCKER_COMPOSE_SHA256=3dc98cacf0e0a05d8a714cc729827c062ff7ec13ffcd626e7b3767b362ce9b65
# Fri, 19 Jul 2024 17:59:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0206d135152eb909f50159d6ca348a5aead199afacbafc000b770c1b0720f6`  
		Last Modified: Tue, 09 Jul 2024 18:30:31 GMT  
		Size: 751.0 MB (751001543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8501234437fa053506c656c471ce3db7d037e9981684aac7d1e7fcc082b03354`  
		Last Modified: Fri, 19 Jul 2024 17:59:24 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f218f0fad3c95e4bee7898d8ba619fca43ac0ea94ada0305993377c96863b9`  
		Last Modified: Fri, 19 Jul 2024 17:59:24 GMT  
		Size: 346.6 KB (346624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4566179e12bce0072de1b5fb5ebca0cb266732eb4458ac34b7445d7ee25b783`  
		Last Modified: Fri, 19 Jul 2024 17:59:23 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d412f10a0cf365b9c8036b038a9c77d1eb3f85ac90f4fdd2da5a0426f39c51cc`  
		Last Modified: Fri, 19 Jul 2024 17:59:23 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb90ebaf4dbdc16ea25f8008230c04e0dce133410b65e27904b75796d5b4e4c4`  
		Last Modified: Fri, 19 Jul 2024 17:59:25 GMT  
		Size: 19.2 MB (19241196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a227e82f85ceb071f5bd18c38493a966fa675cc7a97e94d47a6d02544794820`  
		Last Modified: Fri, 19 Jul 2024 17:59:21 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8835ccc3b975098a9d5700b731b1645fc20e2b66d6dbec9182c4ac625f5d849`  
		Last Modified: Fri, 19 Jul 2024 17:59:21 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356f74ca7d88280884166b62940429b323ea643025179b2fa655ec3452c2e678`  
		Last Modified: Fri, 19 Jul 2024 17:59:21 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6882175de555d9ce17ea4e7f06bb3538c7f7c121f29b16eadff91bfae6a94247`  
		Last Modified: Fri, 19 Jul 2024 17:59:22 GMT  
		Size: 19.2 MB (19248199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bd49451371f2b38beccf455eb1131bfe7557adb746b710dd7e3deef80ce605`  
		Last Modified: Fri, 19 Jul 2024 17:59:19 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a06966265a612d5f0576249aea58141a17fcc01d81996bfb1fa6256d9b9a732c`  
		Last Modified: Fri, 19 Jul 2024 17:59:19 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8f579fb4e6802441daf771ca27333769cbef5c466d71e353569c539a4377f8`  
		Last Modified: Fri, 19 Jul 2024 17:59:19 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed6fbd3e5cf07c7849c7261fb90035d5596d62ca26e8762a271b52f7a0e5e70`  
		Last Modified: Fri, 19 Jul 2024 17:59:22 GMT  
		Size: 19.7 MB (19682638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:26-windowsservercore` - windows version 10.0.17763.6054; amd64

```console
$ docker pull docker@sha256:4e5477b268c844c17ee4bb0f89b10b5dd97742fb861d46acf96f817c49f576f8
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2297154023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089180c73758c73557b3821124d6a18333caba6eee48f39fdd03d8dd9d6aeb13`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Fri, 19 Jul 2024 17:58:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 19 Jul 2024 18:00:08 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 19 Jul 2024 18:00:08 GMT
ENV DOCKER_VERSION=26.1.4
# Fri, 19 Jul 2024 18:00:09 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-26.1.4.zip
# Fri, 19 Jul 2024 18:00:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 19 Jul 2024 18:00:45 GMT
ENV DOCKER_BUILDX_VERSION=0.16.1
# Fri, 19 Jul 2024 18:00:46 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.windows-amd64.exe
# Fri, 19 Jul 2024 18:00:46 GMT
ENV DOCKER_BUILDX_SHA256=34b8bd302364e9df99ebcd86658eae6ade175baf8baf6e74123ae04fcb2675c3
# Fri, 19 Jul 2024 18:01:13 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 19 Jul 2024 18:01:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.0
# Fri, 19 Jul 2024 18:01:14 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-windows-x86_64.exe
# Fri, 19 Jul 2024 18:01:15 GMT
ENV DOCKER_COMPOSE_SHA256=3dc98cacf0e0a05d8a714cc729827c062ff7ec13ffcd626e7b3767b362ce9b65
# Fri, 19 Jul 2024 18:01:36 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f98e7fe87492b83d7775a348ae0c94412b638ab5bba1a80b03c3a547708acd`  
		Last Modified: Tue, 09 Jul 2024 17:23:28 GMT  
		Size: 587.8 MB (587809033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c0d8d018dfc0da07c5af317ca7901dba0f321dadc23b78d2f6a5217fc7348a7`  
		Last Modified: Fri, 19 Jul 2024 18:01:42 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5175baae9f9101fbf9fa54456c9309e48f2bad27f0c78b881bfa556d8b4956dc`  
		Last Modified: Fri, 19 Jul 2024 18:01:42 GMT  
		Size: 497.7 KB (497741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8528da61a4d55fcf0a1ff897738102a53d160efab06ff7b1b6d50ce1a2d9d648`  
		Last Modified: Fri, 19 Jul 2024 18:01:41 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:385bef8909b6662d8ec39a4231faa2a42769ce51f92e94c1fb7ecdd2107322c5`  
		Last Modified: Fri, 19 Jul 2024 18:01:41 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb9d915f00ab16b2a6f4f0d84b40303fe64f4622cafba61229156054071d48b`  
		Last Modified: Fri, 19 Jul 2024 18:01:42 GMT  
		Size: 19.3 MB (19265870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fed5463623baafa3d86ed5a750f5a4155b053997c7263285c301aff83a6357a`  
		Last Modified: Fri, 19 Jul 2024 18:01:40 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48cf0d0077d1e296417364c96fd77044ce67f7dd023c791bbeff38ccb158f8f2`  
		Last Modified: Fri, 19 Jul 2024 18:01:40 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eea35a19f216e104d710d27a11afb2ed483fb6bc41ab5a36c5b53537caf1cb6`  
		Last Modified: Fri, 19 Jul 2024 18:01:40 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5da1e7261bd45aae4f612c13afeb6464630daab0bc5123deda855ee24e1f6fd`  
		Last Modified: Fri, 19 Jul 2024 18:01:41 GMT  
		Size: 19.3 MB (19260742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0e3065f066734578f74b5be9c909a5311f866bdcb5dfb726dd398be0d034ca`  
		Last Modified: Fri, 19 Jul 2024 18:01:39 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d955d0d2fabaa7a553bcecc1ca286f0b288d7ec24d631a5fa5e99a27a4c28214`  
		Last Modified: Fri, 19 Jul 2024 18:01:39 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eddad6d9ce39fa599dee13b83fc746b91f23be3225746b698d8dacaf03dcb5db`  
		Last Modified: Fri, 19 Jul 2024 18:01:39 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2a691a0b084d26fc9599fb2276a51f8a4a1e26d21514bf10b2070a6295789a0`  
		Last Modified: Fri, 19 Jul 2024 18:01:41 GMT  
		Size: 19.7 MB (19688589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
