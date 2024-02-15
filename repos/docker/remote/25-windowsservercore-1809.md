## `docker:25-windowsservercore-1809`

```console
$ docker pull docker@sha256:dbf3380fb411aefba96073598eaa949e6089d3a8483a08859f573766ba5cf085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `docker:25-windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull docker@sha256:68e9ebccaeda21011e5a7c4f6985f9fab0821c1685d1fd49d74cc59e9571c2a5
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2136090772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6be8e277bc144866bcccb697b2b94b35f2b43ceedd68c1ffec9700a6f7a008f6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 19:59:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 20:00:31 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 14 Feb 2024 20:00:32 GMT
ENV DOCKER_VERSION=25.0.3
# Wed, 14 Feb 2024 20:00:32 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-25.0.3.zip
# Wed, 14 Feb 2024 20:00:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 20:01:00 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Wed, 14 Feb 2024 20:01:00 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.windows-amd64.exe
# Wed, 14 Feb 2024 20:01:01 GMT
ENV DOCKER_BUILDX_SHA256=0ff0853a09960ff8f454d5db7253d5d935f5538856ea4985a276cbd1b28a96a5
# Wed, 14 Feb 2024 20:01:24 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 20:01:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.5
# Wed, 14 Feb 2024 20:01:25 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.24.5/docker-compose-windows-x86_64.exe
# Wed, 14 Feb 2024 20:01:26 GMT
ENV DOCKER_COMPOSE_SHA256=eb60363d21a5c85eff2d2e18a4ed94d84d5016be59471d77d520046fdd888aa9
# Wed, 14 Feb 2024 20:01:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b30df4cb0bea084a4dc6dda930c0ed7ef8ff45e9f921923b1e5a6111152651`  
		Last Modified: Wed, 14 Feb 2024 20:01:57 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90816fb6e4eff364fdf13d72d39a9ff562f014eff14abc1e778cc1c3f08e997e`  
		Last Modified: Wed, 14 Feb 2024 20:01:57 GMT  
		Size: 493.1 KB (493073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68776fc505376ef3d7a31661b42033244aef864c845c45c12ab12b299f21e8d5`  
		Last Modified: Wed, 14 Feb 2024 20:01:56 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1e0d8b97fd7e02b8944e4ea0718c410ad41caf523bf15b07b09ab2ab71334c8`  
		Last Modified: Wed, 14 Feb 2024 20:01:56 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652e425a669bc6109dc2dca070e7c214696e9c38d466b4f5b9b39a587e879cce`  
		Last Modified: Wed, 14 Feb 2024 20:01:57 GMT  
		Size: 18.1 MB (18071166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:886751e16db60734887a86ed7c6b93314a60ab147d70ed29f5624137688b01d3`  
		Last Modified: Wed, 14 Feb 2024 20:01:55 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91cd5b413921b9f50024d26213f7208b5fa7cae1eda270e3b004d7145e4f1b62`  
		Last Modified: Wed, 14 Feb 2024 20:01:54 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6438e3f590a14464a3a659441059ad8f938719ebc5d53db2c9c85bfa2632a7f4`  
		Last Modified: Wed, 14 Feb 2024 20:01:54 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:374430723c4883e114be34a6f9bb15ecf34f060643643bcc4b97b7a99d47d28a`  
		Last Modified: Wed, 14 Feb 2024 20:01:56 GMT  
		Size: 18.0 MB (18019900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4776c4c17f9727a1f0433af3689ffe9bda0afcf3c125233a608b231bb853a425`  
		Last Modified: Wed, 14 Feb 2024 20:01:53 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ec23ed4bc845cc6e0eb18bc0244d1cc80d9b618f65518c7f38a51a2e66a558`  
		Last Modified: Wed, 14 Feb 2024 20:01:53 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b16e889fc5ecabb1f544cee6ff9b6db4d2af1ea38fe51fda71008abdbfa1db`  
		Last Modified: Wed, 14 Feb 2024 20:01:53 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f525f7dcb63e0d9a2b455dce4e8c38074553990f8f205a4c9daf47ab88350b`  
		Last Modified: Wed, 14 Feb 2024 20:01:56 GMT  
		Size: 19.0 MB (19046204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
