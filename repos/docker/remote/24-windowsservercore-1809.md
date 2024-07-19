## `docker:24-windowsservercore-1809`

```console
$ docker pull docker@sha256:e1f6d3bad4edb48d6bc9c8b5d0c40bc16856dddcee311c83e4580c1f8f3c8f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `docker:24-windowsservercore-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull docker@sha256:a1273d5008740d4a67f7626bf463637124ea88ee97b352c3622431a1f95ff530
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2295468100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e71c67bba223dbf1a001c1cbcb998099fe3bdd09eb8d7a30461e4e2a118d36d9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Fri, 19 Jul 2024 18:06:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 19 Jul 2024 18:06:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 19 Jul 2024 18:06:44 GMT
ENV DOCKER_VERSION=24.0.9
# Fri, 19 Jul 2024 18:06:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.9.zip
# Fri, 19 Jul 2024 18:07:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 19 Jul 2024 18:07:11 GMT
ENV DOCKER_BUILDX_VERSION=0.16.1
# Fri, 19 Jul 2024 18:07:11 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.windows-amd64.exe
# Fri, 19 Jul 2024 18:07:12 GMT
ENV DOCKER_BUILDX_SHA256=34b8bd302364e9df99ebcd86658eae6ade175baf8baf6e74123ae04fcb2675c3
# Fri, 19 Jul 2024 18:07:36 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 19 Jul 2024 18:07:37 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.0
# Fri, 19 Jul 2024 18:07:38 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-windows-x86_64.exe
# Fri, 19 Jul 2024 18:07:38 GMT
ENV DOCKER_COMPOSE_SHA256=3dc98cacf0e0a05d8a714cc729827c062ff7ec13ffcd626e7b3767b362ce9b65
# Fri, 19 Jul 2024 18:08:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f98e7fe87492b83d7775a348ae0c94412b638ab5bba1a80b03c3a547708acd`  
		Last Modified: Tue, 09 Jul 2024 17:23:28 GMT  
		Size: 587.8 MB (587809033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9259d63bdedbd99cfc97390e6e55d6e718187d47be3b25fc0cad2b10e825d115`  
		Last Modified: Fri, 19 Jul 2024 18:08:11 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e82655653a499eab02505f5946b05c45004d343f7ba5fa6fab07113a06a3e74d`  
		Last Modified: Fri, 19 Jul 2024 18:08:11 GMT  
		Size: 499.5 KB (499543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f63e40268623713efa06a8e89e2f6364f4e876e81957a45cbfb17623ec1ac0`  
		Last Modified: Fri, 19 Jul 2024 18:08:10 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02f50b6622e24dc6483505d719aa2314c24959ce4b3e7db0c1d8612f285b36e`  
		Last Modified: Fri, 19 Jul 2024 18:08:10 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95a68b57f115d5040c0339c2ce8952639b28b28c936e73bba94384a891b24e2`  
		Last Modified: Fri, 19 Jul 2024 18:08:11 GMT  
		Size: 17.6 MB (17550809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:404527ec3a06d4f6b97d5c4d1d93da78038cf5ee90d42c652121e780a3c00644`  
		Last Modified: Fri, 19 Jul 2024 18:08:08 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6e17fb73d8e584ad2031259243a4cbe6166c94953cbe027779f131398d34a9`  
		Last Modified: Fri, 19 Jul 2024 18:08:08 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03cdf8495b9a256af475c7b82cf728972991c98ace89bda59715fa147151df3`  
		Last Modified: Fri, 19 Jul 2024 18:08:08 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87933757bafadcb619d402249e7deab3fa89341363f7c4031492695c73f45c08`  
		Last Modified: Fri, 19 Jul 2024 18:08:09 GMT  
		Size: 19.3 MB (19271286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3474550c8ec8f2d22731b0f3b603c622f7a7ad76ba80cc2e46c6f1345f001855`  
		Last Modified: Fri, 19 Jul 2024 18:08:06 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3a5a6590def9fc0b4b2efcc0d862e808359ab15bce531f5f8c50c8ee46a2c94`  
		Last Modified: Fri, 19 Jul 2024 18:08:06 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3de97be46c2b7045211e7329449da698dc2fba90273abce0f611e2b6ee10a8f`  
		Last Modified: Fri, 19 Jul 2024 18:08:06 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4557bd6a4aa1f5ce96631f36309990b7acc1879d78dc05105840af4cf520da21`  
		Last Modified: Fri, 19 Jul 2024 18:08:09 GMT  
		Size: 19.7 MB (19705389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
