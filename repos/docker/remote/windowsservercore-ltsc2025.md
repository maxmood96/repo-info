## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:4c2d528f844dac99062dc79967dd48348177d2db9ea7c66e86dd29010b571301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.3476; amd64

```console
$ docker pull docker@sha256:81996f945dd6afd17a2f454f627cc9301a6d669d579eee88075c6866592b7eac
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2974045827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90411219e91a7a2282d6bafa1fa9f88374b9cc7fc5023a00346072afe20d252f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Tue, 18 Mar 2025 17:48:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Mar 2025 17:48:58 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 18 Mar 2025 17:48:59 GMT
ENV DOCKER_VERSION=28.0.1
# Tue, 18 Mar 2025 17:49:00 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Tue, 18 Mar 2025 17:49:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:49:13 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Tue, 18 Mar 2025 17:49:14 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.windows-amd64.exe
# Tue, 18 Mar 2025 17:49:15 GMT
ENV DOCKER_BUILDX_SHA256=f9ccbfaf42c68e61833f7031e0bdb4b71931cf5ef54d132b39f9faccda02ec7c
# Tue, 18 Mar 2025 17:49:24 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:49:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 18 Mar 2025 17:49:26 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 18 Mar 2025 17:49:28 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 18 Mar 2025 17:49:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d0cd020c6471f62220ad8ed2ae2b3772b806f467cb0f11bc4308b9f2d0d26a`  
		Last Modified: Tue, 18 Mar 2025 17:49:48 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5cf4955d1aad1f83447efbdbcf08c9bd7423c84e7c6ac5bc6a5625140c991e0`  
		Last Modified: Tue, 18 Mar 2025 17:49:48 GMT  
		Size: 400.2 KB (400166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90786f2c40deca413eed711fbbeb0abe197cababcf2e8b187fda5466bf3f9e14`  
		Last Modified: Tue, 18 Mar 2025 17:49:46 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3684238c758b95728bef5bbcf3815bce65fcb21040c3ec400e17b2e4b2975988`  
		Last Modified: Tue, 18 Mar 2025 17:49:46 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7eac4b401484a405d9d595d4ab1ab2e2fa8f1dc11da64e453e0d575e376817`  
		Last Modified: Tue, 18 Mar 2025 17:49:48 GMT  
		Size: 19.9 MB (19862606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c68379e676f653db1ef6496f93f7f34f94e2e6adc3897f119f4d93a2092313f0`  
		Last Modified: Tue, 18 Mar 2025 17:49:44 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df3c74807df3393363f62fd1b3dec83fe3a43f74559b92815cd5cbd580fbe6f`  
		Last Modified: Tue, 18 Mar 2025 17:49:44 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5332d7c8bb3be4f3f08437752f48d8a66371aad10f5328510eeaa532db9383ba`  
		Last Modified: Tue, 18 Mar 2025 17:49:44 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ebe5ad6be9c69cb89a53b45d42605e0654403950049245df6ed82d6552beb2`  
		Last Modified: Tue, 18 Mar 2025 17:49:45 GMT  
		Size: 22.8 MB (22789480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7945eb3de2b551bb141ecdcf88f5508c82ba67aa0f4910a08e9833a279946fde`  
		Last Modified: Tue, 18 Mar 2025 17:49:42 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32749cc1ae150ad64cd11025c4de890ad6f72d84ccb8714200245b156bf136d1`  
		Last Modified: Tue, 18 Mar 2025 17:49:42 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598bafa4dd3f7f04b9861f17341c80a693efdf2c84a11ab664533e4b3c2334b2`  
		Last Modified: Tue, 18 Mar 2025 17:49:42 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b541b6491c1b4a89b6665a2775f4c706b4f2d8349747d04f83ac14f4ac23ca`  
		Last Modified: Tue, 18 Mar 2025 17:49:45 GMT  
		Size: 22.3 MB (22334051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
