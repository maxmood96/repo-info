## `docker:windowsservercore`

```console
$ docker pull docker@sha256:8383ed532574f25a2d0df048a23f8f0b00b2f31cce8c9e17d1cb82c0a2e6da63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

### `docker:windowsservercore` - windows version 10.0.20348.2402; amd64

```console
$ docker pull docker@sha256:b0dd1feb52cc9f4e0481f90f1a104351f79b9d53e2606b644f2a334db3c7a59d
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2057588320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e21330b293363b19ff39ade57f97263b47a404da266208cb229cf1c9cb122c33`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 23 Apr 2024 23:50:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 23 Apr 2024 23:51:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 23 Apr 2024 23:51:42 GMT
ENV DOCKER_VERSION=26.1.0
# Tue, 23 Apr 2024 23:51:43 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-26.1.0.zip
# Tue, 23 Apr 2024 23:52:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 23 Apr 2024 23:52:06 GMT
ENV DOCKER_BUILDX_VERSION=0.14.0
# Tue, 23 Apr 2024 23:52:06 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.windows-amd64.exe
# Tue, 23 Apr 2024 23:52:07 GMT
ENV DOCKER_BUILDX_SHA256=d43f5008431fb4ffd438d14ea686ed0f9c7ef101f2dfd1f84a5670979aeb39a8
# Tue, 23 Apr 2024 23:52:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 23 Apr 2024 23:52:29 GMT
ENV DOCKER_COMPOSE_VERSION=2.26.1
# Tue, 23 Apr 2024 23:52:29 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-windows-x86_64.exe
# Tue, 23 Apr 2024 23:52:30 GMT
ENV DOCKER_COMPOSE_SHA256=d8a386d375ef26a77be0bee97516b0287d93acafb3976806f42e2b76c6904125
# Tue, 23 Apr 2024 23:52:52 GMT
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
	-	`sha256:7ea3b6e702ce4e81f143337df34eddaded968714e121574391d79056ef2a4e4d`  
		Last Modified: Tue, 23 Apr 2024 23:52:58 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6df52a8101c05850b0840427b9d830364bea581b586c5af98bb0c7a424769a`  
		Last Modified: Tue, 23 Apr 2024 23:52:58 GMT  
		Size: 501.3 KB (501255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93470676367d4b91723003ec292cfcca56c4baac1060cc6e0ede57df68686ca3`  
		Last Modified: Tue, 23 Apr 2024 23:52:57 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a64f8df61f19077ba301117ed5d43f969a11126340d943a795dd5495f04e424`  
		Last Modified: Tue, 23 Apr 2024 23:52:56 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129397c47de5e5edaa17a2c13235890e814ed06588e8b7e99c99da7c102aca09`  
		Last Modified: Tue, 23 Apr 2024 23:52:58 GMT  
		Size: 19.2 MB (19235435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da47b927c149b2fae4ff20377614a663cdd93fe558b2657b8f60be0cf5a66d40`  
		Last Modified: Tue, 23 Apr 2024 23:52:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02319e17a9d7ce2636ae96f119cabe5553dc17fce2315f05838aef9a0e07afa1`  
		Last Modified: Tue, 23 Apr 2024 23:52:55 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:502dd159c494837fc9065980ddb53f359e9cc4dad8fe30fb4533d68a95c24e82`  
		Last Modified: Tue, 23 Apr 2024 23:52:55 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55640999f7034968ab957263950b0c07914c89d4a8f7baf324d3172222c9a19b`  
		Last Modified: Tue, 23 Apr 2024 23:52:57 GMT  
		Size: 18.9 MB (18927299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61bc354de8a5b73184ab8435930f6bb331a3eca3501fb442304fb72cdaff603d`  
		Last Modified: Tue, 23 Apr 2024 23:52:54 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65fbfe6a971e909b070b243e4d06bf15f5bb357f55ad2b6b5e0ad90543ccc96b`  
		Last Modified: Tue, 23 Apr 2024 23:52:54 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a00d95494ccf8566d5c70351f6d86d3127d8250bb5591a525e9314e6cbc51b`  
		Last Modified: Tue, 23 Apr 2024 23:52:54 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1650ff156187703c6c419748912c0c77588ef058507987acdd818b4a669af593`  
		Last Modified: Tue, 23 Apr 2024 23:52:57 GMT  
		Size: 19.5 MB (19539069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.5696; amd64

```console
$ docker pull docker@sha256:419a83db6379468f26e2ec6a131548d9ffdf11b225d6240a665c72d71b9786f7
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2222590738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9c26a5abe59b14b61be3f69c8f3c43ff405131d8cceb5f326fc917b48d37971`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 23 Apr 2024 23:50:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 23 Apr 2024 23:52:29 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 23 Apr 2024 23:52:30 GMT
ENV DOCKER_VERSION=26.1.0
# Tue, 23 Apr 2024 23:52:30 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-26.1.0.zip
# Tue, 23 Apr 2024 23:53:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 23 Apr 2024 23:53:05 GMT
ENV DOCKER_BUILDX_VERSION=0.14.0
# Tue, 23 Apr 2024 23:53:05 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.windows-amd64.exe
# Tue, 23 Apr 2024 23:53:06 GMT
ENV DOCKER_BUILDX_SHA256=d43f5008431fb4ffd438d14ea686ed0f9c7ef101f2dfd1f84a5670979aeb39a8
# Tue, 23 Apr 2024 23:53:33 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 23 Apr 2024 23:53:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.26.1
# Tue, 23 Apr 2024 23:53:35 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-windows-x86_64.exe
# Tue, 23 Apr 2024 23:53:35 GMT
ENV DOCKER_COMPOSE_SHA256=d8a386d375ef26a77be0bee97516b0287d93acafb3976806f42e2b76c6904125
# Tue, 23 Apr 2024 23:53:59 GMT
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
	-	`sha256:16d80469a0d2df6d7da7089aaacbd9844a0842739c6f6a9cd497baf3e6af8597`  
		Last Modified: Tue, 23 Apr 2024 23:54:05 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac58ae951b23be092b0d306b19032acf99920815c91a2a000feda4a615a563e0`  
		Last Modified: Tue, 23 Apr 2024 23:54:05 GMT  
		Size: 486.2 KB (486191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:839bc6d7690aa38d58bc6a94f16b50073f7886e8e69bebacf508c55b8c3f6ee2`  
		Last Modified: Tue, 23 Apr 2024 23:54:04 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e645a87e1b1842318781ef7ab4f6909cb6e689fc42daeef335a94edd9c50bd`  
		Last Modified: Tue, 23 Apr 2024 23:54:04 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee61c15587dbd2a2c5efc72bec447bde4303145be891a819d21d2c9d7cdc33d7`  
		Last Modified: Tue, 23 Apr 2024 23:54:06 GMT  
		Size: 19.2 MB (19225934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6aa855979adf1dcf59e7bdfdcc66b50dba5af193cb08edf7ffd93161548f134`  
		Last Modified: Tue, 23 Apr 2024 23:54:03 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1fe8d1ad161dc4a8662c8fe2686ecefd8388f707feee9512f3980947336c57c`  
		Last Modified: Tue, 23 Apr 2024 23:54:03 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c665b062a1955877180dbddf7de297997c9cfefc9b172a5dd9a27f6bf7408f45`  
		Last Modified: Tue, 23 Apr 2024 23:54:03 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3e15349a9136628e27dbef8873c56c7cbb28e9e57d68428ec4c73ae2929400`  
		Last Modified: Tue, 23 Apr 2024 23:54:04 GMT  
		Size: 18.9 MB (18916235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a66680e0e172db550e0b6af1b057878f4261621951615be3b45c12b1b4b0c2a`  
		Last Modified: Tue, 23 Apr 2024 23:54:01 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e73bc7da5b305683e445df10cbf0141204f74292f4d7984c6198077669c8975`  
		Last Modified: Tue, 23 Apr 2024 23:54:02 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd2d98142b19e3b48bb521c81e32c7239e18fd412c8bbabbaa51e06563575d0`  
		Last Modified: Tue, 23 Apr 2024 23:54:02 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2b3942489fa27b148532f10436a25df28a59cb15d2c9a26fcdd7762831e81a`  
		Last Modified: Tue, 23 Apr 2024 23:54:04 GMT  
		Size: 19.5 MB (19522702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
