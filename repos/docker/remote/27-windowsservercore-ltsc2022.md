## `docker:27-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:27379678fb59e194cd712ebb0e1c2815c075f491a692d84c185f9c023d3e6807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `docker:27-windowsservercore-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull docker@sha256:c8aa4fe546c608c397c121187d89bc56ea3d9737443405876c1ef9d2acb4b05b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1858142020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4411154f7c2d251f560e0da541ddab796f6fee7a12d0eee01c6bf7bbf3edc6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Mon, 04 Nov 2024 22:03:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 04 Nov 2024 22:04:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 04 Nov 2024 22:04:15 GMT
ENV DOCKER_VERSION=27.3.1
# Mon, 04 Nov 2024 22:04:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Mon, 04 Nov 2024 22:04:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 04 Nov 2024 22:04:28 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Mon, 04 Nov 2024 22:04:29 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Mon, 04 Nov 2024 22:04:30 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Mon, 04 Nov 2024 22:04:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 04 Nov 2024 22:04:40 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Mon, 04 Nov 2024 22:04:41 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-windows-x86_64.exe
# Mon, 04 Nov 2024 22:04:41 GMT
ENV DOCKER_COMPOSE_SHA256=bf29dcf1b35cf226ca0fe337d0de903060ec50855eea5c0eb54739e3c3c3fa5a
# Mon, 04 Nov 2024 22:04:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ee01e199a2f24e8b6b493c7367a13ddfae6bba887e466c01ad020d2524bc5a`  
		Last Modified: Mon, 04 Nov 2024 22:05:01 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e2bbb9fdbcc87bfb4b93de3c0cdae83c335e9f7dbc06d098d192e52bafabe50`  
		Last Modified: Mon, 04 Nov 2024 22:05:00 GMT  
		Size: 492.1 KB (492079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ebbb20ded945183fd4c14656b19cda045f5b7e97bb07f22b9843e50895f43f`  
		Last Modified: Mon, 04 Nov 2024 22:04:59 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f968ccc0dac3674bd61466b0204370379096fb7357ab18f5657b0bd96f2cc72`  
		Last Modified: Mon, 04 Nov 2024 22:04:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1db93b3cff5d285cbe387f545603057efda45b74dd0b03b2994f021ce6e5c871`  
		Last Modified: Mon, 04 Nov 2024 22:05:00 GMT  
		Size: 18.9 MB (18889070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43876228572fd4804ce70ac9c566ac1d193206a3ea2d121a1e830f9d0c0fa73c`  
		Last Modified: Mon, 04 Nov 2024 22:04:57 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602105bafc75282867b0569c543c716118673ba5e5ca0f4e52fd6cfd5d55bd33`  
		Last Modified: Mon, 04 Nov 2024 22:04:57 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a078c599f2a3701b122a8fd2b8924fbeabf9b5dd4ceeee5247bc4eae9b988d6`  
		Last Modified: Mon, 04 Nov 2024 22:04:57 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:864c90fc0fd7fe7cc190db57aee11560a7f3148518ae59c477b9500175aaa116`  
		Last Modified: Mon, 04 Nov 2024 22:04:57 GMT  
		Size: 19.4 MB (19413058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5f8dea2b99b1a1c06346aa7d434e05c39e531fc9a0771a1a42eb7d5b300741`  
		Last Modified: Mon, 04 Nov 2024 22:04:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86fa469fc9ccf873529283ea129bc855ebff8a8fc727cc1a97da3dc40791299d`  
		Last Modified: Mon, 04 Nov 2024 22:04:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65181de9a5a0c56771fd37894a1db0360670b93d58280e39fe9a08e7a9288114`  
		Last Modified: Mon, 04 Nov 2024 22:04:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d4dd212468a9d7f2c6ace60eab51374804cdcd5337f5de1fabf7a928190b55`  
		Last Modified: Mon, 04 Nov 2024 22:04:58 GMT  
		Size: 20.0 MB (19994513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
