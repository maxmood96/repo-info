## `docker:25-rc-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:8698641a3df78d74b2aaabfe66ebcf7061616d81a1ea7f5afe43d8a23edcdc71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2159; amd64

### `docker:25-rc-windowsservercore-ltsc2022` - windows version 10.0.20348.2159; amd64

```console
$ docker pull docker@sha256:8e3c38693683b86a4fe8b76bec3f9b69a08b11e18dae3c1b3a1cc3efc8a72c9e
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1944555525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6909fe52cfa314e82eebcc380b370101278641f94b558cf3e8d022b6130da683`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 02 Dec 2023 12:42:56 GMT
RUN Install update 10.0.20348.2159
# Fri, 05 Jan 2024 01:53:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 05 Jan 2024 01:54:05 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 05 Jan 2024 01:54:05 GMT
ENV DOCKER_VERSION=25.0.0-rc.1
# Fri, 05 Jan 2024 01:54:06 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-25.0.0-rc.1.zip
# Fri, 05 Jan 2024 01:54:16 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 05 Jan 2024 01:54:17 GMT
ENV DOCKER_BUILDX_VERSION=0.12.0
# Fri, 05 Jan 2024 01:54:17 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.windows-amd64.exe
# Fri, 05 Jan 2024 01:54:18 GMT
ENV DOCKER_BUILDX_SHA256=dcf01329368381fae8c24b494186a30d2f1c4adb4bef7a0410b4803e5bb1c352
# Fri, 05 Jan 2024 01:54:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 05 Jan 2024 01:54:27 GMT
ENV DOCKER_COMPOSE_VERSION=2.23.3
# Fri, 05 Jan 2024 01:54:28 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-windows-x86_64.exe
# Fri, 05 Jan 2024 01:54:29 GMT
ENV DOCKER_COMPOSE_SHA256=7d3f56cc84838ca54c5f0e9c8a3645dd96030482d838663c367d93bc6c38dc05
# Fri, 05 Jan 2024 01:54:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7839fc47f6e056f9e09a214230f8b7115e69419dbc74acbbb1ad6bc0caa28862`  
		Last Modified: Tue, 12 Dec 2023 18:27:40 GMT  
		Size: 500.7 MB (500674814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82e134744414b0e7a2e1b29256a4e28782d16f56fa4e5663d2b4ce8a58998dd3`  
		Last Modified: Fri, 05 Jan 2024 01:54:47 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12156ced78e81b7689d80a13e42395b67e29abd88da95d2f012624d3de027204`  
		Last Modified: Fri, 05 Jan 2024 01:54:47 GMT  
		Size: 492.5 KB (492544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3492eda4d27820ebcb261f48a246c678f627fc25e40698a6a8b1678038caf5`  
		Last Modified: Fri, 05 Jan 2024 01:54:46 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee4d9d55a81e9df51dfdef3eadd97a2d382b4b19f91085ab0d10c1b5b213cfb`  
		Last Modified: Fri, 05 Jan 2024 01:54:46 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48874a07ff6e5b8b6cd0f878b53c18f43285f0f52f56c270e1e30213e2cd53aa`  
		Last Modified: Fri, 05 Jan 2024 01:54:47 GMT  
		Size: 18.1 MB (18060232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8f061006e2fcb90b2f62c0196e539f9f4c5db1c4632babbd2dbe91124085ca`  
		Last Modified: Fri, 05 Jan 2024 01:54:44 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e5879d952cb3122dcf011e71d825906820bbfdb6ed48c049854f00ecba9466`  
		Last Modified: Fri, 05 Jan 2024 01:54:44 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a0e3558c69df0f8e48d280568fceba4f7e1f1b53782b3d1f3e17eabffa73c5`  
		Last Modified: Fri, 05 Jan 2024 01:54:44 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7dff2ef3132cc388161ef39239118cc8b62a184ec8ad0578cae3fcddfd65df`  
		Last Modified: Fri, 05 Jan 2024 01:54:44 GMT  
		Size: 18.0 MB (18016667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3245b5f3009c58abe0944f0682a5787a0585726794c58ac0068b7b083f9a2adc`  
		Last Modified: Fri, 05 Jan 2024 01:54:42 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6efcd69a25f0fb305102ce04b499366e8ac3e3a26491675d2b6b97c5e7b179f8`  
		Last Modified: Fri, 05 Jan 2024 01:54:42 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58a7046d87ecaf1af4569f41cca67d81a9e5e65b22cb5ca923e36fa8e3d96572`  
		Last Modified: Fri, 05 Jan 2024 01:54:42 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3a085f9bdc92a23682f445d1e8255290f707431c6d159034682d4cf4583cdc`  
		Last Modified: Fri, 05 Jan 2024 01:54:45 GMT  
		Size: 18.7 MB (18700876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
