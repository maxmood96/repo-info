## `docker:28-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:cd1cfabacfc7a0d06b1bbf71c5320fa56bc101946b3c6d1a43587a53f615149d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3932; amd64

### `docker:28-windowsservercore-ltsc2022` - windows version 10.0.20348.3932; amd64

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
