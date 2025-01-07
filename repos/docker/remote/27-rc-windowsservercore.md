## `docker:27-rc-windowsservercore`

```console
$ docker pull docker@sha256:48c904f5e170ed211543c9b084281b5ff8dbe1fffcf7f0eb30059f82b8282817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `docker:27-rc-windowsservercore` - windows version 10.0.20348.2966; amd64

```console
$ docker pull docker@sha256:f060df9628c987ea789c4df5780c0943df13de795de60711bb97d96b0529a222
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2313174502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79c54349c5113cf4e6163046f713fabab511bacc7b343b6014c159fba49cbe30`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Tue, 24 Dec 2024 21:32:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 24 Dec 2024 21:32:31 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 24 Dec 2024 21:32:32 GMT
ENV DOCKER_VERSION=27.5.0-rc.1
# Tue, 24 Dec 2024 21:32:32 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-27.5.0-rc.1.zip
# Tue, 24 Dec 2024 21:32:44 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 24 Dec 2024 21:32:45 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Tue, 24 Dec 2024 21:32:45 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Tue, 24 Dec 2024 21:32:46 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Tue, 24 Dec 2024 21:32:54 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 24 Dec 2024 21:32:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Tue, 24 Dec 2024 21:32:56 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-windows-x86_64.exe
# Tue, 24 Dec 2024 21:32:56 GMT
ENV DOCKER_COMPOSE_SHA256=5dc7ac86e8d3972c2c68066c6ac370daf0a42b7c8d3338336c9dbde34af06213
# Tue, 24 Dec 2024 21:33:05 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63539bd5606097057aa02c357af9d7a0e1646815b12be20dc8f737692a0f0e3`  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22d3469291cd45bf8e0e73371485a1742ba6f079a8eb2ed0cd0d86ddbfa6122`  
		Size: 344.5 KB (344495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2806a68fc42aa330bf56cb205269fa5babf79accb9b1386be6a9e0fb93119cbb`  
		Last Modified: Tue, 24 Dec 2024 21:33:12 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22666c5dabea757b86076cd5fe26537d5bebbe49a7a79cf89c5ee12643efa9b8`  
		Last Modified: Tue, 24 Dec 2024 21:33:12 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:413691bf0e8f67c1a40025543e4c2d35b542644368a6478293fbed434ecb5d9f`  
		Size: 19.2 MB (19152808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0afb618bebd1ae71a220d6645aba1b28bc34f615b1e3c1d1b95515b127f02cd7`  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef2efc888bd6324dfb7b051550d7efe5480bd2b53a9c5da68fc5c5a86bd7760`  
		Last Modified: Tue, 24 Dec 2024 21:33:11 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e018d4d50ac765f64fd6c45823dff2ba7c53d05bdf53def4650edd17021382`  
		Last Modified: Tue, 24 Dec 2024 21:33:10 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a87787eeb120e7bcc6042c679f7f51cc3c1f290e226d2cae2942f93826f74e97`  
		Size: 19.6 MB (19637964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884da3d04c115b4a1215815cf66e0d0be9480171f497ef11dc2b9abab5d6fa52`  
		Last Modified: Tue, 24 Dec 2024 21:33:09 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38c6d76f55c43dcabade54de45a3b2ac5397beea2b685d25cec730cba2a53c6`  
		Last Modified: Tue, 24 Dec 2024 21:33:09 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7937e1c18b4dbdd128c94ee1e67dbf60e81fb28a163156f31c1e430c2bd2031`  
		Last Modified: Tue, 24 Dec 2024 21:33:09 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4513c6265bdc4a4841cd89793fbc86cbe1d89824943d131fd32064295171fe7f`  
		Last Modified: Tue, 24 Dec 2024 21:33:12 GMT  
		Size: 20.2 MB (20154041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27-rc-windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull docker@sha256:686c30f73587c730321cad9c057971af53a33370b7d8d4286cae294d26ad4ec8
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2073612215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b84832ebdf5b660baa2d76253298957b71d48305b3240d2c38f373daca00d98f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Tue, 24 Dec 2024 21:32:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 24 Dec 2024 21:32:32 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 24 Dec 2024 21:32:33 GMT
ENV DOCKER_VERSION=27.5.0-rc.1
# Tue, 24 Dec 2024 21:32:33 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-27.5.0-rc.1.zip
# Tue, 24 Dec 2024 21:32:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 24 Dec 2024 21:32:51 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Tue, 24 Dec 2024 21:32:51 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Tue, 24 Dec 2024 21:32:52 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Tue, 24 Dec 2024 21:33:11 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 24 Dec 2024 21:33:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Tue, 24 Dec 2024 21:33:12 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-windows-x86_64.exe
# Tue, 24 Dec 2024 21:33:12 GMT
ENV DOCKER_COMPOSE_SHA256=5dc7ac86e8d3972c2c68066c6ac370daf0a42b7c8d3338336c9dbde34af06213
# Tue, 24 Dec 2024 21:33:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf5cc0f04280c4f94e99dc74bca4537c728a2e865602b4c7df0a869b97aa2d8`  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5c018baa4cd08368e4409d9ae0701a563e189edc81adc7468070d83211bcf4`  
		Last Modified: Tue, 24 Dec 2024 21:33:32 GMT  
		Size: 471.9 KB (471890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe5dfa39ceae9ecfc0b85879c1bcb7dca3dd816220ce026c911c0e30fb978d3f`  
		Last Modified: Tue, 24 Dec 2024 21:33:32 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87db596dbd06aa586eae180b90bb0dceb163ef6e953c4e69bf1c89fb2b45631b`  
		Last Modified: Tue, 24 Dec 2024 21:33:31 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6c8e6be11d6c2aa0ea24c4911a23b271b12242b2535e34e162365d65beec9a`  
		Last Modified: Tue, 24 Dec 2024 21:33:33 GMT  
		Size: 19.2 MB (19161495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2a800dea9cd4124557d6b0c02bdd1a09c0c3adf94da5e9aacbec30a070b383`  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d4c0e71b35e0a4cfd400d2243d7b5d1b4e5057a89c8e8078cddaa8a4e78155`  
		Last Modified: Tue, 24 Dec 2024 21:33:31 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc3986b91b8e1d14f961566561f915ae092de47cb2fe551c16efad827743e846`  
		Last Modified: Tue, 24 Dec 2024 21:33:31 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97c32bdf11582062e3ba8903a9933e9bad10302993456a9c6e008239c3130ca`  
		Size: 19.6 MB (19644920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abcde94ac84f47d4747374f206c74626ec3ee839195b361af7c21a5d40566556`  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec3c7da2aea03b09076b099c426ff7c9b535cfa3a03620dc3521cdf8176e70b`  
		Last Modified: Tue, 24 Dec 2024 21:33:30 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf7001b3252d15320448d1fdd6d814bef5bfbc775a2eb7e002331e06c46b8f5`  
		Last Modified: Tue, 24 Dec 2024 21:33:30 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a5d5eab58c6a81afbbfc00aae2929a4b893a3039b9da20e06a640895ab95011`  
		Last Modified: Tue, 24 Dec 2024 21:33:32 GMT  
		Size: 20.2 MB (20152101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
