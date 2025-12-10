## `docker:29-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:f1da8d96a13c6d2f5c2c77394c41baa60cba07f4323fb4c5a10c042d18dc0591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `docker:29-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull docker@sha256:895cf5abcd8b5c61241aba2dd46c1dfd3d0ae29324f35730e0c05a23d6bd0cb9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1835132397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f5a3f08a73b3091edff5dba7b7b84491fdc8c6ea4263706f1af48bde068687`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Tue, 09 Dec 2025 20:29:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 20:29:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Dec 2025 20:29:34 GMT
ENV DOCKER_VERSION=29.1.2
# Tue, 09 Dec 2025 20:29:35 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.2.zip
# Tue, 09 Dec 2025 20:29:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 09 Dec 2025 20:29:48 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 09 Dec 2025 20:29:50 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Tue, 09 Dec 2025 20:29:50 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Tue, 09 Dec 2025 20:30:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 09 Dec 2025 20:30:08 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Tue, 09 Dec 2025 20:30:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-windows-x86_64.exe
# Tue, 09 Dec 2025 20:30:09 GMT
ENV DOCKER_COMPOSE_SHA256=e8a5338e20bc6d30ae38db5533ce63ebf3c229801c20a74051fd06a650e5a8f9
# Tue, 09 Dec 2025 20:30:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dac22ca67391bc67ae059bdc6b4fe7cfa91d0dd9f198a7a4a48d1208814e923`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:043349e15d735002fd555e4be32832770828589a651eae11f6cf3f2d02ad4b4e`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 488.7 KB (488734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236b0fb93b3fcc9496a612d74204ac287360ea57a3a26361271104c86be97334`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea35c40b9971e81debd25b3b9ba90709cdd71ad966066d98d4ef47f7ef1eaa74`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868c903082601f929e25172b2414f102a42725f192ad9fd0edda66b432253e2f`  
		Last Modified: Tue, 09 Dec 2025 20:37:36 GMT  
		Size: 19.4 MB (19412413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3cf58d9086ad644440d4cd0239041b6305aceaeee9f403302a36428940da55`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b32043b05c27d4f3be96d052d081c4c79b08a4d493ba5737e2814bf8698c0d9`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c50ed9458936b4b0976ddb6a0aa490c6a3a101279aa9cf908ea25110d348fd`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f549308f1773171323e5c688a1a6ffb5c50c95638f3ad4d039147527e46a3a8a`  
		Last Modified: Tue, 09 Dec 2025 20:37:36 GMT  
		Size: 23.9 MB (23912184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38406868117ff3519bb0788d7047ec66dfa6834a044d57d8182b6d146b3160e`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd122a724ea56e0e9207b97122512081dd96d6795b3e61063cef71d5a12e001`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:530aa0c39c848502a74b0e0aeea5d02325c53752e036d70f6be87168e64e92ea`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7727d6e218b2e69fbc73769cf1761c3f84c1884e76186c74a315eaf7ac866ba`  
		Last Modified: Tue, 09 Dec 2025 20:37:35 GMT  
		Size: 11.4 MB (11427927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
