## `docker:28-rc-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:09c684b756a00b6134791e50af79db3caf6d4482d33173572d15d33be281d5f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `docker:28-rc-windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

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
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 21:54:27 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a213871dc509676833c3969ea1cb16f84310de2d456b4021d90c29e3aca9d2d2`  
		Last Modified: Mon, 10 Feb 2025 21:10:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9fc4c72bdc1a56ac7d8c2c95740ba3a0b085594900e8ca1cc8bad995741c990`  
		Last Modified: Mon, 10 Feb 2025 21:10:09 GMT  
		Size: 361.9 KB (361914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bd3ab2a430972d1a591e2f4ea777bd242e9de88a6345eb5b8f8af7f6c45960f`  
		Last Modified: Mon, 10 Feb 2025 21:10:09 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779e8d8aec56d18f71c4fb7faa6f9f4ab072ea9847151f6d0545718a1112143f`  
		Last Modified: Mon, 10 Feb 2025 21:10:09 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:569dd59dadb8ac2d4585e7897b0dd6f6b246df1b64080aff8496cdd9f57768dd`  
		Last Modified: Mon, 10 Feb 2025 21:10:10 GMT  
		Size: 19.7 MB (19746376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab598433afc79b8b1057224b16c125b2d2e1a0e73f17db626b29716c3f96fbd`  
		Last Modified: Tue, 11 Feb 2025 00:33:02 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c720194805c2a72822522d63e42d220e0940a68cbd5f9b9bcd5fdb824e50c35b`  
		Last Modified: Tue, 11 Feb 2025 00:33:02 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98e1b0aea560ed6c668bad2cf94c9e1969c81fc3c8f08210ebb2cc927806bcd`  
		Last Modified: Mon, 10 Feb 2025 21:10:09 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81f1085e099f74fc0bdd3059622af8bdaeecd85fd5400154b8a169838f18ffa`  
		Last Modified: Mon, 10 Feb 2025 21:10:10 GMT  
		Size: 21.1 MB (21113111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8195a4d1932f29a79f1e8a91d897a36991b5e82da2968a04ba6ebd4d9a1d41c9`  
		Last Modified: Mon, 10 Feb 2025 21:10:09 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd64c4f18c1c7af704d82b583124edbb141c7121f77457701bff0a2fe017293`  
		Last Modified: Tue, 11 Feb 2025 00:33:04 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63621efff038217af888388aa3c756c75b063224ce27bad543d4a772d03bdc19`  
		Last Modified: Tue, 11 Feb 2025 00:33:04 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e346e19eae77eefd56ddaf6956374587cca631f08023a45e5dcfbe517be36e3`  
		Last Modified: Mon, 10 Feb 2025 21:10:09 GMT  
		Size: 20.1 MB (20141059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
