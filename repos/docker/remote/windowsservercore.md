## `docker:windowsservercore`

```console
$ docker pull docker@sha256:acabe8f5ea14f85118986fc67f6b22e50e16da1755d2fe56ae8a00b11b935898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `docker:windowsservercore` - windows version 10.0.20348.2227; amd64

```console
$ docker pull docker@sha256:250f63457c2cbdb17dd8c6d44c846bd4025d0c6bbe452521dd06d3fb413b91dc
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1955319981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c54004e755259e9347fc2f8bd5cc6e10356a53852fc617dd51d175008f44fd6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Thu, 18 Jan 2024 23:03:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 18 Jan 2024 23:04:56 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 18 Jan 2024 23:04:56 GMT
ENV DOCKER_VERSION=24.0.7
# Thu, 18 Jan 2024 23:04:57 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.7.zip
# Thu, 18 Jan 2024 23:05:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 18 Jan 2024 23:05:18 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Thu, 18 Jan 2024 23:05:19 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.windows-amd64.exe
# Thu, 18 Jan 2024 23:05:20 GMT
ENV DOCKER_BUILDX_SHA256=0ff0853a09960ff8f454d5db7253d5d935f5538856ea4985a276cbd1b28a96a5
# Thu, 18 Jan 2024 23:05:32 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 18 Jan 2024 23:05:32 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.1
# Thu, 18 Jan 2024 23:05:33 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-windows-x86_64.exe
# Thu, 18 Jan 2024 23:05:34 GMT
ENV DOCKER_COMPOSE_SHA256=6c94193c282d5fba71563c617fe8ddf8dce9355fb1d0ae93609221c590d06fcb
# Thu, 18 Jan 2024 23:05:45 GMT
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
	-	`sha256:87c5a34f0c4d490d6ffa59426951c0a4ddb32e21711f263a59706e55ced18470`  
		Last Modified: Thu, 18 Jan 2024 23:05:55 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5eafa83929cac4ed5ee9abb9950e342585f93533221884dd5c9ab16510f3f81`  
		Last Modified: Thu, 18 Jan 2024 23:05:54 GMT  
		Size: 500.2 KB (500178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46e9a66b019dc60c70ea97c2352be7afc7c5f47aa466d209ba31661b43905b4`  
		Last Modified: Thu, 18 Jan 2024 23:05:53 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9bdda7b37c1e254d1f66bbe0506ba65cdf80ad22a3d254256b32c086c7297e0`  
		Last Modified: Thu, 18 Jan 2024 23:05:53 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9966e7797df3b9665486c85443bb20ea51645208cba880c135c4694787feb18f`  
		Last Modified: Thu, 18 Jan 2024 23:05:55 GMT  
		Size: 17.5 MB (17534088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67ab1ac3c7984d09f76e29a26f8e02311962d2835bcc2822d553f8c372012314`  
		Last Modified: Thu, 18 Jan 2024 23:05:51 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4cf8bf2cf4c6c0c64e9d5a06e0d3f11984fed1a572022e3ce2af656d6728bee`  
		Last Modified: Thu, 18 Jan 2024 23:05:51 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a5ba0442f8799227b40febf1590857f02a6dd752415140ce6d5d5b731e1b3a7`  
		Last Modified: Thu, 18 Jan 2024 23:05:51 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139e067d2c115af4ff60f396b04475b4d8be5a99ca06c703d59be68f3f069ca2`  
		Last Modified: Thu, 18 Jan 2024 23:05:52 GMT  
		Size: 18.0 MB (18025751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d0b41cdbbb1e1b83d2ea5340ed76eb75774684c18834006ae69ee6f1b1d16c`  
		Last Modified: Thu, 18 Jan 2024 23:05:49 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d040e7b1a17e55d32f6f49a0c1d64f989faf7b5341bd27fd5429e771b0607d`  
		Last Modified: Thu, 18 Jan 2024 23:05:49 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0c59d6bee178e95b5a4c8ca20a1a3513d42321f7f6cc063655ffed6755bf9f`  
		Last Modified: Thu, 18 Jan 2024 23:05:49 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f4dfdfcfd1c72b473e92dd20c882318ac2fe91cd349afbf280d9d660b04fbf`  
		Last Modified: Thu, 18 Jan 2024 23:05:52 GMT  
		Size: 19.0 MB (19035689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.5329; amd64

```console
$ docker pull docker@sha256:5650c4cb2e6da910ac23b337134327a31f07e1181beb8878666bd95b02ed2a03
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2124816394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9a82f082619251e6003b546c5e63b71b59d10443505c9af4cadcb8924dc643`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 18 Jan 2024 23:04:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 18 Jan 2024 23:07:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 18 Jan 2024 23:07:15 GMT
ENV DOCKER_VERSION=24.0.7
# Thu, 18 Jan 2024 23:07:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.7.zip
# Thu, 18 Jan 2024 23:07:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 18 Jan 2024 23:07:53 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Thu, 18 Jan 2024 23:07:54 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.windows-amd64.exe
# Thu, 18 Jan 2024 23:07:54 GMT
ENV DOCKER_BUILDX_SHA256=0ff0853a09960ff8f454d5db7253d5d935f5538856ea4985a276cbd1b28a96a5
# Thu, 18 Jan 2024 23:08:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 18 Jan 2024 23:08:20 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.1
# Thu, 18 Jan 2024 23:08:21 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-windows-x86_64.exe
# Thu, 18 Jan 2024 23:08:22 GMT
ENV DOCKER_COMPOSE_SHA256=6c94193c282d5fba71563c617fe8ddf8dce9355fb1d0ae93609221c590d06fcb
# Thu, 18 Jan 2024 23:08:46 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72e935298f8980c8c04e967f4d9bddf598445377b19c43f2c58e13d6660a5f00`  
		Last Modified: Thu, 18 Jan 2024 23:08:52 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed7bd16558f3a9e0959c7bbc53d5139cb635cdff7c81fddaa6876796ae19b80`  
		Last Modified: Thu, 18 Jan 2024 23:08:52 GMT  
		Size: 495.5 KB (495468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c93575ab21ec0af0884e3406661644829b36c240a3b9514ba815f12c0aa3e9`  
		Last Modified: Thu, 18 Jan 2024 23:08:51 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91100e4a19a3a9152bcd40d8c02ac3ad445d146c5e4521396c8206d5e94b1448`  
		Last Modified: Thu, 18 Jan 2024 23:08:51 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:645c9844826d13da243c96996e14473f445d28ec22cf1aa3d0d182d4fdc23d49`  
		Last Modified: Thu, 18 Jan 2024 23:08:52 GMT  
		Size: 17.5 MB (17538398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9238e10f1a8aab6901be04b2306aa50e06c960da33fa290d3eea84d19bda6779`  
		Last Modified: Thu, 18 Jan 2024 23:08:50 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89f77c0d968fee19826050fc17d734971538d88d26468a00d919c80c85139dd`  
		Last Modified: Thu, 18 Jan 2024 23:08:50 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f896434c11afa7393532eeb9b8cff3c15ef274984fd0e734bc563eb2cdbacf`  
		Last Modified: Thu, 18 Jan 2024 23:08:50 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d4b59b8ce258884cfc0b36d131d4e081933d4d6a5e898f28d225b1f524a967`  
		Last Modified: Thu, 18 Jan 2024 23:08:51 GMT  
		Size: 18.0 MB (18021206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e8abd303e0c0a46e0804822f00016ab56057238750ceb158216e82b52283199`  
		Last Modified: Thu, 18 Jan 2024 23:08:49 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0850ebdd4699fe1926d6f4be14ac85e26c34f8f68182ddeb5e42e30ad4aa4074`  
		Last Modified: Thu, 18 Jan 2024 23:08:49 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acba53531bbf0b6e6e870aba5eb012bcb5f69317832e919909ff7bf729740158`  
		Last Modified: Thu, 18 Jan 2024 23:08:49 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a81b4a1eb33d96b5d833bc9667565a9f3656ea3215b27bf1bfbf5cde29529e55`  
		Last Modified: Thu, 18 Jan 2024 23:08:51 GMT  
		Size: 19.0 MB (19027123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
