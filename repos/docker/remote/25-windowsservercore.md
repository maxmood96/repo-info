## `docker:25-windowsservercore`

```console
$ docker pull docker@sha256:2d6cf13a1839d65e19948b83acb35e4fa6530ba0fdf34e24e0012af9944eb113
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2340; amd64
	-	windows version 10.0.17763.5576; amd64

### `docker:25-windowsservercore` - windows version 10.0.20348.2340; amd64

```console
$ docker pull docker@sha256:c1f0a498f29ceee6c893a1c75f609ada1799d5c5da128da4dc55b60b16989c3a
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2013954479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee7090c276339a885b7d0712e15f176f373c1a699ca15bf485f01516f17558e2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 20 Mar 2024 01:03:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 20 Mar 2024 01:03:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 20 Mar 2024 01:03:14 GMT
ENV DOCKER_VERSION=25.0.5
# Wed, 20 Mar 2024 01:03:14 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-25.0.5.zip
# Wed, 20 Mar 2024 01:03:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 20 Mar 2024 01:03:24 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Wed, 20 Mar 2024 01:03:24 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.windows-amd64.exe
# Wed, 20 Mar 2024 01:03:25 GMT
ENV DOCKER_BUILDX_SHA256=6b113e84cbc3cd645646aa82f00a7f7d3737cc10375b4341e0aca0de0c997c75
# Wed, 20 Mar 2024 01:03:32 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 20 Mar 2024 01:03:33 GMT
ENV DOCKER_COMPOSE_VERSION=2.25.0
# Wed, 20 Mar 2024 01:03:33 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-windows-x86_64.exe
# Wed, 20 Mar 2024 01:03:34 GMT
ENV DOCKER_COMPOSE_SHA256=27289c82fe3ee64eaa415ae47f028f7c6af6ab347f1af4fde0e0d7d2b4a84dbb
# Wed, 20 Mar 2024 01:03:43 GMT
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
	-	`sha256:6376c60b4611f500397f78651c6dd80d12266aad0ab97d88b3d786f11ffc8353`  
		Last Modified: Wed, 20 Mar 2024 01:03:50 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e0337b19f313f7b759ea63ea773186a64743683742f6f57e937d66222ecbc5`  
		Last Modified: Wed, 20 Mar 2024 01:03:50 GMT  
		Size: 497.1 KB (497094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442490a2e1f99aaf586a4fc65c064bce0d1dbb86138a42ddbbaab6712213aa49`  
		Last Modified: Wed, 20 Mar 2024 01:03:49 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a4e208dd2a5c3ffbb84916924767131966d2e52329b277741373ea4cad68585`  
		Last Modified: Wed, 20 Mar 2024 01:03:49 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc1df293c17a277cd75203ab2849053a0eadff700b3d472ba3ff2fcbd919f17`  
		Last Modified: Wed, 20 Mar 2024 01:03:51 GMT  
		Size: 18.1 MB (18073694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81ee6b82b8a37706730a8acb6a4c4a6b1b2bdc2579157734e8ad239e305a60b`  
		Last Modified: Wed, 20 Mar 2024 01:03:48 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4cfe8cf5de038ef11f89919fb6b859c96da4ec3796a7cf341859db1b69207d`  
		Last Modified: Wed, 20 Mar 2024 01:03:48 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a9fda86ab91f66131afd9163d91ed9d8b1c5c8d4c479686884531dfe06945d`  
		Last Modified: Wed, 20 Mar 2024 01:03:48 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f69861dbab9bc3dc770b2cb41b8832db250d7cda8769531bac138840269a82`  
		Last Modified: Wed, 20 Mar 2024 01:03:50 GMT  
		Size: 18.8 MB (18830009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff79c48ff1aa0b56251255763ed7face6e1d25a840b58c669f67cc454d89dcd`  
		Last Modified: Wed, 20 Mar 2024 01:03:47 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19107d8b5f28c3746cfc5233456bc2ff0dbc6e8747ff7db9bf115906b1dbf325`  
		Last Modified: Wed, 20 Mar 2024 01:03:47 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992c2bcae5e462a9b086080dcaed4aed12b3d0afc3b721c646799f9cc82f5b3d`  
		Last Modified: Wed, 20 Mar 2024 01:03:47 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4f7a153722e4f4cac3271f833c47dc7d8507e7588ce94af8090e323e120400`  
		Last Modified: Wed, 20 Mar 2024 01:03:50 GMT  
		Size: 19.1 MB (19082852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:25-windowsservercore` - windows version 10.0.17763.5576; amd64

```console
$ docker pull docker@sha256:5a681c1639cc291bc425b4177a9288e52420d6792edf00a9eb0f48b6050bed55
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2181599392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5473ff741a88aaafe1289b81ba6f10905d6016e81e6b47360a0dfc290620dc2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 20 Mar 2024 00:58:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 20 Mar 2024 00:59:15 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 20 Mar 2024 00:59:16 GMT
ENV DOCKER_VERSION=25.0.5
# Wed, 20 Mar 2024 00:59:16 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-25.0.5.zip
# Wed, 20 Mar 2024 00:59:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 20 Mar 2024 00:59:44 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Wed, 20 Mar 2024 00:59:44 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.windows-amd64.exe
# Wed, 20 Mar 2024 00:59:45 GMT
ENV DOCKER_BUILDX_SHA256=6b113e84cbc3cd645646aa82f00a7f7d3737cc10375b4341e0aca0de0c997c75
# Wed, 20 Mar 2024 01:00:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 20 Mar 2024 01:00:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.25.0
# Wed, 20 Mar 2024 01:00:10 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-windows-x86_64.exe
# Wed, 20 Mar 2024 01:00:11 GMT
ENV DOCKER_COMPOSE_SHA256=27289c82fe3ee64eaa415ae47f028f7c6af6ab347f1af4fde0e0d7d2b4a84dbb
# Wed, 20 Mar 2024 01:00:35 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c3801be3bdcdc80a6dcea9ada6c520e9be6805d1e0a19e405268d55afbb8f8e`  
		Last Modified: Wed, 20 Mar 2024 01:00:46 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436c30a5cc4d5b400d8c1d4384898f845dbaf5e276eef4d06eb02d609039c625`  
		Last Modified: Wed, 20 Mar 2024 01:00:45 GMT  
		Size: 497.4 KB (497432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb9af9d91c8604be4b70f06669aac2febaf2567491bb51b868d800ca474cac0f`  
		Last Modified: Wed, 20 Mar 2024 01:00:44 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6006896737a6cbe88ffa66d35450be1e6ae093d5b4a572b13dc6efc61e781d8b`  
		Last Modified: Wed, 20 Mar 2024 01:00:44 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc612f5fddc52d2631a1d619006d153360c52b4fbe09e1f6ceb4014b1eb549f`  
		Last Modified: Wed, 20 Mar 2024 01:00:46 GMT  
		Size: 18.1 MB (18078964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4b7ae6479ee598555f6fdc27cd770dd5bac3457daa7532dcdbc4f31175e059`  
		Last Modified: Wed, 20 Mar 2024 01:00:42 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151abb70e884987c714b3b87be173d2ba63c14ef3398056c0529726a872e650f`  
		Last Modified: Wed, 20 Mar 2024 01:00:42 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65785d8d6cc725e88fe3fe2d4bef897a07de22bb1215b17e82529947417b77ab`  
		Last Modified: Wed, 20 Mar 2024 01:00:42 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef332b47a9228d8662faa180e2ce2c94cf5356558e43be3e7494e4facdc75139`  
		Last Modified: Wed, 20 Mar 2024 01:00:42 GMT  
		Size: 18.8 MB (18832792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:910256afd3e0123ef26b8522fd3045ae279a839db897283c99ba8f106f574ebc`  
		Last Modified: Wed, 20 Mar 2024 01:00:40 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daed536c4d4dc6f375510a42f3c5a52b52add005cfd76750997a116928a6680b`  
		Last Modified: Wed, 20 Mar 2024 01:00:40 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7eb223946ebf5675520e3d4c9750d7a16012d8f3e8c4289dbe6567a963d11d`  
		Last Modified: Wed, 20 Mar 2024 01:00:40 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008d4bbbc2965ad3f58845787abc326824fa4aa14b5b6c4f7c30ba305f532bd1`  
		Last Modified: Wed, 20 Mar 2024 01:00:43 GMT  
		Size: 19.1 MB (19078611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
