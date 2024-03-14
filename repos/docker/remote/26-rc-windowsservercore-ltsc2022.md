## `docker:26-rc-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:d9acf1dd7457778dd2e505f0c59d00eee5286e213bf9579426110a526a8f25dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `docker:26-rc-windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull docker@sha256:a6ad8ae9e11f219ce5403b17e5c19b854f0535bf111897b8dd34553011b701db
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2013956756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93be2f101abfbe5aeb68e1992b81bbee19b716c1e3bae089dcfc24853a78d526`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Thu, 14 Mar 2024 17:57:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Mar 2024 17:57:24 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 14 Mar 2024 17:57:24 GMT
ENV DOCKER_VERSION=26.0.0-rc2
# Thu, 14 Mar 2024 17:57:25 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-26.0.0-rc2.zip
# Thu, 14 Mar 2024 17:57:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 14 Mar 2024 17:57:34 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Thu, 14 Mar 2024 17:57:35 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.windows-amd64.exe
# Thu, 14 Mar 2024 17:57:35 GMT
ENV DOCKER_BUILDX_SHA256=6b113e84cbc3cd645646aa82f00a7f7d3737cc10375b4341e0aca0de0c997c75
# Thu, 14 Mar 2024 17:57:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 14 Mar 2024 17:57:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.7
# Thu, 14 Mar 2024 17:57:44 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-windows-x86_64.exe
# Thu, 14 Mar 2024 17:57:44 GMT
ENV DOCKER_COMPOSE_SHA256=1a5ffa12cff51a65f4e5e8874ed46b0783cfbc8f5ef837f5b9523decf1afd1d0
# Thu, 14 Mar 2024 17:57:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a5f033b4a2f0dd657701163d15da54d3976388e52603d6ea0bf2b2b12295cc7`  
		Last Modified: Thu, 14 Mar 2024 17:58:01 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1cb4b0993a579aec3d8569bc663298410706d341ea2951d6b223616072e41de`  
		Last Modified: Thu, 14 Mar 2024 17:58:00 GMT  
		Size: 489.9 KB (489878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e00cf3f431030a26deef39dd3ed7c29df3a396d6af90bce50b3ab94e97cd17`  
		Last Modified: Thu, 14 Mar 2024 17:57:59 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874dbf50f399ded22bd3705109bd57a3ec05b0fed0855543f382dd27f8e0acf0`  
		Last Modified: Thu, 14 Mar 2024 17:57:59 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c874b1370dba27dd43180dff7b6dfd1b8cb5b041482a74ed7906a27871d49c44`  
		Last Modified: Thu, 14 Mar 2024 17:58:01 GMT  
		Size: 18.1 MB (18093938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ddae5243f8191ea6508b60a70964f38954cadc1c2d885446b0b3957f3004f7`  
		Last Modified: Thu, 14 Mar 2024 17:57:57 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3394c9fa02510fc8bbfa5fbeaaaac51ddfbcafaa7d0f1587e0978a0f7aae32fb`  
		Last Modified: Thu, 14 Mar 2024 17:57:57 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b88b5fe4d36cf47f91066f36b131354335a2dec7c5d13ce2070c4b923f85c25`  
		Last Modified: Thu, 14 Mar 2024 17:57:57 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231357fc64e83e91d1181a475718f8cab10228b1d267e44b7e3932e85d8cc4ef`  
		Last Modified: Thu, 14 Mar 2024 17:58:03 GMT  
		Size: 18.8 MB (18828437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be297b25a223a9a6bf054f1922af88bfd923c8ac80de5117603cb751511964c4`  
		Last Modified: Thu, 14 Mar 2024 17:57:55 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6338d284c39b2932588dc7b778df1d29bd48aa2934810df16a879c1aa4e04ad`  
		Last Modified: Thu, 14 Mar 2024 17:57:55 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8c3cfc99862aecd93a61dec31bd6c3b0f04f5d6b38072cb25aa835dcda9f60`  
		Last Modified: Thu, 14 Mar 2024 17:57:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:204309f9a690bc58df49d92515dc9396180a7542602c3513f574686ab43e4580`  
		Last Modified: Thu, 14 Mar 2024 17:57:58 GMT  
		Size: 19.1 MB (19073916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
