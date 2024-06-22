## `docker:25-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:055561b69382da8cd648670fe6525a93bdbfa840ce78711b78423f8840daa2a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2529; amd64

### `docker:25-windowsservercore-ltsc2022` - windows version 10.0.20348.2529; amd64

```console
$ docker pull docker@sha256:40decea9b286b28dae320dca2f78d101e6721df5fbe7212805a828dc96cbcbb4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2175241343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:641ad20f9aade6b1902414bdfb50bd7e4dd5541ed4d56ecf2ff7c45818cf8c65`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 19 Jun 2024 19:58:05 GMT
RUN Install update 10.0.20348.2529
# Fri, 21 Jun 2024 23:59:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 21 Jun 2024 23:59:39 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 21 Jun 2024 23:59:39 GMT
ENV DOCKER_VERSION=25.0.5
# Fri, 21 Jun 2024 23:59:40 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-25.0.5.zip
# Fri, 21 Jun 2024 23:59:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 21 Jun 2024 23:59:48 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Fri, 21 Jun 2024 23:59:49 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.windows-amd64.exe
# Fri, 21 Jun 2024 23:59:50 GMT
ENV DOCKER_BUILDX_SHA256=d28cff3df9fdbb37aa7434edb09d8befe5e90e5ef5887807569b694f25bebd33
# Fri, 21 Jun 2024 23:59:57 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 21 Jun 2024 23:59:58 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.2
# Fri, 21 Jun 2024 23:59:58 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-windows-x86_64.exe
# Fri, 21 Jun 2024 23:59:59 GMT
ENV DOCKER_COMPOSE_SHA256=b9878421deeff63bb4685a0ee502fc737429123f68ee40de326cdc9fab800c1d
# Sat, 22 Jun 2024 00:00:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb373ec9afdfc5f09b9380d981e0c61f9c7b48537b887135c7c66810086e705e`  
		Last Modified: Fri, 21 Jun 2024 00:27:54 GMT  
		Size: 729.6 MB (729591500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9956944399135c0677e0584678272e758364c1cf2bb48a2eaa0ae9e2d8d55b07`  
		Last Modified: Sat, 22 Jun 2024 00:00:17 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07dba477c61e7349e92d91cc3efa92c5969296074eb135649b99e94a54038b28`  
		Last Modified: Sat, 22 Jun 2024 00:00:16 GMT  
		Size: 346.3 KB (346336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb1b9103466eb78152ac835c1630b1f9861e1392c71d8610520c0d37a036ee2`  
		Last Modified: Sat, 22 Jun 2024 00:00:16 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b125058c4b4b967ccaf95d4ef8a9e076e75914e9ff7ed81137b6428ec6e2e5`  
		Last Modified: Sat, 22 Jun 2024 00:00:15 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2796e88cdee1bcd8d2f553cd9b80b69436c01f0044a65de93a5e4f138a63e98a`  
		Last Modified: Sat, 22 Jun 2024 00:00:17 GMT  
		Size: 18.1 MB (18060086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6763f1f6cacefc2fe53172e493b84b0540511ad0b2ffb63f45f78c52e2245545`  
		Last Modified: Sat, 22 Jun 2024 00:00:13 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6041188cd5ce5a9fb5f71f7ec5170e1356dc74f08746100a9d20a0d15d0e9fa8`  
		Last Modified: Sat, 22 Jun 2024 00:00:13 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e0d9aa963b30d3a6d0197f69132f925c67d7bfde40b3c50159f17ecd1b19eb`  
		Last Modified: Sat, 22 Jun 2024 00:00:13 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d93efff431461ffebdeb4dd3a1494cddb66e04dc9899f9ba2bc11eb2cf85c095`  
		Last Modified: Sat, 22 Jun 2024 00:00:14 GMT  
		Size: 19.0 MB (19011879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe451552f4ff932fafce3ddc544d912a77fe6b212836e2286b83f8dd31530427`  
		Last Modified: Sat, 22 Jun 2024 00:00:11 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:851d8b6e183ebf779bd0902cf08f76ec344df38b62916ccf153a3eba661175f1`  
		Last Modified: Sat, 22 Jun 2024 00:00:11 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8e0b4bea6fa39cf405c653ec5cca35ad7def303233500de2cd289f098f634b`  
		Last Modified: Sat, 22 Jun 2024 00:00:11 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956f68e01a9876796586ac5f0ea79fbc1e65d1ee3c4ce38d5be83d0fc953ecc9`  
		Last Modified: Sat, 22 Jun 2024 00:00:14 GMT  
		Size: 19.6 MB (19621214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
