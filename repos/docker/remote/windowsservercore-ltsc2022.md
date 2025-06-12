## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:f640af5c3e1bd4c0cb40cf589e9f2f5903fcff110a95226d0c3f09140b3962eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull docker@sha256:53498ccee3c78a70215add9ae3ef737168375a5c54328c792752c0e5fde4eabf
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2345354530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485c313a4ef331fdb3d3de62a8679e0f3981409d24dfa2b371f0d9efb2c3ff07`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Thu, 12 Jun 2025 22:40:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jun 2025 22:40:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 12 Jun 2025 22:40:43 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 12 Jun 2025 22:40:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.2.zip
# Thu, 12 Jun 2025 22:40:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 12 Jun 2025 22:40:54 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 12 Jun 2025 22:40:55 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 12 Jun 2025 22:40:55 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 12 Jun 2025 22:41:04 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 12 Jun 2025 22:41:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 12 Jun 2025 22:41:05 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-windows-x86_64.exe
# Thu, 12 Jun 2025 22:41:06 GMT
ENV DOCKER_COMPOSE_SHA256=132fb31ef7dc81a82d7b1429adf3fd76cc0a7128059af3a172945445a50f2801
# Thu, 12 Jun 2025 22:41:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ce7730719b3563f78c11a86c6e7ca9e7ecab63539d89528367a963b46668ee`  
		Last Modified: Thu, 12 Jun 2025 22:42:44 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa44face37189a26dfbb23b8d5da4e8ec912b0e7403fa7e57fe746ede8ca163`  
		Last Modified: Thu, 12 Jun 2025 22:42:47 GMT  
		Size: 351.9 KB (351892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b288554d751322bcbba469e2992e7ed3d7addecc28b36b87bb0ac57981ad64a`  
		Last Modified: Thu, 12 Jun 2025 22:42:46 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b3bdb645c2944656eeb7ae7bf819f0cd63f9c83b2677298c9c21d710111eec`  
		Last Modified: Thu, 12 Jun 2025 22:42:47 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b59891c80d4b303cd1655e3255818d7a3cb47a43fe98781999d05abb780b0ed`  
		Last Modified: Thu, 12 Jun 2025 22:42:50 GMT  
		Size: 20.5 MB (20450522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1af8f19e40999102aa31f1f4406c7f15eeb18843036b70938f492dee65f6943`  
		Last Modified: Thu, 12 Jun 2025 22:42:49 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f07268cae3a2cdfcdce7a98218844be1e3ede2baa06062288c10119e5414b06`  
		Last Modified: Thu, 12 Jun 2025 22:42:50 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bea31ae088d4884385e4c9bf2ff15ca1ed5f8581b5d17cba15b96224a1533af`  
		Last Modified: Thu, 12 Jun 2025 22:42:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428d152391bf0297baa1308e6b7a51fa8dfb41c8f2dd3071d1d21fa3e4f42d41`  
		Last Modified: Thu, 12 Jun 2025 22:42:54 GMT  
		Size: 22.3 MB (22261181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b28b4c745fe11d31b3e00254bc2bc9aec2a58ab17157f558834f43f95a248ea`  
		Last Modified: Thu, 12 Jun 2025 22:42:54 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa41358ec814cca1a580968a15e80fadcab82f43e7c6b59aea4861acb3c83ad`  
		Last Modified: Thu, 12 Jun 2025 22:42:55 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10bc742c50fda0894e2260bf3f7eb9919c098581d407b6cf2a42e3a41062305b`  
		Last Modified: Thu, 12 Jun 2025 22:42:56 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06dfd207ec226196bd2af1228c11187c3803b22f4c3f4ac01c21d67d7207e67`  
		Last Modified: Thu, 12 Jun 2025 22:42:58 GMT  
		Size: 22.0 MB (22027759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
