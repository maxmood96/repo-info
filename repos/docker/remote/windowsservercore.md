## `docker:windowsservercore`

```console
$ docker pull docker@sha256:9be998e6d9dfe5dee63ac07fb88b973b9b1876c3d5f62201609688166ea0a196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4652; amd64
	-	windows version 10.0.20348.3932; amd64

### `docker:windowsservercore` - windows version 10.0.26100.4652; amd64

```console
$ docker pull docker@sha256:cd049096238aa699bc8f8956eb548adc22ec038f62153dc52d1c2548cfd09c0f
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3557293437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:074acd2cc26f4024ce5ba9def74466228bc2b00196af8e20f33d09f9c46ce5da`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 05 Jul 2025 18:40:54 GMT
RUN Install update 10.0.26100.4652
# Wed, 09 Jul 2025 18:08:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jul 2025 18:09:06 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Jul 2025 18:09:07 GMT
ENV DOCKER_VERSION=28.3.1
# Wed, 09 Jul 2025 18:09:08 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.1.zip
# Wed, 09 Jul 2025 18:09:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 09 Jul 2025 18:09:21 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 18:09:22 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Wed, 09 Jul 2025 18:09:23 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Wed, 09 Jul 2025 18:09:33 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 09 Jul 2025 18:09:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 18:09:35 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-windows-x86_64.exe
# Wed, 09 Jul 2025 18:09:37 GMT
ENV DOCKER_COMPOSE_SHA256=ba8f09d3873f7a9755b863ed2013a1276b96fcbbc074c69ff3d3cfbce3e0186f
# Wed, 09 Jul 2025 18:09:46 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ebc78effce2335b8fe04c34f5f1f3e33e513d5a7831fa81718af6737b3d654`  
		Last Modified: Wed, 09 Jul 2025 19:09:08 GMT  
		Size: 1.3 GB (1275866158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2400277aa5a9a9f6a50930d2286f810d84d4849672ba018a5261219c74813386`  
		Last Modified: Wed, 09 Jul 2025 20:07:32 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ba8713d6e9298684036d73d3a3009914a2d4b05c2565531b8c83608cc7b6e1`  
		Last Modified: Wed, 09 Jul 2025 20:07:32 GMT  
		Size: 368.1 KB (368055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67753642cb243e41f157fb4b098e83d39607cffc35afa91677ca803e52d864b`  
		Last Modified: Wed, 09 Jul 2025 20:07:32 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b402e09e54c2892c41d9f1cdf4d6238c72c2f5e283cb06d0f201efc494ef6c7a`  
		Last Modified: Wed, 09 Jul 2025 20:07:32 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca2d0126c870f8ed3f106568b81feedad7e42b16aed02ecdef2de275d56d90f`  
		Last Modified: Wed, 09 Jul 2025 20:07:37 GMT  
		Size: 20.8 MB (20838738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8ec28bfbf4492a67248f82d1f6c4fb32e95aa9afe0222875f60c20c9d4d87e`  
		Last Modified: Wed, 09 Jul 2025 20:07:32 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe8ee61b1ad37122b3c4fe71fd6dc55d8885c79964418557b3885aaedded7ce`  
		Last Modified: Wed, 09 Jul 2025 20:07:32 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aab439fc7dc4475e04846f7078ff45e1dc56a2a4a0f02d87681174ede800c5f`  
		Last Modified: Wed, 09 Jul 2025 20:07:33 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198d080ec4e5fe9f371062d85bd32b5b279f5aea87efff5b580418cd24ed6512`  
		Last Modified: Wed, 09 Jul 2025 20:07:38 GMT  
		Size: 22.7 MB (22666832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96cbd90c78b678be68b0cef5b4a06a2dc7acd7cdcc17ac3a1cf03f4ca6912a0e`  
		Last Modified: Wed, 09 Jul 2025 20:07:35 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4d9cfd5c615842072ccc91bf8007c105fc5f12726e89a54f2e334c82c294a0`  
		Last Modified: Wed, 09 Jul 2025 20:07:35 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab8de79b7e70bbdc6e4dab949d52fc6e9c9c5d9ca16f983d803c1574d3a87e2e`  
		Last Modified: Wed, 09 Jul 2025 20:07:35 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bb364e9bfdfdfcd6bda3146d47f3c8d8d7ffcd2cdcf5e64384c786ac9fcb26`  
		Last Modified: Wed, 09 Jul 2025 20:07:40 GMT  
		Size: 22.2 MB (22234671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.3932; amd64

```console
$ docker pull docker@sha256:f471c03e1a4385b005b4b212bb95c8cc39064406b00e58b5be71820fe6f9e6c4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346645145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:309de51c13e50fa47b3a70f3cf20f81113bfa635be7a4d0191458e082699903c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 05 Jul 2025 05:31:06 GMT
RUN Install update 10.0.20348.3932
# Wed, 09 Jul 2025 18:06:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jul 2025 18:06:20 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Jul 2025 18:06:21 GMT
ENV DOCKER_VERSION=28.3.1
# Wed, 09 Jul 2025 18:06:22 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.1.zip
# Wed, 09 Jul 2025 18:06:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 09 Jul 2025 18:06:32 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 18:06:33 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Wed, 09 Jul 2025 18:06:33 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Wed, 09 Jul 2025 18:06:42 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 09 Jul 2025 18:06:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 18:06:44 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-windows-x86_64.exe
# Wed, 09 Jul 2025 18:06:45 GMT
ENV DOCKER_COMPOSE_SHA256=ba8f09d3873f7a9755b863ed2013a1276b96fcbbc074c69ff3d3cfbce3e0186f
# Wed, 09 Jul 2025 18:06:53 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b829944a73d1d8ad37eaa13c64bf9189b6895cc5b45b79bb3563fa325d94b6a7`  
		Last Modified: Wed, 09 Jul 2025 00:17:04 GMT  
		Size: 818.4 MB (818411069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:504990a3a2e27e9956e063855fad8aca8c7d18f3b80d30a9a48a95513380af37`  
		Last Modified: Wed, 09 Jul 2025 20:07:31 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03713561473e7a81c8467c28e8428499669e58e36534f02923c98539af0c18f`  
		Last Modified: Wed, 09 Jul 2025 20:07:31 GMT  
		Size: 350.2 KB (350197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e849e0dd5106b0b57ebd32e89550ec78444cb8016001bbaa6fcbef6a80c689f5`  
		Last Modified: Wed, 09 Jul 2025 20:07:31 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78bf734f391373dbebb12237b09d859275af0298ed390f919931b3b41e065a16`  
		Last Modified: Wed, 09 Jul 2025 20:07:31 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a83d75351372ad4c97e1ee509b27a0c32b51c2a67e67a13c8eb505104fff6a`  
		Last Modified: Wed, 09 Jul 2025 20:07:35 GMT  
		Size: 20.8 MB (20822350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4ea888ad5e21df6793cff22ea3bb097c74aac6abfbce727e00d2a4da63cdaa`  
		Last Modified: Wed, 09 Jul 2025 20:07:32 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64bbd295d1ddb3bf70c450d619100f5b0a378a1d7c31b6605261809a61ec22a`  
		Last Modified: Wed, 09 Jul 2025 20:07:32 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fd2cca3d2fc91d9f9acd1a59c274f72a6f9a0613f9bede2ff7bb7a6672479df`  
		Last Modified: Wed, 09 Jul 2025 20:07:32 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6054fdd01401787ce8f5ce2a67098b5bf46a13aef265961f3226302fd68aad44`  
		Last Modified: Wed, 09 Jul 2025 20:07:35 GMT  
		Size: 22.6 MB (22646856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b626f0733b76ac0b5f695e4ae7e18645489dea4e61b050d314007ed08d44021b`  
		Last Modified: Wed, 09 Jul 2025 20:07:32 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566ec2fe2a328f4272c0f4754da783b872db3d696e5a8b1629ae28c77efc8fca`  
		Last Modified: Wed, 09 Jul 2025 20:07:33 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd471695febb68305655a1cd8adc6c7202f87344c4c401a04f54c289f7da1d1`  
		Last Modified: Wed, 09 Jul 2025 20:07:33 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8656c07858d3337cd8ea3ad0a79dd45527ac99847d5f839e0c80a8065dfd8d32`  
		Last Modified: Wed, 09 Jul 2025 20:07:36 GMT  
		Size: 22.2 MB (22210704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
