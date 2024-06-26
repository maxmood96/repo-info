## `docker:25-windowsservercore`

```console
$ docker pull docker@sha256:1a522e5f311d5b646fb8ad6fc342f15f91e35393eaf31f8959c7c8ff1a138023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2529; amd64
	-	windows version 10.0.17763.5936; amd64

### `docker:25-windowsservercore` - windows version 10.0.20348.2529; amd64

```console
$ docker pull docker@sha256:2c29af40935aceba1595595e0c769263b62ad37ba0358c6b5186f087bc547044
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2175300721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ba278b991fe45b7289d5b00c26089137c6e610adba4493c1fdd0a3dfa291fb8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 19 Jun 2024 19:58:05 GMT
RUN Install update 10.0.20348.2529
# Mon, 24 Jun 2024 23:04:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 24 Jun 2024 23:04:28 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 24 Jun 2024 23:04:28 GMT
ENV DOCKER_VERSION=25.0.5
# Mon, 24 Jun 2024 23:04:29 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-25.0.5.zip
# Mon, 24 Jun 2024 23:04:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 24 Jun 2024 23:04:39 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Mon, 24 Jun 2024 23:04:40 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.windows-amd64.exe
# Mon, 24 Jun 2024 23:04:40 GMT
ENV DOCKER_BUILDX_SHA256=d28cff3df9fdbb37aa7434edb09d8befe5e90e5ef5887807569b694f25bebd33
# Mon, 24 Jun 2024 23:04:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 24 Jun 2024 23:04:48 GMT
ENV DOCKER_COMPOSE_VERSION=2.28.1
# Mon, 24 Jun 2024 23:04:48 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-windows-x86_64.exe
# Mon, 24 Jun 2024 23:04:49 GMT
ENV DOCKER_COMPOSE_SHA256=7dbd8848d9b8dce489c4d2ce1bb4f4b7a3dccb07a08596ae98b85091e1645bcc
# Mon, 24 Jun 2024 23:04:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb373ec9afdfc5f09b9380d981e0c61f9c7b48537b887135c7c66810086e705e`  
		Last Modified: Fri, 21 Jun 2024 00:27:54 GMT  
		Size: 729.6 MB (729591500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3748d42dc0e5259e67f82a2e11b61aa77aa393a19b2f172078a7f272c2678e76`  
		Last Modified: Mon, 24 Jun 2024 23:05:01 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c30ea1e085b1dd25cd3facc0b222560cdf92e785685d1458f995bae82375feea`  
		Last Modified: Mon, 24 Jun 2024 23:05:01 GMT  
		Size: 355.9 KB (355917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dc88a06260288066e46ac8e15402dcb7992135e540bc8dec6fe138c4f54cfe`  
		Last Modified: Mon, 24 Jun 2024 23:05:01 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ed3cb69009b8c11287759962e5e9b436a48cedbb3bc56852765079dd941882`  
		Last Modified: Mon, 24 Jun 2024 23:05:00 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0221a2ea52e64ec05b3b5f6d0fd8e17b7dbf4c7a7e548464287cb371028d6086`  
		Last Modified: Mon, 24 Jun 2024 23:05:02 GMT  
		Size: 18.1 MB (18067951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a10fc01583dcfc23bede2bcf44eac90c52a2ad64b6a1b6c04ec51bc781c92535`  
		Last Modified: Mon, 24 Jun 2024 23:04:59 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:609dc5121209c90648e892c6dce4acad1b7f646c375101a6bac734b223142f46`  
		Last Modified: Mon, 24 Jun 2024 23:04:59 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9b45da6e6af1bbb804402127960c0b7c2b8bb9f0d16aea4d656a0af3b77197`  
		Last Modified: Mon, 24 Jun 2024 23:04:59 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ca3e53a83f8a3187e7281d3605224911126df2ccadd5664dc6f3d4c340793e2`  
		Last Modified: Mon, 24 Jun 2024 23:05:01 GMT  
		Size: 19.0 MB (19019407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07db5ca5025f5a215342fefe5986db1cbc82b12d2398360a3e96514602e2cf9`  
		Last Modified: Mon, 24 Jun 2024 23:04:58 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f1f64ce6eb82d2501b880eb3216ca97e3012653fc950610d036cb0c110d7525`  
		Last Modified: Mon, 24 Jun 2024 23:04:58 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:641b1371c1374dbfe7ab9a0a59bf49f63c5172de0b85940a191c146b0913c819`  
		Last Modified: Mon, 24 Jun 2024 23:04:58 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12aec8503f2b3c62234ed5811f1140ab032cfdc9427d7f4a6f09ed2cddfed6f3`  
		Last Modified: Mon, 24 Jun 2024 23:05:01 GMT  
		Size: 19.7 MB (19655548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:25-windowsservercore` - windows version 10.0.17763.5936; amd64

```console
$ docker pull docker@sha256:d129b6325908ffe268d4c631460e118897b8c6f138c75969ef1b351c8672939c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2277898303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f651bd10571fd06e5df6ec1eda12c9d8481342bc30ecb49be9f8d04de10366a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Mon, 24 Jun 2024 23:01:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 24 Jun 2024 23:01:47 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 24 Jun 2024 23:01:48 GMT
ENV DOCKER_VERSION=25.0.5
# Mon, 24 Jun 2024 23:01:49 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-25.0.5.zip
# Mon, 24 Jun 2024 23:02:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 24 Jun 2024 23:02:11 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Mon, 24 Jun 2024 23:02:11 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.windows-amd64.exe
# Mon, 24 Jun 2024 23:02:12 GMT
ENV DOCKER_BUILDX_SHA256=d28cff3df9fdbb37aa7434edb09d8befe5e90e5ef5887807569b694f25bebd33
# Mon, 24 Jun 2024 23:02:33 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 24 Jun 2024 23:02:33 GMT
ENV DOCKER_COMPOSE_VERSION=2.28.1
# Mon, 24 Jun 2024 23:02:34 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-windows-x86_64.exe
# Mon, 24 Jun 2024 23:02:34 GMT
ENV DOCKER_COMPOSE_SHA256=7dbd8848d9b8dce489c4d2ce1bb4f4b7a3dccb07a08596ae98b85091e1645bcc
# Mon, 24 Jun 2024 23:02:55 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d318046e9bd440ea0ec9aa57ed990f601c21029c08febd870293f2ee967158`  
		Last Modified: Mon, 24 Jun 2024 23:03:05 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b6a96970d573ec6e9760a86cdc0a456dd6479574267f796ad43b792da32578`  
		Last Modified: Mon, 24 Jun 2024 23:03:06 GMT  
		Size: 481.5 KB (481492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495347e01dc603993c293020dfa6d661537b6cdbbec59f694b0d333d62ecd4d2`  
		Last Modified: Mon, 24 Jun 2024 23:03:03 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21addd8bbb3c944e698a3c36527388b6ae41214fc6868a10b6eb31b503ebfe5e`  
		Last Modified: Mon, 24 Jun 2024 23:03:03 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8520bffd5bd95254b22f2d3f5e6128851cdf49b89b4da1d0fd9edab4ca3d4964`  
		Last Modified: Mon, 24 Jun 2024 23:03:05 GMT  
		Size: 18.1 MB (18064503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc09ff4cb1d375668d4c2e7a754eab22acd24a771a2610a0f98c0ff8c4dddeed`  
		Last Modified: Mon, 24 Jun 2024 23:03:01 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2998ec6e21ca6b19d5f95b35549574d844a66f0d3f16816d1bb3a32e34f98c7b`  
		Last Modified: Mon, 24 Jun 2024 23:03:01 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fdd9aefd1b57666cc641e153d39b2ada8775b61ae32897a539f585c82278ec1`  
		Last Modified: Mon, 24 Jun 2024 23:03:01 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d2bd0fd170580a775f6ba04acdd55bab9fdcf6faac0c4f44b6e0b3d47309da`  
		Last Modified: Mon, 24 Jun 2024 23:03:03 GMT  
		Size: 19.0 MB (19015838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0251f15d108b52c6d86f976a7df10e9942230c2a9a246dc76cbf6dff16dac39`  
		Last Modified: Mon, 24 Jun 2024 23:02:59 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36db4b9f4a5405193f29309425270265a175f5e11a80e35e4165b86069dd71cb`  
		Last Modified: Mon, 24 Jun 2024 23:02:59 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecfc5cacb05fa2d800e08dbe7e5e6d9c38bdefd6e2aa2226e5a0a468507ace40`  
		Last Modified: Mon, 24 Jun 2024 23:02:59 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c7b53da34a5b0befcc9d5790a2ada6eec7216121aff924dd1c7ac3d8891fb1`  
		Last Modified: Mon, 24 Jun 2024 23:03:02 GMT  
		Size: 19.6 MB (19643630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
