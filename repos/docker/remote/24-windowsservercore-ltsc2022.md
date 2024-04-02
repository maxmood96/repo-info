## `docker:24-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:f3e9fd5b446243a5eebd6e36cb5cd73fa6da0586bc17e2e6d9b01abbc6758450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `docker:24-windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull docker@sha256:f11765625090dcd6879c675befbb6f8552b17e8446bd5aecb89361f733b14391
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2013776059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12d386c1f1695c6805cd70a4a3cbc7b0272e3055033a297fde1273333c8bfb8e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Mon, 01 Apr 2024 23:49:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 01 Apr 2024 23:50:49 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 01 Apr 2024 23:50:51 GMT
ENV DOCKER_VERSION=24.0.9
# Mon, 01 Apr 2024 23:50:52 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.9.zip
# Mon, 01 Apr 2024 23:51:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 01 Apr 2024 23:51:08 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Mon, 01 Apr 2024 23:51:09 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.windows-amd64.exe
# Mon, 01 Apr 2024 23:51:10 GMT
ENV DOCKER_BUILDX_SHA256=6b113e84cbc3cd645646aa82f00a7f7d3737cc10375b4341e0aca0de0c997c75
# Mon, 01 Apr 2024 23:51:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 01 Apr 2024 23:51:21 GMT
ENV DOCKER_COMPOSE_VERSION=2.26.1
# Mon, 01 Apr 2024 23:51:22 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-windows-x86_64.exe
# Mon, 01 Apr 2024 23:51:23 GMT
ENV DOCKER_COMPOSE_SHA256=d8a386d375ef26a77be0bee97516b0287d93acafb3976806f42e2b76c6904125
# Mon, 01 Apr 2024 23:51:36 GMT
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
	-	`sha256:224b791f59147470f32d1ebeb0869e4742cd9203ffdefec38054d0f368dc8069`  
		Last Modified: Mon, 01 Apr 2024 23:51:47 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6936e96ecaa0053a8770205e2bfedc4f8382018d6fae784ac2491ac6754393f4`  
		Last Modified: Mon, 01 Apr 2024 23:51:47 GMT  
		Size: 502.6 KB (502600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbac7a9a63c83a44ec36da54daa8566d3520ea2f6f62ec3d87efd0cd5ac0f70`  
		Last Modified: Mon, 01 Apr 2024 23:51:46 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c486ff2e7edc42719e4dbc94cdf674b53f34eb54eeadcf0a719a407618ce9c`  
		Last Modified: Mon, 01 Apr 2024 23:51:46 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ceae6a8f600794f2b478048a88d62a4e94f4a9251e0d0f90ec90ce606222836`  
		Last Modified: Mon, 01 Apr 2024 23:51:47 GMT  
		Size: 17.5 MB (17502905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28dec4b63f6f87dc1618561874ff5cc5877531636b95033c97bc18a7cf91fbb4`  
		Last Modified: Mon, 01 Apr 2024 23:51:44 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8ffcd161c81d4ea13cf9c8bd30116483cf148e4cd8327ffcf6fe8cf206f175`  
		Last Modified: Mon, 01 Apr 2024 23:51:44 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d85e35dcf2c3c98b40bb331ef082ed729197402429aa5a573d45de13e992f6d3`  
		Last Modified: Mon, 01 Apr 2024 23:51:44 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b26b571937491adefaad77b0d265e669e89589676403f798463f962657f33313`  
		Last Modified: Mon, 01 Apr 2024 23:51:44 GMT  
		Size: 18.8 MB (18797704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe29f676429e41d5332e963cca7ece1c8a1548efb46ea22c47dbe243bfa7496`  
		Last Modified: Mon, 01 Apr 2024 23:51:41 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eb6042fbbb3558a4fe894414ac7332fb4f239ffa7831f8863daae64f5e45662`  
		Last Modified: Mon, 01 Apr 2024 23:51:41 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f6a2d335027318596a61b5f1711deead5b8bd552f308af54cfde3d571025e9`  
		Last Modified: Mon, 01 Apr 2024 23:51:41 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c22e0dd18e6c85ac63c15104bb68e60c623e472a47bec9d903e7d0e887a620a3`  
		Last Modified: Mon, 01 Apr 2024 23:51:44 GMT  
		Size: 19.5 MB (19502180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
