## `docker:28-rc-windowsservercore`

```console
$ docker pull docker@sha256:b9c20646c54e383ea8d16e9e479a44218dd09052e20983e41d809764be7aba3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4349; amd64
	-	windows version 10.0.20348.3807; amd64

### `docker:28-rc-windowsservercore` - windows version 10.0.26100.4349; amd64

```console
$ docker pull docker@sha256:a60deabb16c716e73f7f320b81f86c51702ef87d997b76678b050be07cc361df
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3542401823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4afcd33a7fb827b0e7f8260798f292263b6d1f80874403a9e660bda5002a7940`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Fri, 20 Jun 2025 19:13:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 20 Jun 2025 19:13:53 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 20 Jun 2025 19:13:54 GMT
ENV DOCKER_VERSION=28.3.0-rc.1
# Fri, 20 Jun 2025 19:13:55 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.3.0-rc.1.zip
# Fri, 20 Jun 2025 19:14:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 20 Jun 2025 19:14:07 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Fri, 20 Jun 2025 19:14:08 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Fri, 20 Jun 2025 19:14:09 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Fri, 20 Jun 2025 19:14:19 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 20 Jun 2025 19:14:20 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.2
# Fri, 20 Jun 2025 19:14:21 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-windows-x86_64.exe
# Fri, 20 Jun 2025 19:14:22 GMT
ENV DOCKER_COMPOSE_SHA256=f52bba6d8031da7e01c5bcf621dadea0afa41a317be09f2946701e15e899f8a4
# Fri, 20 Jun 2025 19:14:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b61d8f1bb5129502a06cea04657715aa68d500a1dc0ddcf37003afcd263c28`  
		Last Modified: Tue, 10 Jun 2025 22:09:36 GMT  
		Size: 1.3 GB (1260866861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5267f6ce2f4e2fbb532ab1c876611de270e8bcb294bb8cf8b0848a90cedd9114`  
		Last Modified: Fri, 20 Jun 2025 19:17:53 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf7f639c7392e25bcb40208d23f45f6b14f4798cac4e75295ca7cc71a0b0890`  
		Last Modified: Fri, 20 Jun 2025 19:17:53 GMT  
		Size: 408.9 KB (408943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea786ca379792ba41d1d4babb0ca70ddc0af7ed80270d2b9c304ce59e9cb682`  
		Last Modified: Fri, 20 Jun 2025 19:17:54 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d43983e48350c2fa9dfc337e99c1ab6c9b3c3e691dbda5973d4085a054c8a3aa`  
		Last Modified: Fri, 20 Jun 2025 19:17:53 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96531e224fe4bb3d3e9f6a7591738aa9b78cb0c50901e0681199cd0904559a9a`  
		Last Modified: Fri, 20 Jun 2025 19:17:55 GMT  
		Size: 20.9 MB (20872319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d29985f0ae38efa74d773f47d79e21c47a9d33883fe9ec391ececf73b365f14b`  
		Last Modified: Fri, 20 Jun 2025 19:17:54 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4162ea217b469678d5f678a7177c0483746d11957113c918544054033e26bb2c`  
		Last Modified: Fri, 20 Jun 2025 19:17:54 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5d8fc8ef47f50dadeda363de26a2db96875403ef1e6a5c09519cdf2eb849a6`  
		Last Modified: Fri, 20 Jun 2025 19:17:55 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:563654ae8716dd2ea80c17e5a29e5062bfd29cbe2d1de704aa299eda639c5f74`  
		Last Modified: Fri, 20 Jun 2025 19:17:56 GMT  
		Size: 22.7 MB (22697997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e02260c196277d6855a6ccdda1d57646f14e7c55643a1892947827a9187f93`  
		Last Modified: Fri, 20 Jun 2025 19:17:55 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd2fd3fd88271869083c2978c3ef3caaf0ecdef5f75f2cdde1773a474b4692e`  
		Last Modified: Fri, 20 Jun 2025 19:17:55 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6469916da743eddf2d93e810e777dd5f2a95de2c5caed8e72c8df281ff4bf3d4`  
		Last Modified: Fri, 20 Jun 2025 19:17:55 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b83db248ab8b76981cdabecafb456e7f6f9f525217010d912fd373cf622bdb2b`  
		Last Modified: Fri, 20 Jun 2025 19:17:59 GMT  
		Size: 22.2 MB (22236692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-rc-windowsservercore` - windows version 10.0.20348.3807; amd64

```console
$ docker pull docker@sha256:8a8db850894c7fdb377f08607cc1de35c733ddb2f969a6490399db9920a7764e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346178897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8927de3f62ca7e39aef3ee520929d55cc0a71e6999ed2516cc0746f7f2e6da76`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Fri, 20 Jun 2025 19:08:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 20 Jun 2025 19:09:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 20 Jun 2025 19:09:33 GMT
ENV DOCKER_VERSION=28.3.0-rc.1
# Fri, 20 Jun 2025 19:09:34 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.3.0-rc.1.zip
# Fri, 20 Jun 2025 19:09:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 20 Jun 2025 19:09:56 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Fri, 20 Jun 2025 19:09:56 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Fri, 20 Jun 2025 19:09:57 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Fri, 20 Jun 2025 19:10:06 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 20 Jun 2025 19:10:06 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.2
# Fri, 20 Jun 2025 19:10:07 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-windows-x86_64.exe
# Fri, 20 Jun 2025 19:10:08 GMT
ENV DOCKER_COMPOSE_SHA256=f52bba6d8031da7e01c5bcf621dadea0afa41a317be09f2946701e15e899f8a4
# Fri, 20 Jun 2025 19:10:19 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec9df081f850e610bfde9c9d6925682c9cea53cbad71eb5971c794fbfc2a85b`  
		Last Modified: Fri, 20 Jun 2025 19:10:36 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc97827a3294177be3160890658319a3e3199628670954d1440cfcbc34ecac9`  
		Last Modified: Fri, 20 Jun 2025 19:10:36 GMT  
		Size: 357.1 KB (357149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2fc980f3c59381f6d009eab513fd005b7d068c168efa6069a6846055a748c1a`  
		Last Modified: Fri, 20 Jun 2025 19:10:35 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c9d7094984969e02304d7f7d61b7f5996c959e1fae94c5cf106bbaa1926a45`  
		Last Modified: Fri, 20 Jun 2025 19:10:35 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da5e42afe6acfa8b0f0ceeaae20c2f5a383794aab6a31f069f6ed2788e919b6`  
		Last Modified: Fri, 20 Jun 2025 19:10:39 GMT  
		Size: 20.8 MB (20789351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499eb92ce8822e4f87c6bb6d12386f3320cca6a9db008bcc8f78cb62a5ba5a74`  
		Last Modified: Fri, 20 Jun 2025 19:10:36 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707ac5ee4bf2d0b8186fa41a3d5e51059de8071a4838bb786b6d936989b4fb7b`  
		Last Modified: Fri, 20 Jun 2025 19:10:36 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb14dd03f5574580f3ce904d24918f6a97bd1b0a985a3eb3b4d78258a811645`  
		Last Modified: Fri, 20 Jun 2025 19:10:36 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c365da66f44c5960d9108e19e434d06fb39a04a28445f7131ad391d0e392f530`  
		Last Modified: Fri, 20 Jun 2025 19:10:39 GMT  
		Size: 22.6 MB (22618475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca048996dbcdf8da087a200c4e3cae5c58a3299d70b9754ac5b4b73a1d217b2b`  
		Last Modified: Fri, 20 Jun 2025 19:10:36 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21da89037871bdf6b4c5cbf747ba14dace90939149e11e7fe5ac705f3f5f49dc`  
		Last Modified: Fri, 20 Jun 2025 19:10:37 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe30cec6727774569881a684e9f256b10ac01d7fe34c37f8d208873a4d89f7d`  
		Last Modified: Fri, 20 Jun 2025 19:10:38 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e86b0a2e42b396fa4f565435ae62b765240596fea9aae3773c635c13bd5b1461`  
		Last Modified: Fri, 20 Jun 2025 19:10:40 GMT  
		Size: 22.2 MB (22150780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
