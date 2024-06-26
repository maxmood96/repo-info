## `docker:windowsservercore`

```console
$ docker pull docker@sha256:e34e4dac3fc542f245025b4a723385315b007fcdae0dd7f741084e418ce6e091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2529; amd64
	-	windows version 10.0.17763.5936; amd64

### `docker:windowsservercore` - windows version 10.0.20348.2529; amd64

```console
$ docker pull docker@sha256:5ea11db716ffcae87c1e02027b6f849c0ad83c0dd7cc4adecbfc0bc59f5f37df
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2176365754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c97ded8cfe670ed1c29823ce5a044e6dc662de9ec09dd39a46ce9bca75a06cf`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 19 Jun 2024 19:58:05 GMT
RUN Install update 10.0.20348.2529
# Tue, 25 Jun 2024 22:57:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 25 Jun 2024 22:58:31 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 25 Jun 2024 22:58:32 GMT
ENV DOCKER_VERSION=27.0.1
# Tue, 25 Jun 2024 22:58:34 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.0.1.zip
# Tue, 25 Jun 2024 22:58:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 25 Jun 2024 22:58:56 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Tue, 25 Jun 2024 22:58:57 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.windows-amd64.exe
# Tue, 25 Jun 2024 22:58:58 GMT
ENV DOCKER_BUILDX_SHA256=d28cff3df9fdbb37aa7434edb09d8befe5e90e5ef5887807569b694f25bebd33
# Tue, 25 Jun 2024 22:59:06 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 25 Jun 2024 22:59:07 GMT
ENV DOCKER_COMPOSE_VERSION=2.28.1
# Tue, 25 Jun 2024 22:59:07 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-windows-x86_64.exe
# Tue, 25 Jun 2024 22:59:08 GMT
ENV DOCKER_COMPOSE_SHA256=7dbd8848d9b8dce489c4d2ce1bb4f4b7a3dccb07a08596ae98b85091e1645bcc
# Tue, 25 Jun 2024 22:59:16 GMT
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
	-	`sha256:94f029cccff4cc4d21d33df72b49a94b1e7c1ba3454a1149c76ae3f86b38f6fa`  
		Last Modified: Tue, 25 Jun 2024 22:59:22 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a0f80e286f9f1a917dff91f670da9ee2c1c1edfca97a97fb664c9cde931968`  
		Last Modified: Tue, 25 Jun 2024 22:59:22 GMT  
		Size: 348.2 KB (348213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d9288f7d04f217c555e5e0967e12d2b9913f9c87c6bc30f3243a1fe090451c`  
		Last Modified: Tue, 25 Jun 2024 22:59:21 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4400ef17a95bfe6569125ead9f2843d635a5ada5a8cae78851e50f6140fb73f`  
		Last Modified: Tue, 25 Jun 2024 22:59:21 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d00005f4532d5650406739264b2b64c7d681a46d6c0199d42dd018e22f1e05d4`  
		Last Modified: Tue, 25 Jun 2024 22:59:23 GMT  
		Size: 19.2 MB (19223209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6cd842477070a8075d2ccb25c21b43cea58812ff933641078ab3a1a639c2c59`  
		Last Modified: Tue, 25 Jun 2024 22:59:20 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae56a556b349585ea0fefa2715215bcbd5edf8ff6d2ed98859fea29521d4238`  
		Last Modified: Tue, 25 Jun 2024 22:59:20 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab0fa01d19d279555e762692488c91f5edc0f8b4831eef5a8fd94cccec154c15`  
		Last Modified: Tue, 25 Jun 2024 22:59:19 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4448a305bfbd8971c1b5ad691b820c14bef5a196c7c14b7d5cd946361137c243`  
		Last Modified: Tue, 25 Jun 2024 22:59:22 GMT  
		Size: 19.0 MB (18978332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:530d16eec6da9b6dfa56124112480148243e846b4f8e8dd289b626ae45eed048`  
		Last Modified: Tue, 25 Jun 2024 22:59:19 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e589d5f408855c042260b55a2ef182642385d1f28fc46942bfa622db5e336e`  
		Last Modified: Tue, 25 Jun 2024 22:59:19 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79bd0f23baa17b513b4c8e7589526fe232b7a732c2829edf5d465b9f1a5d293`  
		Last Modified: Tue, 25 Jun 2024 22:59:19 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75aef6bca146b987840c30a0ebccd22c09214aacff1615dddf0adf5dc82d9e74`  
		Last Modified: Tue, 25 Jun 2024 22:59:21 GMT  
		Size: 19.6 MB (19613871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.5936; amd64

```console
$ docker pull docker@sha256:a3c187729e592f34e15972af057857b2fd3aab5a7abf77524600c975927805d7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2279185882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47eecc1bf7a0f64586e7bc2e085f05bab1e7d760c67c72453ff798ec7f9e73b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Tue, 25 Jun 2024 22:56:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 25 Jun 2024 22:59:08 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 25 Jun 2024 22:59:09 GMT
ENV DOCKER_VERSION=27.0.1
# Tue, 25 Jun 2024 22:59:09 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.0.1.zip
# Tue, 25 Jun 2024 22:59:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 25 Jun 2024 22:59:43 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Tue, 25 Jun 2024 22:59:44 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.windows-amd64.exe
# Tue, 25 Jun 2024 22:59:45 GMT
ENV DOCKER_BUILDX_SHA256=d28cff3df9fdbb37aa7434edb09d8befe5e90e5ef5887807569b694f25bebd33
# Tue, 25 Jun 2024 23:00:16 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 25 Jun 2024 23:00:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.28.1
# Tue, 25 Jun 2024 23:00:17 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-windows-x86_64.exe
# Tue, 25 Jun 2024 23:00:18 GMT
ENV DOCKER_COMPOSE_SHA256=7dbd8848d9b8dce489c4d2ce1bb4f4b7a3dccb07a08596ae98b85091e1645bcc
# Tue, 25 Jun 2024 23:00:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff460c2b2669366f8923f4353bc59fa5adffdea3f1e1be5e2281c392d3e0615`  
		Last Modified: Tue, 25 Jun 2024 23:00:50 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b176e08842c74b5955f1f5f997e8d218d262fe2a04a0d59eaa50bf0a44c689`  
		Last Modified: Tue, 25 Jun 2024 23:00:49 GMT  
		Size: 498.0 KB (497974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e8b93b93b9bf37e531a4bef16949fc3dffd3b5e8acc18d1bf7be975c21160d0`  
		Last Modified: Tue, 25 Jun 2024 23:00:48 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:184487007cba88869c94372461267eccbc0392a2495ccb975a5816ba8782e977`  
		Last Modified: Tue, 25 Jun 2024 23:00:48 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a0dfb4bf2d445f1850dcb360d995ca8418e1c54c8e31a3cda465e5abbd7431`  
		Last Modified: Tue, 25 Jun 2024 23:00:50 GMT  
		Size: 19.3 MB (19285325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb94b6fdc63f0b9c0afa2f228689c0bcb4148a1e5239fcac194ef6589748d371`  
		Last Modified: Tue, 25 Jun 2024 23:00:47 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4774034de22ff33a63e0e7b8f60f1dac4f586292bf935fdc1746e69671bd4a78`  
		Last Modified: Tue, 25 Jun 2024 23:00:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c61971f505a2f9c7d94b6112397441d5063548ef0d2eaf2f50b4305ca189f7c`  
		Last Modified: Tue, 25 Jun 2024 23:00:47 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd26eaf38a06a3f4b0cb1f42d64108e203f682c3bf282073c242786386efc9f`  
		Last Modified: Tue, 25 Jun 2024 23:00:48 GMT  
		Size: 19.0 MB (19038241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cd692bf8c7edb058de2d9ba87b47f9c381077af9f025d4d55b9f35bd3df9ad1`  
		Last Modified: Tue, 25 Jun 2024 23:00:46 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67516ba147a8b64a5b38fc5f9aab78b03e412f3039aa856363dd91b305e91bf7`  
		Last Modified: Tue, 25 Jun 2024 23:00:46 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0757dd21f164a200ef9f088d11a0616b4dd8cdc2aab2b740d379521498b6c811`  
		Last Modified: Tue, 25 Jun 2024 23:00:46 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8165af98e1601c148b37271ea4bc4605002c5d4300a7c398937ce6e5dadd16`  
		Last Modified: Tue, 25 Jun 2024 23:00:48 GMT  
		Size: 19.7 MB (19671486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
