## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:c780cf7ac1c5c0cb9599b2df0349dc29186be36aae111d30e399c208f227ae72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull docker@sha256:8b2723933f4e20b03d82fad4f272979c45d21e29d5d5437a257dddd7a19b69e9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2216826173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dad7864511de6cf197875bc99d7c27cee1e5e4a9511cdb529bf075ad6e87eed`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Tue, 18 Mar 2025 17:52:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Mar 2025 17:53:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 18 Mar 2025 17:53:43 GMT
ENV DOCKER_VERSION=28.0.1
# Tue, 18 Mar 2025 17:53:43 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Tue, 18 Mar 2025 17:53:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:53:58 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Tue, 18 Mar 2025 17:53:58 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.windows-amd64.exe
# Tue, 18 Mar 2025 17:53:59 GMT
ENV DOCKER_BUILDX_SHA256=f9ccbfaf42c68e61833f7031e0bdb4b71931cf5ef54d132b39f9faccda02ec7c
# Tue, 18 Mar 2025 17:54:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 18 Mar 2025 17:54:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 18 Mar 2025 17:54:09 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 18 Mar 2025 17:54:10 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 18 Mar 2025 17:54:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7efae6d46cdd88fc96e587336604ae353dae631d3edfb17299749b56f042f86e`  
		Last Modified: Tue, 18 Mar 2025 17:54:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabff009c2b284cea2d40695c1b44d8b2e2b9a499dca58e92884fc4c4139d19b`  
		Last Modified: Tue, 18 Mar 2025 17:54:26 GMT  
		Size: 338.8 KB (338767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299a5346171e96e11bbf7e75d2c923c9e767db919ae268e6303f0a8b51505132`  
		Last Modified: Tue, 18 Mar 2025 17:54:25 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b5681385a5fb68fbaf1d531ba43ef1a4eebca86ff9357c638c2b7ab8722096c`  
		Last Modified: Tue, 18 Mar 2025 17:54:25 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bf621533bae634d522d1baa809d4030a69957056c545455ed8a6b54a582f37`  
		Last Modified: Tue, 18 Mar 2025 17:54:28 GMT  
		Size: 19.8 MB (19814343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59d74b41781047bb821590370c205f708cb1312ac611cf3ffa7d92817cb3385`  
		Last Modified: Tue, 18 Mar 2025 17:54:24 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8fd088b8dce22bb00a6dae4b3c11ff824bc93bbd5375cf39d193367b61b418`  
		Last Modified: Tue, 18 Mar 2025 17:54:24 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c212d22018c8ed56b082699241fba4b6a975dcc80941663d3333e79726ef710`  
		Last Modified: Tue, 18 Mar 2025 17:54:24 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120f89b8213b7712056cc20c3454b43dfbefee8092827722ba2bd7183f6693ea`  
		Last Modified: Tue, 18 Mar 2025 17:54:26 GMT  
		Size: 22.7 MB (22744744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbe59c92ae308cc1ca95460830da582ea729bd502e6fdcc9e91a0980a0cf7f0`  
		Last Modified: Tue, 18 Mar 2025 17:54:23 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24199190c27c55807d7aa76cacb9f25e09fbcbaf0385f92d8088eed73e875917`  
		Last Modified: Tue, 18 Mar 2025 17:54:23 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561f962b02a3d44056e12be508848bc41eb716d98ca72374c1e979fbcd1cf7c7`  
		Last Modified: Tue, 18 Mar 2025 17:54:23 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08ac0a28f0cff7f101228c34c93dbaf640a640f1ee5472053393f4931082d129`  
		Last Modified: Tue, 18 Mar 2025 17:54:26 GMT  
		Size: 22.3 MB (22281907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
