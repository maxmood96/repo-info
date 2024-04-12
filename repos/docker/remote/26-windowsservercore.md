## `docker:26-windowsservercore`

```console
$ docker pull docker@sha256:ccad09c7edc338f903529c588e4e2fe51f5af0850ca291c476e9a2766bff5322
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

### `docker:26-windowsservercore` - windows version 10.0.20348.2402; amd64

```console
$ docker pull docker@sha256:96402f73dc71f569a983f84080cc8e2943046986a0e8b74e65a7293ec165416e
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2056365325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ba216ea3f1646f2d3d5e0587575cb91b43ad004713a6b55060b90b602c2fd0e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Fri, 12 Apr 2024 01:04:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 12 Apr 2024 01:05:02 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 12 Apr 2024 01:05:03 GMT
ENV DOCKER_VERSION=26.0.1
# Fri, 12 Apr 2024 01:05:04 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-26.0.1.zip
# Fri, 12 Apr 2024 01:05:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 12 Apr 2024 01:05:14 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Fri, 12 Apr 2024 01:05:14 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.windows-amd64.exe
# Fri, 12 Apr 2024 01:05:15 GMT
ENV DOCKER_BUILDX_SHA256=6b113e84cbc3cd645646aa82f00a7f7d3737cc10375b4341e0aca0de0c997c75
# Fri, 12 Apr 2024 01:05:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 12 Apr 2024 01:05:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.26.1
# Fri, 12 Apr 2024 01:05:24 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-windows-x86_64.exe
# Fri, 12 Apr 2024 01:05:24 GMT
ENV DOCKER_COMPOSE_SHA256=d8a386d375ef26a77be0bee97516b0287d93acafb3976806f42e2b76c6904125
# Fri, 12 Apr 2024 01:05:32 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318e3aedd05dc5ba503bf3e3f4b277765cff34f17a5416d6c81489e79ffd3f3c`  
		Last Modified: Fri, 12 Apr 2024 01:05:38 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dfb0aa985cd2b0a84d5382418315a5a71ed014a964c5c0a82d9f66e7caa25a`  
		Last Modified: Fri, 12 Apr 2024 01:05:38 GMT  
		Size: 490.8 KB (490812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:433cc0c6cb374efcc5b80c4b986fddebc5696ce76e6fe8ef567fab1d50bb6172`  
		Last Modified: Fri, 12 Apr 2024 01:05:37 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb97bf0318c13b429253dc43bf538c3a77a12f8cc41050c8609e4c9172a4e15`  
		Last Modified: Fri, 12 Apr 2024 01:05:37 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd43778fc657f82adfc6610533649fda9f0d399e80f7c870c84a31c69a8c1e9`  
		Last Modified: Fri, 12 Apr 2024 01:05:38 GMT  
		Size: 18.1 MB (18146952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b958c037159c3d2109bfe07e132968244462b555150d26378728f873b8133945`  
		Last Modified: Fri, 12 Apr 2024 01:05:36 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4530e493e1102da18625631cdb3cd870679f9f097a2d51c60d8aff23473125`  
		Last Modified: Fri, 12 Apr 2024 01:05:36 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d49176465084c23dcc0cc534665e312253bee622e457059228348b0fbb59c95`  
		Last Modified: Fri, 12 Apr 2024 01:05:36 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fbf7bc591ed6cf63699e50bfd767e97ee29c6f6ece83661f9bb1a9fdfee582b`  
		Last Modified: Fri, 12 Apr 2024 01:05:37 GMT  
		Size: 18.8 MB (18818534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66fce74cd0f3d14647169d12cb26caef6c8aa670706c8d60594064127f597f8`  
		Last Modified: Fri, 12 Apr 2024 01:05:34 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b70fbf7e46f3f34bd41e4966c9066467d9abc4232ba165962fda6805677cbf4`  
		Last Modified: Fri, 12 Apr 2024 01:05:34 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e551125f01dcac5fce8456b7c8bbe7ae6573b567e1cb0c30df7958e01c4cadfb`  
		Last Modified: Fri, 12 Apr 2024 01:05:34 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d670928ef93f4fed5217646c512cad98d938e8f6ad6948c257e04cd6ba97748d`  
		Last Modified: Fri, 12 Apr 2024 01:05:37 GMT  
		Size: 19.5 MB (19523784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:26-windowsservercore` - windows version 10.0.17763.5696; amd64

```console
$ docker pull docker@sha256:43be00b649c1cc747b91a889bba9db43fe9ffd96eb5318df19beae4ef8983e21
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2221315820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ec58d8e672f75753823be51df4d838f0510eecd7f6e0c8f256147b31ea3e09`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Fri, 12 Apr 2024 01:04:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 12 Apr 2024 01:05:23 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 12 Apr 2024 01:05:23 GMT
ENV DOCKER_VERSION=26.0.1
# Fri, 12 Apr 2024 01:05:24 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-26.0.1.zip
# Fri, 12 Apr 2024 01:05:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 12 Apr 2024 01:05:50 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Fri, 12 Apr 2024 01:05:51 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.windows-amd64.exe
# Fri, 12 Apr 2024 01:05:51 GMT
ENV DOCKER_BUILDX_SHA256=6b113e84cbc3cd645646aa82f00a7f7d3737cc10375b4341e0aca0de0c997c75
# Fri, 12 Apr 2024 01:06:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 12 Apr 2024 01:06:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.26.1
# Fri, 12 Apr 2024 01:06:17 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-windows-x86_64.exe
# Fri, 12 Apr 2024 01:06:17 GMT
ENV DOCKER_COMPOSE_SHA256=d8a386d375ef26a77be0bee97516b0287d93acafb3976806f42e2b76c6904125
# Fri, 12 Apr 2024 01:06:41 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9727f38969486e7a42a6a82d4b93c6f6ad1f1c35c40980855bccaee0702040`  
		Last Modified: Fri, 12 Apr 2024 01:06:51 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8174200c9a663a3882d61302a9065e8195c0b14913c10c56f603daa05f208cbf`  
		Last Modified: Fri, 12 Apr 2024 01:06:51 GMT  
		Size: 458.1 KB (458078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6734622511bbb0ec07956d9b04ebed81d22698d8c10b3f31066983033b652a46`  
		Last Modified: Fri, 12 Apr 2024 01:06:50 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8abe092c4b8f208b2d7c9c8c5530a6ee7957cee065309549a5a315efb96227`  
		Last Modified: Fri, 12 Apr 2024 01:06:50 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4973455dd59f78980b90fa194767374ef8ef2e6deb2e375ccf5c8a756200284`  
		Last Modified: Fri, 12 Apr 2024 01:06:52 GMT  
		Size: 18.1 MB (18122523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ba1f19a9e6a2c816b055846bc9e712d15b58dfa069261674b8e65bff23c404`  
		Last Modified: Fri, 12 Apr 2024 01:06:48 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb4f53948d1e103d37940be8ef0050075617f32a6fcbe3bff8dbd02d42967718`  
		Last Modified: Fri, 12 Apr 2024 01:06:47 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922d0ab46f9b8a41eb3d7d5523de84e8fff5905f14ad171e008795040f55814c`  
		Last Modified: Fri, 12 Apr 2024 01:06:48 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:335c8604c77198467816c6efa72694851307b20446ce881a4a80968518225862`  
		Last Modified: Fri, 12 Apr 2024 01:06:48 GMT  
		Size: 18.8 MB (18797974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06034b5a5e9f897b50b8f9775624cab90d782335128056a19ec03e8396f129f1`  
		Last Modified: Fri, 12 Apr 2024 01:06:45 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e11c468704bc88a7484380e27084d3eb3bd0708135b7d5827340de652aea527c`  
		Last Modified: Fri, 12 Apr 2024 01:06:45 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a25f0df11fed5ffda2b8389e91ffe767269df670f103c13987daf3392cdf844`  
		Last Modified: Fri, 12 Apr 2024 01:06:45 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c5a8e3c5d093399869ece1415285a92c32a627d1542db65691688b6767dc9d`  
		Last Modified: Fri, 12 Apr 2024 01:06:48 GMT  
		Size: 19.5 MB (19497596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
