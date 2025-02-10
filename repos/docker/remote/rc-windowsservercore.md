## `docker:rc-windowsservercore`

```console
$ docker pull docker@sha256:a34f9b7e5b67102bd11b645557aadf52e6383c23723b12222bd3be61603aba54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `docker:rc-windowsservercore` - windows version 10.0.26100.2894; amd64

```console
$ docker pull docker@sha256:d8d1cda89556f2cc63184602e800980cc333f81ab9790534179e76c4bb8221cb
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2561876106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90884cfafcbab44a38222da25c11198d7e14c35f286c197b066bad904bc60cee`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Mon, 10 Feb 2025 19:31:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 10 Feb 2025 19:31:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 10 Feb 2025 19:31:43 GMT
ENV DOCKER_VERSION=28.0.0-rc.1
# Mon, 10 Feb 2025 19:31:43 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.0.0-rc.1.zip
# Mon, 10 Feb 2025 19:31:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 10 Feb 2025 19:31:53 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Mon, 10 Feb 2025 19:31:54 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.windows-amd64.exe
# Mon, 10 Feb 2025 19:31:55 GMT
ENV DOCKER_BUILDX_SHA256=39f53ec70c6ce37beca6898809e8eb89a77a1651be35ea50b51629c7a5d3b1f2
# Mon, 10 Feb 2025 19:32:03 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 10 Feb 2025 19:32:03 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 10 Feb 2025 19:32:04 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Mon, 10 Feb 2025 19:32:05 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Mon, 10 Feb 2025 19:32:13 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e8bb6d67e66867cd26dd75571a9921560ae7549a83cb7ffaf49c9b5cf8de8c`  
		Last Modified: Mon, 10 Feb 2025 19:32:19 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e146419bf0cafabd7c95cca7223b7fd2709fff5a9922c8a6eedb4dda9ac553f`  
		Last Modified: Mon, 10 Feb 2025 19:32:18 GMT  
		Size: 384.5 KB (384533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00befedf094078094ad0364ed2bad0c1b198a4c30a7e14f4164f24e370965b46`  
		Last Modified: Mon, 10 Feb 2025 19:32:17 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8452cd101f395a2a1a97e508fa7b09ba624f9e5e149396acac0a93cd363f2342`  
		Last Modified: Mon, 10 Feb 2025 19:32:17 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b05d9d424f3d0c5658e6ef1c4310292395fd766b6a9baa37340632d38cfab5`  
		Last Modified: Mon, 10 Feb 2025 19:32:19 GMT  
		Size: 19.8 MB (19814358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4820b5ebef8471388ac91eb6031d458dc07676d70f181db8975e0564371ef929`  
		Last Modified: Mon, 10 Feb 2025 19:32:16 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3eafcbe41b227623f16607ad596c80e7a88a8fbb5285b14c4939e6b2a1bc141`  
		Last Modified: Mon, 10 Feb 2025 19:32:16 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab0399db27f2e68a02688db07e2fd58a8ef7d74fb806c6d369f24c541310b82`  
		Last Modified: Mon, 10 Feb 2025 19:32:16 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef904bc3954677d34b300350c39ea44bff65ab42be00a32b8465be45974a8b88`  
		Last Modified: Mon, 10 Feb 2025 19:32:18 GMT  
		Size: 21.2 MB (21179334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760d7f549a1ba08606bdadb13e9020d6fe8bd0d0b6a86ec459de63c4471d87ee`  
		Last Modified: Mon, 10 Feb 2025 19:32:15 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53133fd9219d43ca4ac2d464c67c795da883fd0d9af126788718ca96e67f6e59`  
		Last Modified: Mon, 10 Feb 2025 19:32:15 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:896fb6a29e0c8b0155e78f66f81983033dc44b3f831c05f27e33df46110b8024`  
		Last Modified: Mon, 10 Feb 2025 19:32:15 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e84e59864ba0ecea7a15bff7de6ee2e33783fb5c20d08073f0318d515eac73d`  
		Last Modified: Mon, 10 Feb 2025 19:32:18 GMT  
		Size: 20.2 MB (20208550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:rc-windowsservercore` - windows version 10.0.20348.3091; amd64

```console
$ docker pull docker@sha256:46f2f7f28e1660b17972a884166ff04a08fd4894d705f396dcefd15ab4f160f3
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2323759547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b35da0a7c266a4f85b86e521abc50ba87d800b23161a5d1c243112658f954b3d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Mon, 10 Feb 2025 19:28:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 10 Feb 2025 19:29:01 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 10 Feb 2025 19:29:02 GMT
ENV DOCKER_VERSION=28.0.0-rc.1
# Mon, 10 Feb 2025 19:29:02 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.0.0-rc.1.zip
# Mon, 10 Feb 2025 19:29:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 10 Feb 2025 19:29:25 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Mon, 10 Feb 2025 19:29:25 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.windows-amd64.exe
# Mon, 10 Feb 2025 19:29:26 GMT
ENV DOCKER_BUILDX_SHA256=39f53ec70c6ce37beca6898809e8eb89a77a1651be35ea50b51629c7a5d3b1f2
# Mon, 10 Feb 2025 19:29:35 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 10 Feb 2025 19:29:35 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 10 Feb 2025 19:29:36 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Mon, 10 Feb 2025 19:29:37 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Mon, 10 Feb 2025 19:29:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a213871dc509676833c3969ea1cb16f84310de2d456b4021d90c29e3aca9d2d2`  
		Last Modified: Mon, 10 Feb 2025 19:29:54 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9fc4c72bdc1a56ac7d8c2c95740ba3a0b085594900e8ca1cc8bad995741c990`  
		Last Modified: Mon, 10 Feb 2025 19:29:54 GMT  
		Size: 361.9 KB (361914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bd3ab2a430972d1a591e2f4ea777bd242e9de88a6345eb5b8f8af7f6c45960f`  
		Last Modified: Mon, 10 Feb 2025 19:29:53 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779e8d8aec56d18f71c4fb7faa6f9f4ab072ea9847151f6d0545718a1112143f`  
		Last Modified: Mon, 10 Feb 2025 19:29:53 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:569dd59dadb8ac2d4585e7897b0dd6f6b246df1b64080aff8496cdd9f57768dd`  
		Last Modified: Mon, 10 Feb 2025 19:29:54 GMT  
		Size: 19.7 MB (19746376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab598433afc79b8b1057224b16c125b2d2e1a0e73f17db626b29716c3f96fbd`  
		Last Modified: Mon, 10 Feb 2025 19:29:52 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c720194805c2a72822522d63e42d220e0940a68cbd5f9b9bcd5fdb824e50c35b`  
		Last Modified: Mon, 10 Feb 2025 19:29:52 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98e1b0aea560ed6c668bad2cf94c9e1969c81fc3c8f08210ebb2cc927806bcd`  
		Last Modified: Mon, 10 Feb 2025 19:29:52 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81f1085e099f74fc0bdd3059622af8bdaeecd85fd5400154b8a169838f18ffa`  
		Last Modified: Mon, 10 Feb 2025 19:29:54 GMT  
		Size: 21.1 MB (21113111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8195a4d1932f29a79f1e8a91d897a36991b5e82da2968a04ba6ebd4d9a1d41c9`  
		Last Modified: Mon, 10 Feb 2025 19:29:51 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd64c4f18c1c7af704d82b583124edbb141c7121f77457701bff0a2fe017293`  
		Last Modified: Mon, 10 Feb 2025 19:29:51 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63621efff038217af888388aa3c756c75b063224ce27bad543d4a772d03bdc19`  
		Last Modified: Mon, 10 Feb 2025 19:29:51 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e346e19eae77eefd56ddaf6956374587cca631f08023a45e5dcfbe517be36e3`  
		Last Modified: Mon, 10 Feb 2025 19:29:53 GMT  
		Size: 20.1 MB (20141059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:rc-windowsservercore` - windows version 10.0.17763.6775; amd64

```console
$ docker pull docker@sha256:7714ffae44851ceadb7ce05df46c8f31fc058e90cb050c80d69ddb2b58d2bd28
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2183634877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565224969ab6d580f99a1d91d01207c6aa873aa5aa14aa8e7a87179704d34b8f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Mon, 10 Feb 2025 19:27:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 10 Feb 2025 19:28:23 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 10 Feb 2025 19:28:23 GMT
ENV DOCKER_VERSION=28.0.0-rc.1
# Mon, 10 Feb 2025 19:28:24 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.0.0-rc.1.zip
# Mon, 10 Feb 2025 19:28:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 10 Feb 2025 19:28:39 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Mon, 10 Feb 2025 19:28:40 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.windows-amd64.exe
# Mon, 10 Feb 2025 19:28:41 GMT
ENV DOCKER_BUILDX_SHA256=39f53ec70c6ce37beca6898809e8eb89a77a1651be35ea50b51629c7a5d3b1f2
# Mon, 10 Feb 2025 19:28:53 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 10 Feb 2025 19:28:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 10 Feb 2025 19:28:54 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Mon, 10 Feb 2025 19:28:55 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Mon, 10 Feb 2025 19:29:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad421ac7b9b1a4c9fccb5d9be1b4c39a7980c94365636f8cd8d8c9c3371e79a3`  
		Last Modified: Mon, 10 Feb 2025 19:29:16 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c117c3ead9914a0a5d20416354afb307216b046e784751991e2c39637ae2ab3b`  
		Last Modified: Mon, 10 Feb 2025 19:29:17 GMT  
		Size: 340.1 KB (340071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a6cff2c2e1714567784de34d844b4f7e5d016fc009d0419de7ec6e96b5dd46`  
		Last Modified: Mon, 10 Feb 2025 19:29:15 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef5d05858ed84a3e18ad3414a6dcc2e8721d6a10f1221ebf196a064eb30a6c9`  
		Last Modified: Mon, 10 Feb 2025 19:29:15 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd23188b85bae2a5c99b1be179068cefe1a4efb06026a6f5d18661d5b463dcf8`  
		Last Modified: Mon, 10 Feb 2025 19:29:17 GMT  
		Size: 19.8 MB (19775687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2e0087b99ecccee549815cabbea01dd00cb39b844aebabb31cc9f4efb8c630`  
		Last Modified: Mon, 10 Feb 2025 19:29:13 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b5c61405a12a15018a09f70a6c3449e6a4a1e7bd5e4271e7e12dbe9517622e`  
		Last Modified: Mon, 10 Feb 2025 19:29:13 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b843f8f863211e43a7aa438bdda92df683b2c04ba30a66702eb1ee7dd9f7a3`  
		Last Modified: Mon, 10 Feb 2025 19:29:13 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1fe62c994507df2ffeaa49907c8ae1de2966cc42c640de512908a86d74cd96`  
		Last Modified: Mon, 10 Feb 2025 19:29:14 GMT  
		Size: 21.1 MB (21131375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d619581d802e88f96c89aaca9f1b2ebc8879f0628091808d6114f0c9f33f3476`  
		Last Modified: Mon, 10 Feb 2025 19:29:11 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579795127c5544d3f700ecc76bba61de71d65567d4d6fc88970be3ced0948eb9`  
		Last Modified: Mon, 10 Feb 2025 19:29:11 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e7d8e3689a1094d7a8b9f1c5a772c8653297b5969a7bd81773b92395639dba`  
		Last Modified: Mon, 10 Feb 2025 19:29:11 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8786e98794ffc685ace3c69ece60579421998ca3a2da340ed005087278b0f3ce`  
		Last Modified: Mon, 10 Feb 2025 19:29:14 GMT  
		Size: 20.2 MB (20163836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
