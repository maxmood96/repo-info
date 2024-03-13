## `docker:24-windowsservercore-1809`

```console
$ docker pull docker@sha256:b54a294942ea8a00738a2ff541eb4daa904faf1b8f9b6587d64d13359d5a7db0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `docker:24-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull docker@sha256:a311e6d249b633d4e8e3cc1ba85aeeae57b477d1866387a2b45986b69b7e0da2
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2181082704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c10a38b2ad24870ca9b25cd082463a501f604200181aaeb1a2cd3e9fb04eb6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:06:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 00:07:31 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Mar 2024 00:07:32 GMT
ENV DOCKER_VERSION=24.0.9
# Wed, 13 Mar 2024 00:07:33 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.9.zip
# Wed, 13 Mar 2024 00:08:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 00:08:05 GMT
ENV DOCKER_BUILDX_VERSION=0.13.0
# Wed, 13 Mar 2024 00:08:05 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.windows-amd64.exe
# Wed, 13 Mar 2024 00:08:06 GMT
ENV DOCKER_BUILDX_SHA256=001dd8c707862d7c7a7bc17ebb024922ee304bddad1bca11da5b3b3ff18effa6
# Wed, 13 Mar 2024 00:08:36 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 00:08:36 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.7
# Wed, 13 Mar 2024 00:08:38 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-windows-x86_64.exe
# Wed, 13 Mar 2024 00:08:38 GMT
ENV DOCKER_COMPOSE_SHA256=1a5ffa12cff51a65f4e5e8874ed46b0783cfbc8f5ef837f5b9523decf1afd1d0
# Wed, 13 Mar 2024 00:09:08 GMT
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
	-	`sha256:f0083a5ae015549160983bb1b57d10eddc594209ab762bad4e7c23ca43e615e5`  
		Last Modified: Wed, 13 Mar 2024 00:09:17 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f1133407603ce24d161be642cd96ece0498cbe5f7e551fb544d219cd8fd3885`  
		Last Modified: Wed, 13 Mar 2024 00:09:17 GMT  
		Size: 497.6 KB (497621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08ad2b843e4e0b3088b35d05e9cc02a00d00bcadb870dfd5fe227a3131f70690`  
		Last Modified: Wed, 13 Mar 2024 00:09:16 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4e9c662741340ed36fe14800d8b2b1fdb05547671fd07e56328a38121ab04e`  
		Last Modified: Wed, 13 Mar 2024 00:09:17 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170fc62efb380fe2454a18cb77f2266246fc19e95dbc547819b3121d1e260bc4`  
		Last Modified: Wed, 13 Mar 2024 00:09:18 GMT  
		Size: 17.5 MB (17548497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d2e2c190961a8239894d6bd1ce12d82cbbfa71323f4220c7182c2dce994fd4`  
		Last Modified: Wed, 13 Mar 2024 00:09:15 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbceb25847d27bbc4569124790294a5497a01b369ea3d7293feecd801ceccedb`  
		Last Modified: Wed, 13 Mar 2024 00:09:14 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5437c13dd592a5b9f3d42d5305a03fbcc921b27472566ddb6be25d73ae1ba5e`  
		Last Modified: Wed, 13 Mar 2024 00:09:14 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb120aef3ebe1e89bdbc19f2ec513ee3dd9e2a18a34d2445af012c534bccdb01`  
		Last Modified: Wed, 13 Mar 2024 00:09:15 GMT  
		Size: 18.8 MB (18838961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc55e5f6dbcc1a6a6aa9edc5e9fac61987938e62beede34d29c68f62242c7fc`  
		Last Modified: Wed, 13 Mar 2024 00:09:12 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47eb383237dfbc9beb195c7050425598f656be6624a6ed1f83846b75feb2ac5a`  
		Last Modified: Wed, 13 Mar 2024 00:09:12 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7024fa7531541ac77871a5bcc418a7593d70186d521f841631b54503522d1ab0`  
		Last Modified: Wed, 13 Mar 2024 00:09:12 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a58653ff4a512dd72abd5737d46bc836e9829d3e7f302f3daacc0055d32134`  
		Last Modified: Wed, 13 Mar 2024 00:09:15 GMT  
		Size: 19.1 MB (19086045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
