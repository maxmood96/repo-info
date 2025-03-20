## `docker:28-windowsservercore-1809`

```console
$ docker pull docker@sha256:7322bffa89bfcbba6b885f3a84c7a8667bebd58d8779f50c989d27b592660c9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `docker:28-windowsservercore-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull docker@sha256:e49f900b7066c7f4479b5463464c2fe598d85021ef7b9f258a37c96c3d3c6b09
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2216876041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb48cac8fcee2a0b499e26f6b75c75829742bad033f5ac2d1e877314a3a0b1a4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Thu, 20 Mar 2025 17:51:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Mar 2025 17:51:44 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 20 Mar 2025 17:51:44 GMT
ENV DOCKER_VERSION=28.0.2
# Thu, 20 Mar 2025 17:51:45 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.2.zip
# Thu, 20 Mar 2025 17:51:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 20 Mar 2025 17:51:58 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 20 Mar 2025 17:51:58 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Thu, 20 Mar 2025 17:51:59 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Thu, 20 Mar 2025 17:52:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 20 Mar 2025 17:52:08 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Thu, 20 Mar 2025 17:52:09 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Thu, 20 Mar 2025 17:52:09 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Thu, 20 Mar 2025 17:52:17 GMT
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
	-	`sha256:8e7b99d15e9d66e78942814ff31f439995704ffae92b370d27447d55ac6880f0`  
		Last Modified: Thu, 20 Mar 2025 17:52:26 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d389c4a21a099d434a7f596bc13b48ea68841b780f6dc22deb1886c4eec2b893`  
		Last Modified: Thu, 20 Mar 2025 17:52:27 GMT  
		Size: 339.3 KB (339301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:284af1da45dc3a354e9e0eba4133cd14bd23eb884ab30f7e5358a0867f9096a9`  
		Last Modified: Thu, 20 Mar 2025 17:52:25 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9ba49508dd2af87af61a794a1f2bfabc7808db2795a8ea6412666f875d8a3ab`  
		Last Modified: Thu, 20 Mar 2025 17:52:25 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc1bfc06cedbe8063d4c05ad59b2d402921391a18eac754c7d175111d3e1de72`  
		Last Modified: Thu, 20 Mar 2025 17:52:27 GMT  
		Size: 19.8 MB (19846955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ee880b2dd8c3f571035d9aac3942ad1bc5744f243f6fb470fdf5d47a0d70db`  
		Last Modified: Thu, 20 Mar 2025 17:52:23 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40f92e1700fa88b5aaef287d762b16cb1b865c6ed4a1c08f92171ef10a9de68`  
		Last Modified: Thu, 20 Mar 2025 17:52:23 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91cb9a42681e4f06f787988a0131a95438d66c5e65feb01f1ea340f4311f4740`  
		Last Modified: Thu, 20 Mar 2025 17:52:23 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d31965ce4136be1befcc849ac48920827cb5a6fd6e9f5a985522f415173d98`  
		Last Modified: Thu, 20 Mar 2025 17:52:24 GMT  
		Size: 22.8 MB (22761381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0605a29fd8e5a8f26bae14a4aced4b49079a501691f86de991f094d608bba8d9`  
		Last Modified: Thu, 20 Mar 2025 17:52:21 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a848037b72a1dff152a4d9c6e27d984f473f13fff71ec199d71e7b4b1be6ea96`  
		Last Modified: Thu, 20 Mar 2025 17:52:21 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dbbfbcbf08ecc39b56b0368b11a6ab984926bfad5a379f5317e698ff47c4f42`  
		Last Modified: Thu, 20 Mar 2025 17:52:21 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff3cce97836547eee20f0170a79a4670aa43aea72711dc88a45870e69f48f886`  
		Last Modified: Thu, 20 Mar 2025 17:52:24 GMT  
		Size: 22.3 MB (22282109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
