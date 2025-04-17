## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:0e3165a326104dd3ad878334450ca69407002dd9f2ebaccba66e4ce78d8f9c31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3775; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.3775; amd64

```console
$ docker pull docker@sha256:d85562ac9bf51b00d6bb67bfa82a01d77e92962ce2df6fea152bd784e779350d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3459283331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcf86844da028fbaa04ce4598b6416501a2467541288fc1e4f79a81c88ca4bc6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 06 Apr 2025 07:48:58 GMT
RUN Install update 10.0.26100.3775
# Thu, 17 Apr 2025 18:33:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Apr 2025 18:34:01 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 17 Apr 2025 18:34:02 GMT
ENV DOCKER_VERSION=28.1.0
# Thu, 17 Apr 2025 18:34:03 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.0.zip
# Thu, 17 Apr 2025 18:34:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 17 Apr 2025 18:34:15 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Thu, 17 Apr 2025 18:34:16 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Thu, 17 Apr 2025 18:34:17 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Thu, 17 Apr 2025 18:34:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 17 Apr 2025 18:34:29 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.1
# Thu, 17 Apr 2025 18:34:30 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-windows-x86_64.exe
# Thu, 17 Apr 2025 18:34:31 GMT
ENV DOCKER_COMPOSE_SHA256=971d6000e2c70da19c20f8264330a7ec3962b1fd59601afeb7e3636bad89b8c9
# Thu, 17 Apr 2025 18:34:42 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761846874dadc4dd9490d5635a266306989ac061986d0e4bcfe36a76ef6888b8`  
		Last Modified: Tue, 08 Apr 2025 21:29:58 GMT  
		Size: 1.2 GB (1179372285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f1d6fec13d2b78dbb90905d1bdcc48f4f3320393b795eded7978013045e6534`  
		Last Modified: Thu, 17 Apr 2025 18:34:50 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9256be1a2f31b140534c90582759e2b24207428369106d9742260c95dd19c7ef`  
		Last Modified: Thu, 17 Apr 2025 18:34:50 GMT  
		Size: 396.5 KB (396548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9daab20df86881f5f3c09e0c3f394b365bffa36870115e838711d1b121533a`  
		Last Modified: Thu, 17 Apr 2025 18:34:49 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe08ddff8efa70a7e9b5a3557428ac7dad12b5a0fc2ccebcbd9b4578a01c3169`  
		Last Modified: Thu, 17 Apr 2025 18:34:49 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ce3a76ead6cc32a14ee9ffb79636617cf22bbea876b8ae398355e6b9457993`  
		Last Modified: Thu, 17 Apr 2025 18:34:51 GMT  
		Size: 19.9 MB (19927195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66696ecdd15b3d3ddf6b06596dfa8602574d013a5c308f31fb3416aeca903bbd`  
		Last Modified: Thu, 17 Apr 2025 18:34:48 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd67e9cc3798ccefcaab2f37eee58f0d8fe4400629df9cd9aac726c71ee3323`  
		Last Modified: Thu, 17 Apr 2025 18:34:47 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f2629857f7c604cfc7dbfd7799a28161d94e3cba57e45d66fc9e810f0a9648`  
		Last Modified: Thu, 17 Apr 2025 18:34:47 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace0e5d4fa774957df01e0d2ffdb0080ab092200e1d40fe6a64aba2a1e414bac`  
		Last Modified: Thu, 17 Apr 2025 18:34:49 GMT  
		Size: 22.4 MB (22387723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a15328c76c09357141f88a166fe6094769190ac088339efa79d5764c18b99d`  
		Last Modified: Thu, 17 Apr 2025 18:34:46 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a068518252386032a7f7f1d40662c12a7241f048fbeaf4c59ec80d347be23194`  
		Last Modified: Thu, 17 Apr 2025 18:34:46 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2853a7df2b548d113284e9ba5b71311f8abffb176d0341a772dc85d389d08fa`  
		Last Modified: Thu, 17 Apr 2025 18:34:47 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4da08aa43669ddec97d1fc1af5c73a488852d3ee30761251b0cec33fead47f`  
		Last Modified: Thu, 17 Apr 2025 18:34:49 GMT  
		Size: 21.9 MB (21880315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
