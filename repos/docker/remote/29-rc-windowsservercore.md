## `docker:29-rc-windowsservercore`

```console
$ docker pull docker@sha256:3182b1a03063a343eec409cf1abbf06a875014b623289034c13025aa9b52405e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7462; amd64
	-	windows version 10.0.20348.4529; amd64

### `docker:29-rc-windowsservercore` - windows version 10.0.26100.7462; amd64

```console
$ docker pull docker@sha256:4a7e292dcb0ed08463c15bc5563868bb96e214ddaefb189e5f5f9dc6b31c2286
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3308429847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7463d249f577f72e60c8e45dee85e7bd892fda8ba5f39e255d57368db8cbca0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Dec 2025 21:49:56 GMT
RUN Install update 10.0.26100.7462
# Fri, 09 Jan 2026 19:08:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 09 Jan 2026 19:09:11 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 09 Jan 2026 19:09:11 GMT
ENV DOCKER_VERSION=29.2.0-rc.1
# Fri, 09 Jan 2026 19:09:12 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-29.2.0-rc.1.zip
# Fri, 09 Jan 2026 19:09:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 09 Jan 2026 19:09:28 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 09 Jan 2026 19:09:28 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Fri, 09 Jan 2026 19:09:28 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Fri, 09 Jan 2026 19:09:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 09 Jan 2026 19:09:39 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.1
# Fri, 09 Jan 2026 19:09:39 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-windows-x86_64.exe
# Fri, 09 Jan 2026 19:09:40 GMT
ENV DOCKER_COMPOSE_SHA256=2ae341f9152b4d90f561f84b8f2e263d5b60e1613c6841c804447819290c4119
# Fri, 09 Jan 2026 19:09:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Mon, 08 Dec 2025 10:02:12 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890b21ccebaeedf053c6c32fb4fe8d98ab2c60496b12e6b730ac67df9096fc5b`  
		Last Modified: Tue, 09 Dec 2025 19:44:14 GMT  
		Size: 1.0 GB (1037813290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc090e655787259d8d8b53033c472df1190bfa07e4a912a3dc1e45098db2eaf`  
		Last Modified: Fri, 09 Jan 2026 19:25:24 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3bc8333bb7c7995fd847166c4457031bc741b9e27d4105b849421076c8e0fa0`  
		Last Modified: Fri, 09 Jan 2026 19:25:24 GMT  
		Size: 404.8 KB (404833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9a84c52c8016b108a8bfe90f795d4c054feb27a59fcc11a71fa37f3a144412`  
		Last Modified: Fri, 09 Jan 2026 19:25:26 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a564960ff119edc7cf7a7d79e1d70dfd5b5d345c3cffb0f019adf53b21c1a3`  
		Last Modified: Fri, 09 Jan 2026 19:25:24 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f625ea2d0baaa8f2079919f599b13b92239b72c4ba3cac6a7dc483049da7f6c`  
		Last Modified: Fri, 09 Jan 2026 19:25:25 GMT  
		Size: 19.5 MB (19464931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3671746333720702f7002bb01ebcfb176862afc0610aa8fecb3f2e15b5074fa8`  
		Last Modified: Fri, 09 Jan 2026 19:25:24 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a395022fbd343bef93adeaf516c533d0935dd863016b75d48ba7cc4e73b2639e`  
		Last Modified: Fri, 09 Jan 2026 19:25:24 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e73ba847ba36674534e80bd940edd67921890d47fe5c2ac5421073651bfefd23`  
		Last Modified: Fri, 09 Jan 2026 19:25:24 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0287b7b0c561d9be803ce4095e2bd2681a8555974d606ad167ae2cf9ff03e37c`  
		Last Modified: Fri, 09 Jan 2026 19:25:26 GMT  
		Size: 24.0 MB (23951074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe0de9489ac95aab72bcbe9e09268ce138dd332ba3d1b65648c7e8be3151818`  
		Last Modified: Fri, 09 Jan 2026 19:25:24 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c160a1bcb1799ac4a6e7523de8a32dd0615751e45daa9c7c21c6ce815d8a31a`  
		Last Modified: Fri, 09 Jan 2026 19:25:24 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a80b730f9e36c04c83d17fb700efde234e26db98c93a560b40ed3250d46a14`  
		Last Modified: Fri, 09 Jan 2026 19:25:24 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa2ef7255c842156fd197325d7ff8313b19ea4c48093d64f7f5ad276e41bfe1`  
		Last Modified: Fri, 09 Jan 2026 19:25:25 GMT  
		Size: 11.5 MB (11476727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29-rc-windowsservercore` - windows version 10.0.20348.4529; amd64

```console
$ docker pull docker@sha256:bf01f9f97f266e7a208bbd1daeef57d8fb9930911c10a63c0c5040747ff0aacb
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1835145128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb8c4c795e8bdb9194bc9e220986682ddf2d8fdb114cca5b587f79cf52d4dd7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Fri, 09 Jan 2026 19:05:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 09 Jan 2026 19:06:25 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 09 Jan 2026 19:06:26 GMT
ENV DOCKER_VERSION=29.2.0-rc.1
# Fri, 09 Jan 2026 19:06:26 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-29.2.0-rc.1.zip
# Fri, 09 Jan 2026 19:06:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 09 Jan 2026 19:06:43 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 09 Jan 2026 19:06:44 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Fri, 09 Jan 2026 19:06:44 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Fri, 09 Jan 2026 19:07:01 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 09 Jan 2026 19:07:01 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.1
# Fri, 09 Jan 2026 19:07:02 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-windows-x86_64.exe
# Fri, 09 Jan 2026 19:07:03 GMT
ENV DOCKER_COMPOSE_SHA256=2ae341f9152b4d90f561f84b8f2e263d5b60e1613c6841c804447819290c4119
# Fri, 09 Jan 2026 19:07:18 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d54db5b2bfef493419c117d6a207c0d4fe091f6e1f37a0cdd6765be7939be21b`  
		Last Modified: Fri, 09 Jan 2026 19:16:04 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ea83bf76830d49f589fa7094dd440cb2c49fad152e40308bd90dc6a12d5a6e`  
		Last Modified: Fri, 09 Jan 2026 19:16:04 GMT  
		Size: 490.1 KB (490143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcab4edfaa222459dd4ee99b31be5e6eb33ec3f8a8a5c122c5969e9f222e55b3`  
		Last Modified: Fri, 09 Jan 2026 19:16:04 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0bd960e7f02f2fac99bfc20bcdcad84220cc0d42cc89dc673b462fbe611b6b`  
		Last Modified: Fri, 09 Jan 2026 19:16:08 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e18117f0d11670410ca2a976809ab0ff40c49227de5465215893b0a64d970a16`  
		Last Modified: Fri, 09 Jan 2026 19:16:06 GMT  
		Size: 19.4 MB (19416016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993a751607e4f0d7d4ef8da67c1ccc2e4f60364db55f9bfb00840c919b37c642`  
		Last Modified: Fri, 09 Jan 2026 19:16:04 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c6a796803445bd18c25f4425c1b6c07b88cbead4424cbd3e2658001879b6f3`  
		Last Modified: Fri, 09 Jan 2026 19:16:04 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e60988b474aa534ca59c6a88e9644edd56a70c7a0edbd7febacef4ba17f1976`  
		Last Modified: Fri, 09 Jan 2026 19:16:04 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52afa48d2ee8f1665a801dab604dc65f85fc455b308a868efee023f7e96154a8`  
		Last Modified: Fri, 09 Jan 2026 19:16:08 GMT  
		Size: 23.9 MB (23914483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f0afbabd9e9f4ee51602ba6f30d4d04e8dd2f2e98c8b48bda585a2dc9f71dc`  
		Last Modified: Fri, 09 Jan 2026 19:16:04 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca3d8598912cc82682f0f50bdd0ae34eba9435188866b59283b8f51dbb71438`  
		Last Modified: Fri, 09 Jan 2026 19:16:05 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055c66fb8f9cf35f6ae047ae0f1a77149785a1e83ec71944910f1043588816a9`  
		Last Modified: Fri, 09 Jan 2026 19:16:04 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:684d1594a3396e69305d34beea2baeb70ba1c0db409986a950ffe4140e469d78`  
		Last Modified: Fri, 09 Jan 2026 19:16:06 GMT  
		Size: 11.4 MB (11433295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
