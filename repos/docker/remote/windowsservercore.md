## `docker:windowsservercore`

```console
$ docker pull docker@sha256:b2d718da404667736c0a364457acff80adecd679f1fc14b6f1ac0d42d9f8035f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32522; amd64
	-	windows version 10.0.20348.4893; amd64

### `docker:windowsservercore` - windows version 10.0.26100.32522; amd64

```console
$ docker pull docker@sha256:462fb840b379773702d6f2ecf9e38e2af6d419e6f58f49621e2aa04a2b6028f2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2142426790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b41f20483ff521d6005d1200f88e71a4a3121883bdc4efc41be41de5817c9fb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Tue, 10 Mar 2026 21:55:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Mar 2026 21:55:54 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 10 Mar 2026 21:55:55 GMT
ENV DOCKER_VERSION=29.3.0
# Tue, 10 Mar 2026 21:55:55 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.3.0.zip
# Tue, 10 Mar 2026 21:56:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 10 Mar 2026 21:56:06 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Tue, 10 Mar 2026 21:56:06 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.windows-amd64.exe
# Tue, 10 Mar 2026 21:56:07 GMT
ENV DOCKER_BUILDX_SHA256=47d76e47acf3c7611dd594c4b0909fec680ae6406b6fa775f6077b195837e2b9
# Tue, 10 Mar 2026 21:56:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 10 Mar 2026 21:56:16 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Tue, 10 Mar 2026 21:56:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-windows-x86_64.exe
# Tue, 10 Mar 2026 21:56:17 GMT
ENV DOCKER_COMPOSE_SHA256=ee84e42b93c501cb0aa2caa84d76b5f30ca6fb92f070e289fc37be7332c5822a
# Tue, 10 Mar 2026 21:56:25 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344cc8f410d425104b1ea3d4052161da9518d5e7cef041fc41b1dd5444177827`  
		Last Modified: Tue, 10 Mar 2026 21:56:34 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffac95db6729adeb9501b692a859b1f7501da32d0e68396ade09d5ee2b9c5dba`  
		Last Modified: Tue, 10 Mar 2026 21:56:33 GMT  
		Size: 361.9 KB (361934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c9b204a653da45e48dd97cbcdac8a2e635bb3b80df1e34714481a3663228de`  
		Last Modified: Tue, 10 Mar 2026 21:56:32 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372fff353ecb038a8e708b63d30f1dda19e9ad5baf9184e71eda34dc64a2d787`  
		Last Modified: Tue, 10 Mar 2026 21:56:32 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95bed5d701d4789946d12eff7113c47a85c18140e9647ef23b69f7f0507ea9e9`  
		Last Modified: Tue, 10 Mar 2026 21:56:34 GMT  
		Size: 19.6 MB (19588397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4ab9d4622b960434973dde7fc1669e187aa3ac0c02a003136df3a5784c69f5`  
		Last Modified: Tue, 10 Mar 2026 21:56:30 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f52be483434da9210b19b0a17c9522bfb669e169b2a4a816918258210982af`  
		Last Modified: Tue, 10 Mar 2026 21:56:30 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0b144e97fd6cb2e747bf5310bfd63c0a9d551ceeac0a426a64f1179018f3ac`  
		Last Modified: Tue, 10 Mar 2026 21:56:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1d5879885858c7fde574cec42831b5fbf4787dbfa708675e6aef9c9600357c`  
		Last Modified: Tue, 10 Mar 2026 21:56:34 GMT  
		Size: 29.6 MB (29632810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfd0803d374ab92aae91332ec28f8d02e7943509fb1def7bdb2aef06f9646bf9`  
		Last Modified: Tue, 10 Mar 2026 21:56:29 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33599295df3b8bd759f1e034e75f72c6a6b19993a3a4259b0ff9e621bcf317b`  
		Last Modified: Tue, 10 Mar 2026 21:56:29 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ba634617fc170c1f2f6035065dcb3b2f7efca870573f79a1f6694877ecfbac`  
		Last Modified: Tue, 10 Mar 2026 21:56:29 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff425f8aa0d57b01aac79c8c461221b7844a9a0e06916134be6c0af9fef136a7`  
		Last Modified: Tue, 10 Mar 2026 21:56:31 GMT  
		Size: 11.6 MB (11635780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.4893; amd64

```console
$ docker pull docker@sha256:7218b6c6fbe208207908f94f1ed696b4bd01423d2c443586c5f65031c5e0e93e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2043597626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:378ba248bb85f2c6fe57c779e2da6f4c4498116174b27197870a8f9ee1d337d4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 10 Mar 2026 21:55:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Mar 2026 21:55:44 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 10 Mar 2026 21:55:45 GMT
ENV DOCKER_VERSION=29.3.0
# Tue, 10 Mar 2026 21:55:46 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.3.0.zip
# Tue, 10 Mar 2026 21:56:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 10 Mar 2026 21:56:04 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Tue, 10 Mar 2026 21:56:05 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.windows-amd64.exe
# Tue, 10 Mar 2026 21:56:05 GMT
ENV DOCKER_BUILDX_SHA256=47d76e47acf3c7611dd594c4b0909fec680ae6406b6fa775f6077b195837e2b9
# Tue, 10 Mar 2026 21:56:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 10 Mar 2026 21:56:22 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Tue, 10 Mar 2026 21:56:23 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-windows-x86_64.exe
# Tue, 10 Mar 2026 21:56:24 GMT
ENV DOCKER_COMPOSE_SHA256=ee84e42b93c501cb0aa2caa84d76b5f30ca6fb92f070e289fc37be7332c5822a
# Tue, 10 Mar 2026 21:56:34 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d5e3e0ff6e92ce7cae76c8671079083e197ef5ac43484b480278bafe25a4ce`  
		Last Modified: Tue, 10 Mar 2026 21:56:43 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a17a66011dcb9c38eedc922e2d718b0cff4e70ce31e167daaa8dfee148d9c195`  
		Last Modified: Tue, 10 Mar 2026 21:56:42 GMT  
		Size: 486.8 KB (486826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f159d4d5d7e56333bfd6e2e7b16344a0e872adf0b93acebefa53c4247fbc9396`  
		Last Modified: Tue, 10 Mar 2026 21:56:41 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cccb66eda533f994dbbb9ff81d57c851758147e1a0630eea05e16a0716ff87ad`  
		Last Modified: Tue, 10 Mar 2026 21:56:41 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0cd965bfbb200c967e8ee796997bdd4cdb587a833c56d7a49317544aab06cc6`  
		Last Modified: Tue, 10 Mar 2026 21:56:44 GMT  
		Size: 19.6 MB (19571347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0edc8f49358e8d56eb2e56b6ac13be2048a3a016717f24c53f49dc1fc9bde0f7`  
		Last Modified: Tue, 10 Mar 2026 21:56:40 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8ac62b592ebb8bae48e8d31dadb875c021f30a09defc65097fb06249ef2e6a`  
		Last Modified: Tue, 10 Mar 2026 21:56:40 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554c2edbde552817f409d72b85a719f3c34ddc1651c3a110b24b1d3aa4570cc3`  
		Last Modified: Tue, 10 Mar 2026 21:56:40 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90bad317fa3a54913b9758ee2e45f94e02a64cc9e4e0c693589b644de126d33`  
		Last Modified: Tue, 10 Mar 2026 21:56:46 GMT  
		Size: 29.6 MB (29623149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7dbad83ed52d0db02d4f30b2e0a88e026dd56c68a61c0a3a99f4d64bc5b14d1`  
		Last Modified: Tue, 10 Mar 2026 21:56:38 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d05240889a0e152fce0f29182840145e329281d7d52b384e0251bb1a9abfa8`  
		Last Modified: Tue, 10 Mar 2026 21:56:38 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ac67609452a0105c993416f50fb486c0260df99ed76d920c31b1ab2aa344ab`  
		Last Modified: Tue, 10 Mar 2026 21:56:38 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3aff282c60575fe0964ee93b76dd77692c3ed1f6cbeeb91ecb807cfa30421b8`  
		Last Modified: Tue, 10 Mar 2026 21:56:40 GMT  
		Size: 11.6 MB (11623130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
