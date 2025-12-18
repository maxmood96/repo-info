## `docker:29-rc-windowsservercore`

```console
$ docker pull docker@sha256:22041eb1f0c29aecb57f2d1c346262a6f92a6e821be5e61c826d1540302366a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7462; amd64
	-	windows version 10.0.20348.4529; amd64

### `docker:29-rc-windowsservercore` - windows version 10.0.26100.7462; amd64

```console
$ docker pull docker@sha256:c31edc866f5ef83b59d427cf4cee66b397c56390bea0e56228456c301bbd1e4f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3308417935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fd1fd3cbe8bc7717e8925ad87b7fc64faa3f7b1b0e2ab9b0634e2ee5371f9ed`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Dec 2025 21:49:56 GMT
RUN Install update 10.0.26100.7462
# Wed, 17 Dec 2025 22:01:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 17 Dec 2025 22:02:38 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 17 Dec 2025 22:02:39 GMT
ENV DOCKER_VERSION=29.2.0-rc.1
# Wed, 17 Dec 2025 22:02:40 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-29.2.0-rc.1.zip
# Wed, 17 Dec 2025 22:02:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 17 Dec 2025 22:02:53 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 17 Dec 2025 22:02:54 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Wed, 17 Dec 2025 22:02:54 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Wed, 17 Dec 2025 22:03:03 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 17 Dec 2025 22:03:03 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 17 Dec 2025 22:03:04 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-windows-x86_64.exe
# Wed, 17 Dec 2025 22:03:04 GMT
ENV DOCKER_COMPOSE_SHA256=e8a5338e20bc6d30ae38db5533ce63ebf3c229801c20a74051fd06a650e5a8f9
# Wed, 17 Dec 2025 22:03:11 GMT
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
	-	`sha256:a64e949a48c210bd8665ab95d2199027ac2a2c8c5e7b5cf04101665776947369`  
		Last Modified: Wed, 17 Dec 2025 22:20:45 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55cfa892e8ea71e039ad0596fb244b04ac5ac5609870f990bfa817aa11cb15ec`  
		Last Modified: Wed, 17 Dec 2025 22:20:45 GMT  
		Size: 402.7 KB (402659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:853ba6556d6ab77903d91cd44ff2a26176d6add43f3bb7ea6f1cc8b13ae507cb`  
		Last Modified: Wed, 17 Dec 2025 22:20:45 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4295f0cc9139e53b63b4d7919f9d81866b9179b0a393d4a039e6a2870a9cc2`  
		Last Modified: Wed, 17 Dec 2025 22:20:45 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e6830bfaa4814605fdb76d82c9ff2998673daca58bdaea8bd2b34d9bd1f5b4`  
		Last Modified: Wed, 17 Dec 2025 22:20:47 GMT  
		Size: 19.5 MB (19462863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a5db39bd33171d7a94e46c6666f25a717f046f3812b855040cc107043a457cd`  
		Last Modified: Wed, 17 Dec 2025 22:20:45 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27946ac22728bb1edca0b22cc056058a8abe860c52ab2dad0779aff103d8fcfb`  
		Last Modified: Wed, 17 Dec 2025 22:20:45 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3210be38e9910d65856e6b736534a8aeef2a359bd142e7bfb7a967ec2614635`  
		Last Modified: Wed, 17 Dec 2025 22:20:45 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002a870c6fc232b6abb9d611de70ffedd59c1f76a9c33ed9e2af556ea0f6e210`  
		Last Modified: Wed, 17 Dec 2025 22:20:49 GMT  
		Size: 23.9 MB (23949958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd11d5dfa76696918d30414964a1bed56980ffb8c6a48fdce69cf36eb6dbca3e`  
		Last Modified: Wed, 17 Dec 2025 22:20:45 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c39d638487c58a833de4fa500a7b21f0cdb2dae9c8403035d7d5fd04ea635d0`  
		Last Modified: Wed, 17 Dec 2025 22:20:45 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80278ee330fd9c5d86af1edf21bf81032481a48a27a9a4dc52ebc9825b138d82`  
		Last Modified: Wed, 17 Dec 2025 22:20:45 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48530086ca6811bbde1b97290fdb66717fbc7fc858fc97cdf7ea2e36688b840c`  
		Last Modified: Wed, 17 Dec 2025 22:20:47 GMT  
		Size: 11.5 MB (11470346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29-rc-windowsservercore` - windows version 10.0.20348.4529; amd64

```console
$ docker pull docker@sha256:05c368ec69feeedf5610aff9823ed8b949de198b2238ccfcccde7286c84f3c12
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1835177316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40f3c1a0dcf2c62f39622051c3bb735b4db16d145343c677ec1b3b259d5ce84b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Wed, 17 Dec 2025 22:21:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 17 Dec 2025 22:21:53 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 17 Dec 2025 22:21:53 GMT
ENV DOCKER_VERSION=29.2.0-rc.1
# Wed, 17 Dec 2025 22:21:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-29.2.0-rc.1.zip
# Wed, 17 Dec 2025 22:22:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 17 Dec 2025 22:22:15 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 17 Dec 2025 22:22:16 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Wed, 17 Dec 2025 22:22:17 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Wed, 17 Dec 2025 22:22:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 17 Dec 2025 22:22:40 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 17 Dec 2025 22:22:40 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-windows-x86_64.exe
# Wed, 17 Dec 2025 22:22:41 GMT
ENV DOCKER_COMPOSE_SHA256=e8a5338e20bc6d30ae38db5533ce63ebf3c229801c20a74051fd06a650e5a8f9
# Wed, 17 Dec 2025 22:22:55 GMT
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
	-	`sha256:f15fbd97b1db2c11c6a83d2abe864c71bdad436420fa4b87cdddbc318940dfa6`  
		Last Modified: Wed, 17 Dec 2025 22:32:37 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3daa6982734debb16d777f0da00327753680f264ec092909201f052ac9033925`  
		Last Modified: Wed, 17 Dec 2025 22:32:37 GMT  
		Size: 501.2 KB (501175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:247517d9f44cc165729060fa0cb1c1e58af3c5c7801b6c9beb748880a74ce6f2`  
		Last Modified: Wed, 17 Dec 2025 22:32:37 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e739d6e53c0deb5627b909a779ac38268365ff94202f3be105f7a04e592b92bc`  
		Last Modified: Wed, 17 Dec 2025 22:32:37 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd15f4b120ad5f0164308ccae0f9761aa223b55fd4d567c3922b3e3aa7a643da`  
		Last Modified: Wed, 17 Dec 2025 22:32:40 GMT  
		Size: 19.4 MB (19426495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da1f83517d9049bc971f329acafc5bec0dc92b59ab53fc4725288b139a11ffe`  
		Last Modified: Wed, 17 Dec 2025 22:32:37 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f09773bfc442cc918e2e101e09d2a8b76fec46dc31e8a906e925dc0d13b14db`  
		Last Modified: Wed, 17 Dec 2025 22:32:38 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687912b954660a73d7eeddc2f2e559a6966e5f9af5101bbcc488a29211124e78`  
		Last Modified: Wed, 17 Dec 2025 22:32:38 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe20f5149441870cada28db557d2169cc1411984ad07ca19a4798e02342e8e6`  
		Last Modified: Wed, 17 Dec 2025 22:32:40 GMT  
		Size: 23.9 MB (23922490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50eaa937965704e12a2a2b56d356c10e29f32af2fff592387bcf405a5adc0033`  
		Last Modified: Wed, 17 Dec 2025 22:32:38 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:501f5457d14a019dcd42840f47504e3dd6256197ca8c1f9bd157594d07b53bee`  
		Last Modified: Wed, 17 Dec 2025 22:32:36 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c2a8e2d14fb9bc14690ee763365fc182c25cb621501556835269ed5c207e02`  
		Last Modified: Wed, 17 Dec 2025 22:32:36 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b684e33096cbec38221da883b0af0fcfc09ecac83a8cb6a657ce0b1f1a26701d`  
		Last Modified: Wed, 17 Dec 2025 22:32:37 GMT  
		Size: 11.4 MB (11436104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
