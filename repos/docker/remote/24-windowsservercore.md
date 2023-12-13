## `docker:24-windowsservercore`

```console
$ docker pull docker@sha256:05f41b9519a2909fbb253190d7b2e549da0eca6049ae5be3cc522a99b7e2bf60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2159; amd64
	-	windows version 10.0.17763.5206; amd64

### `docker:24-windowsservercore` - windows version 10.0.20348.2159; amd64

```console
$ docker pull docker@sha256:d4019940a6d9084eb27c1e8dee17fbe1fb76953776e419cce36eaac9bdcabe19
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1944069128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10725151cb22ce19736a5deda5c66840869a2e879a47da1e9b8519157ef3c650`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 02 Dec 2023 12:42:56 GMT
RUN Install update 10.0.20348.2159
# Wed, 13 Dec 2023 01:00:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Dec 2023 01:00:32 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Dec 2023 01:00:33 GMT
ENV DOCKER_VERSION=24.0.7
# Wed, 13 Dec 2023 01:00:34 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.7.zip
# Wed, 13 Dec 2023 01:00:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 13 Dec 2023 01:00:44 GMT
ENV DOCKER_BUILDX_VERSION=0.12.0
# Wed, 13 Dec 2023 01:00:44 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.windows-amd64.exe
# Wed, 13 Dec 2023 01:00:45 GMT
ENV DOCKER_BUILDX_SHA256=dcf01329368381fae8c24b494186a30d2f1c4adb4bef7a0410b4803e5bb1c352
# Wed, 13 Dec 2023 01:00:52 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 13 Dec 2023 01:00:52 GMT
ENV DOCKER_COMPOSE_VERSION=2.23.3
# Wed, 13 Dec 2023 01:00:53 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-windows-x86_64.exe
# Wed, 13 Dec 2023 01:00:54 GMT
ENV DOCKER_COMPOSE_SHA256=7d3f56cc84838ca54c5f0e9c8a3645dd96030482d838663c367d93bc6c38dc05
# Wed, 13 Dec 2023 01:01:01 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7839fc47f6e056f9e09a214230f8b7115e69419dbc74acbbb1ad6bc0caa28862`  
		Last Modified: Tue, 12 Dec 2023 18:27:40 GMT  
		Size: 500.7 MB (500674814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e373ced59cc31b2425e95540d100453fcc2e67e92b4599bf136485fdd462e630`  
		Last Modified: Wed, 13 Dec 2023 01:01:07 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d5218b1a5b8caab533b1476bef5a5d3ec3c389cb0f311604de698fd7e8f2c5c`  
		Last Modified: Wed, 13 Dec 2023 01:01:07 GMT  
		Size: 504.0 KB (504037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279806202655dca7da02fe6b9bf46d63c897ce9d0ebc701886314c96ee3bfe93`  
		Last Modified: Wed, 13 Dec 2023 01:01:06 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90506bc6ce60aed7c8bad1d4cdd06145f7d865ab140626a4422797c6dbffac26`  
		Last Modified: Wed, 13 Dec 2023 01:01:06 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df275c74dca36f8ae807411b1c9056169ce422d63f309c0264a02e69dc055efa`  
		Last Modified: Wed, 13 Dec 2023 01:01:07 GMT  
		Size: 17.5 MB (17536934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5375651333ba20b1f13d8df17f60c242160b5cf6742862821228f4656f8f1ac2`  
		Last Modified: Wed, 13 Dec 2023 01:01:05 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa7be51790c2456da8bb7c2cefb44beb77c1c4c18bdcd2fce77049a32b337b7`  
		Last Modified: Wed, 13 Dec 2023 01:01:05 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c22336bd0bb577de8872f48521d5e6095ed3b3e1e6dcff0366d42d689f5442f`  
		Last Modified: Wed, 13 Dec 2023 01:01:04 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:025e28bd720bb992991a10737ff12f0b7fc2a2d89fa6d9b69e7a612029a7e2d0`  
		Last Modified: Wed, 13 Dec 2023 01:01:05 GMT  
		Size: 18.0 MB (18028927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841a904cc1c6c423e8fef7740a30ca20b6f260101caaa0dc41bdd48478d7b625`  
		Last Modified: Wed, 13 Dec 2023 01:01:03 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59cc15bd3584c597d3d837f65453c389cdbbd154a8a628a6ea3faed64b4ffd3f`  
		Last Modified: Wed, 13 Dec 2023 01:01:03 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a871204ade8c2b511fed5e703c29d72e9b2bdbde3533dc58bdfbee0e37592b16`  
		Last Modified: Wed, 13 Dec 2023 01:01:03 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc8c8de0f3be8cb471c1101e08980008f8c92632a5c075a7346669bf282d7aa`  
		Last Modified: Wed, 13 Dec 2023 01:01:06 GMT  
		Size: 18.7 MB (18713988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:24-windowsservercore` - windows version 10.0.17763.5206; amd64

```console
$ docker pull docker@sha256:7027d3ec1bedc671c1b79772d8b8077913edcd14f6a8c61e60eaa261690c5335
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2114501537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8864e4030552b2b1f29290ae0438b1c98a0b35d96b852b93e15011a083f3156b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Dec 2023 11:24:49 GMT
RUN Install update 10.0.17763.5206
# Wed, 13 Dec 2023 00:59:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Dec 2023 00:59:57 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Dec 2023 00:59:58 GMT
ENV DOCKER_VERSION=24.0.7
# Wed, 13 Dec 2023 00:59:58 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.7.zip
# Wed, 13 Dec 2023 01:00:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 13 Dec 2023 01:00:24 GMT
ENV DOCKER_BUILDX_VERSION=0.12.0
# Wed, 13 Dec 2023 01:00:25 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.windows-amd64.exe
# Wed, 13 Dec 2023 01:00:26 GMT
ENV DOCKER_BUILDX_SHA256=dcf01329368381fae8c24b494186a30d2f1c4adb4bef7a0410b4803e5bb1c352
# Wed, 13 Dec 2023 01:00:48 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 13 Dec 2023 01:00:49 GMT
ENV DOCKER_COMPOSE_VERSION=2.23.3
# Wed, 13 Dec 2023 01:00:50 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-windows-x86_64.exe
# Wed, 13 Dec 2023 01:00:50 GMT
ENV DOCKER_COMPOSE_SHA256=7d3f56cc84838ca54c5f0e9c8a3645dd96030482d838663c367d93bc6c38dc05
# Wed, 13 Dec 2023 01:01:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35ae5ad761bfd7e5fb48c234de8722eaa28e17e2c956816fecb417ab6259c29`  
		Last Modified: Tue, 12 Dec 2023 19:14:24 GMT  
		Size: 409.1 MB (409088642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7670bca866ca2eef91a88bf6b39d874f2e27c239e195da98092cc5ae4c095d53`  
		Last Modified: Wed, 13 Dec 2023 01:01:25 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a4948ca1ae1622c815ded81f14743c0d14ba24a2e8f64a6450b8b72c4b14b0`  
		Last Modified: Wed, 13 Dec 2023 01:01:24 GMT  
		Size: 504.4 KB (504409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb46ee1520ba4d9c0e2e182c54bc50ad54a8b30d57d7088197a90ec39d76cfb1`  
		Last Modified: Wed, 13 Dec 2023 01:01:23 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e247407ab936e1619f3237b08040a47ea97c3f8991e85a6249e98de6c2bba54d`  
		Last Modified: Wed, 13 Dec 2023 01:01:23 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c7e24535471585139595b2782c2275e5751dd9727b2f7f76d5a92124ac9786`  
		Last Modified: Wed, 13 Dec 2023 01:01:25 GMT  
		Size: 17.5 MB (17540301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa472eec9f858f943c5c4911e0b1b7728b7b7398bd3d30b62b873ad13987b685`  
		Last Modified: Wed, 13 Dec 2023 01:01:21 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f8e17e7c990901fed51d593a3fd6787f3c2b44417412a7efbcf5f4a3689dc4`  
		Last Modified: Wed, 13 Dec 2023 01:01:21 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87be1ee681368ad9f4cbb066a4ca1639554e55b39c2c80c3f4a8b233440bdbc6`  
		Last Modified: Wed, 13 Dec 2023 01:01:21 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab5f650ab3d9393a600ea86008a110fb7de6c56e175537f3329b619befe2a1b5`  
		Last Modified: Wed, 13 Dec 2023 01:01:21 GMT  
		Size: 18.0 MB (18028823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda3ee6f65ae63f9c39da9d25a691c8db69c826b48e023c54917d2c2c7b12753`  
		Last Modified: Wed, 13 Dec 2023 01:01:19 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779a694adddcf92711649980fa3d48603aebc44161031082114991cb97c7d9be`  
		Last Modified: Wed, 13 Dec 2023 01:01:19 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b511274244ccc762d6c235ec1a00bc64355543cbaea318ee3f1a550d253b640a`  
		Last Modified: Wed, 13 Dec 2023 01:01:19 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f8384991c974a5ab46e2333619fce76eebddd2b2e28513f9a14073a7e53857`  
		Last Modified: Wed, 13 Dec 2023 01:01:22 GMT  
		Size: 18.7 MB (18707332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
