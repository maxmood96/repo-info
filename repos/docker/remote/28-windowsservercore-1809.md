## `docker:28-windowsservercore-1809`

```console
$ docker pull docker@sha256:6fed54b785c39f7c584b70ac3c8ff8859e0f3517dcc298ea0f3bebcf7e205572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7136; amd64

### `docker:28-windowsservercore-1809` - windows version 10.0.17763.7136; amd64

```console
$ docker pull docker@sha256:9eea48e8624f5a89b632b349df9a9ef60250b1c5ffa205d3d91cf43c32846ccd
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2227127342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785c3dec269da97ebda3793c1818235279080fd52a121be171f0b57b16ddba27`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Tue, 15 Apr 2025 22:12:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 15 Apr 2025 22:13:23 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 15 Apr 2025 22:13:23 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 15 Apr 2025 22:13:24 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Tue, 15 Apr 2025 22:13:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 15 Apr 2025 22:13:39 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Tue, 15 Apr 2025 22:13:40 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Tue, 15 Apr 2025 22:13:41 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Tue, 15 Apr 2025 22:13:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 15 Apr 2025 22:13:51 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Tue, 15 Apr 2025 22:13:52 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-windows-x86_64.exe
# Tue, 15 Apr 2025 22:13:52 GMT
ENV DOCKER_COMPOSE_SHA256=bca44d55a7e612c53a80092661dd5db05aefb936e1eccd7ce06fdb02be7df3c3
# Tue, 15 Apr 2025 22:14:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75559a6ab4985605769e9345e4dff1b1dcce036c5e3f010989bc5d815bcf22db`  
		Last Modified: Tue, 15 Apr 2025 22:14:10 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bbc5225e1556802cd30f8fd34e34314e3d8b61a8646572689a40d59b303a269`  
		Last Modified: Tue, 15 Apr 2025 22:14:10 GMT  
		Size: 341.5 KB (341494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b5c9f84290e2fafec5927a5d6d17a3a064c93078c593270106ea74ad23ec29a`  
		Last Modified: Tue, 15 Apr 2025 22:14:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46bcf429ac4797944cc945ce64dc94e477c8d14341b6fecaf29b9ccc44180cb2`  
		Last Modified: Tue, 15 Apr 2025 22:14:09 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a44bd61aef7b941f7614c31fb50b8660886b2740bbb23a09d281aef1f08832b`  
		Last Modified: Tue, 15 Apr 2025 22:14:11 GMT  
		Size: 19.9 MB (19860556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25d18acc9d9a4944f4b68e2eb3b2056dc918d4f3155a9de9469b804883c9a870`  
		Last Modified: Tue, 15 Apr 2025 22:14:08 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9fb93169fb4009bfe58fef0cb707780bf6d1452c6b71e4add92e8c230fd923`  
		Last Modified: Tue, 15 Apr 2025 22:14:08 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d2981dd79b2395c71b1f2abf10aa7e31aafcd81b94c306767eb6394e5caf23`  
		Last Modified: Tue, 15 Apr 2025 22:14:08 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a04a74dc2f144ff9e196e62a1c06e6277d5004443ce5b7de37e0d4aaa59a13b`  
		Last Modified: Tue, 15 Apr 2025 22:14:10 GMT  
		Size: 22.4 MB (22354530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d80f4121c811468ee950acee266056e1e05a0e7ed4750dba28b1290f9444c9`  
		Last Modified: Tue, 15 Apr 2025 22:14:07 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86e7151feda14da9b65f7fa4811a3d9f596a3f632eee42ca1a9173930178878`  
		Last Modified: Tue, 15 Apr 2025 22:14:07 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62c931e923807455c87709bcd05a0d7067b18b8f1033c6fc5bb4f1d77c0d98b`  
		Last Modified: Tue, 15 Apr 2025 22:14:07 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a55036ef8e12942d5bc9f5782020380597b798bdec106fbd29daa958030524`  
		Last Modified: Tue, 15 Apr 2025 22:14:10 GMT  
		Size: 21.8 MB (21833195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
