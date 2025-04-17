## `docker:windowsservercore`

```console
$ docker pull docker@sha256:c071f952b670d04748f1b306c70676047e2252ac3415e845409c845cc2218dfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3775; amd64
	-	windows version 10.0.20348.3453; amd64
	-	windows version 10.0.17763.7136; amd64

### `docker:windowsservercore` - windows version 10.0.26100.3775; amd64

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

### `docker:windowsservercore` - windows version 10.0.20348.3453; amd64

```console
$ docker pull docker@sha256:3370619ccd432aa92aeb82db6ceb41fb9a2c1d90694f184b93a7fc013216ebb5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335459929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cca8cf5b8b43e5660f7710c121b54b49ba583c85a4332755a99566e58be7eaa1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 04 Apr 2025 23:10:04 GMT
RUN Install update 10.0.20348.3453
# Thu, 17 Apr 2025 18:31:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Apr 2025 18:31:57 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 17 Apr 2025 18:31:58 GMT
ENV DOCKER_VERSION=28.1.0
# Thu, 17 Apr 2025 18:31:58 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.0.zip
# Thu, 17 Apr 2025 18:32:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 17 Apr 2025 18:32:09 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Thu, 17 Apr 2025 18:32:09 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Thu, 17 Apr 2025 18:32:10 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Thu, 17 Apr 2025 18:32:18 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 17 Apr 2025 18:32:19 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.1
# Thu, 17 Apr 2025 18:32:19 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-windows-x86_64.exe
# Thu, 17 Apr 2025 18:32:20 GMT
ENV DOCKER_COMPOSE_SHA256=971d6000e2c70da19c20f8264330a7ec3962b1fd59601afeb7e3636bad89b8c9
# Thu, 17 Apr 2025 18:32:29 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510f1abe0ffe1466f946291b3ac20345b4a5e2063a896736990eae81bbf4bdb4`  
		Last Modified: Tue, 08 Apr 2025 21:40:38 GMT  
		Size: 808.8 MB (808803243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc89a6e0b1598e68afc46c4fd762c3c143b7a6a9ca6d13a0545ffa90a246ece6`  
		Last Modified: Thu, 17 Apr 2025 18:32:40 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8485b6de0a23c7be2467d19ad4e4fa91efed84ac211a385a2d9ca23b35aac182`  
		Last Modified: Thu, 17 Apr 2025 18:32:40 GMT  
		Size: 356.8 KB (356843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9ec570e402cd6771f41e062d7d6ca5e26a619b405a79f72bad46094c5536a3`  
		Last Modified: Thu, 17 Apr 2025 18:32:38 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6790684ad7f44f4cd7a91c47a082c20b0c61dd73bf5b85d7a07913ce2f59e1`  
		Last Modified: Thu, 17 Apr 2025 18:32:38 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd86cc6b81ae033128634b13be5564efd9a67836627df25014144e0375bcb44c`  
		Last Modified: Thu, 17 Apr 2025 18:32:40 GMT  
		Size: 19.9 MB (19894709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a49df8ff1b3aceb7eb937266ec144177a7c4b15ca730b2aace73a2f877ec0de`  
		Last Modified: Thu, 17 Apr 2025 18:32:36 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d125e395249b5f81e16bc146ee6840da492fba8f927e41b1f206d2035d4e6ed5`  
		Last Modified: Thu, 17 Apr 2025 18:32:36 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf14b8452fee435be72ae6a263ba75779d0ab43227b25ae20c2b1350be6c4c0`  
		Last Modified: Thu, 17 Apr 2025 18:32:36 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89f15f838b08d714375b6eaa88ec21f634148d65d3ae6d2ea6b0b925845f1805`  
		Last Modified: Thu, 17 Apr 2025 18:32:37 GMT  
		Size: 22.4 MB (22356793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e20bc799cec825f36c770a446ab96e28f58f0b88b339e86cc99d120952cbc44`  
		Last Modified: Thu, 17 Apr 2025 18:32:34 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc04d2f01c86a938d99ecb87016458ac9f4e1ea9563110c20f8090e9014be30`  
		Last Modified: Thu, 17 Apr 2025 18:32:34 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd962c7e1905c87ee5b53929dd2d92118bb1fd4d4b2ac3bdb76d71b5a5ac384c`  
		Last Modified: Thu, 17 Apr 2025 18:32:34 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f19e8020d1cd200fcd02d473a39957001a180133e91b18400533a685fd1c4f7`  
		Last Modified: Thu, 17 Apr 2025 18:32:38 GMT  
		Size: 21.8 MB (21844326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.7136; amd64

```console
$ docker pull docker@sha256:bcd74492b1ee68fdde0f87b0a9b6814bbca42d32d967cb11004cbef60d035639
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2227153334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84581e1a23e35c8de3113ff26fd88f62d0e602628c8cd58ee03a62fcdce18467`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Thu, 17 Apr 2025 18:31:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Apr 2025 18:31:23 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 17 Apr 2025 18:31:24 GMT
ENV DOCKER_VERSION=28.1.0
# Thu, 17 Apr 2025 18:31:25 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.0.zip
# Thu, 17 Apr 2025 18:31:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 17 Apr 2025 18:31:36 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Thu, 17 Apr 2025 18:31:36 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Thu, 17 Apr 2025 18:31:37 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Thu, 17 Apr 2025 18:31:46 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 17 Apr 2025 18:31:47 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.1
# Thu, 17 Apr 2025 18:31:47 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-windows-x86_64.exe
# Thu, 17 Apr 2025 18:31:48 GMT
ENV DOCKER_COMPOSE_SHA256=971d6000e2c70da19c20f8264330a7ec3962b1fd59601afeb7e3636bad89b8c9
# Thu, 17 Apr 2025 18:31:57 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c8cec22ad2de983d62030efd24464c141807b9f6915d0f0f5efc19aa3df277d`  
		Last Modified: Thu, 17 Apr 2025 18:32:07 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d12d74cd4516ac985ae33ba8dc133b1a915729ae039411b910e6715ad648b93c`  
		Last Modified: Thu, 17 Apr 2025 18:32:08 GMT  
		Size: 341.1 KB (341132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85b86cb3fe3d947bfa201407687c9bb3a9d16c136bdccfbd4b4eeeedf1ca4372`  
		Last Modified: Thu, 17 Apr 2025 18:32:06 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe0d90993ba40b9e47ad5d80df3ea46df28418a166ecfa7d82e0b54eec172f3`  
		Last Modified: Thu, 17 Apr 2025 18:32:06 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0807b17c9af7ec2cbf1985d0c7d2ebb7236dbf88d473cf6b7bb262767aaff932`  
		Last Modified: Thu, 17 Apr 2025 18:32:08 GMT  
		Size: 19.9 MB (19888760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a68aedb9a34383bbd109bba34dd250efd7e66479dd0a30d54ae4062c13621ce`  
		Last Modified: Thu, 17 Apr 2025 18:32:04 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c4adeebc30daa59f684343fa4f7d21804987d2b8db3b36541228bc6498e5476`  
		Last Modified: Thu, 17 Apr 2025 18:32:04 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba68c46bdba8925c73b8c82b8186cc6d127a63b1fd51d6d973e22d73000b1523`  
		Last Modified: Thu, 17 Apr 2025 18:32:04 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1bdf1948bacdde554adc9c3aeb38278ea4702cd4612d005692793de20ba9fa6`  
		Last Modified: Thu, 17 Apr 2025 18:32:05 GMT  
		Size: 22.4 MB (22352511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3472b294423b0e0183b30f58ac079d5a6e7c4ea3c9a637e255056c4df0d7c7c9`  
		Last Modified: Thu, 17 Apr 2025 18:32:02 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd5db15b65cab065f4aa34f3336bcc535d28afca6bdb58a9735b5e23bd1e0b4`  
		Last Modified: Thu, 17 Apr 2025 18:32:02 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1aeafc6ea386121681e626599a0f5e77d802a162c1a453a8ddc2960c4f8b41`  
		Last Modified: Thu, 17 Apr 2025 18:32:02 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635a22ab2d08567f602e6329c17af8041ec90791331a2a4a31e816234ada1042`  
		Last Modified: Thu, 17 Apr 2025 18:32:05 GMT  
		Size: 21.8 MB (21833454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
