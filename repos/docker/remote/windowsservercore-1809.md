## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:8b5e611771751fe8360ccf0f5bb3b6c022a079599c9e8dada6351d3682c645b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull docker@sha256:575fd688c3bf866a95546fe93e2564fea753d26e5931ebfc1e32ebd9bc411358
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2201693889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47afabbd0d9bf289e87beda973d92a82859b49c2b2f83325e44032f22df554d7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Sat, 22 Feb 2025 00:36:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 22 Feb 2025 00:37:03 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 22 Feb 2025 00:37:04 GMT
ENV DOCKER_VERSION=28.0.0
# Sat, 22 Feb 2025 00:37:05 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Sat, 22 Feb 2025 00:37:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:37:18 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Sat, 22 Feb 2025 00:37:18 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.windows-amd64.exe
# Sat, 22 Feb 2025 00:37:19 GMT
ENV DOCKER_BUILDX_SHA256=ab3eba3acbfa6b6612690af075795254f29762efc8abace5f636b8e7628b1851
# Sat, 22 Feb 2025 00:37:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:37:29 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Sat, 22 Feb 2025 00:37:30 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Sat, 22 Feb 2025 00:37:31 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Sat, 22 Feb 2025 00:37:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d662e474d0eebcc45d26c962c3ea2815d5ad421c4abce3dfca970d20d34206`  
		Last Modified: Sat, 22 Feb 2025 00:37:45 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80c05d72492cc29e69146de42b5cbab7c6912ef3a85c579caaf8ccb3b7eabb9`  
		Last Modified: Sat, 22 Feb 2025 00:37:44 GMT  
		Size: 343.2 KB (343235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0623e2321e34b1b589a3f2314cdc767fe978372d17c7d621c1b6e40645f0e2`  
		Last Modified: Sat, 22 Feb 2025 00:37:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177b2d1a530b8667811479317d9e8ae2eb9cf1e26892e886e4baa298209fcfa4`  
		Last Modified: Sat, 22 Feb 2025 00:37:44 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3834ee7310198b95517a8b510904c8f38cbdb7c49df0b228572059fee55faa4`  
		Last Modified: Sat, 22 Feb 2025 00:37:46 GMT  
		Size: 19.8 MB (19805126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7d9cad94e2d870741143d557fc15084b8f7f0c3f510618f76861f6c020ec0c`  
		Last Modified: Sat, 22 Feb 2025 00:37:43 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73e623554754f1c6df8e43e93e867af1218d203b9111a1b977befbc4542f33e`  
		Last Modified: Sat, 22 Feb 2025 00:37:43 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39746d0ab1fefcec984bb203b47fb43af6294430288792c106045708180cf90f`  
		Last Modified: Sat, 22 Feb 2025 00:37:43 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7e0de055ddbb75c2d00fd897c8e623d5d164e9da002c14c5d7b16034ddefb2`  
		Last Modified: Sat, 22 Feb 2025 00:37:45 GMT  
		Size: 22.7 MB (22743044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d103e4264cc2326442d2f2c0d9a6f8a6d63672a9e1888b0eb106211fe4c866a8`  
		Last Modified: Sat, 22 Feb 2025 00:37:42 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e7898abd14f1e9f5aaa3850e26c6e47b5af14ccc7727ace668f06058bb6bbbb`  
		Last Modified: Sat, 22 Feb 2025 00:37:42 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac30b7d53b77634caea695af70ca54fad87eec4119c5d63afcd64b762dadee9f`  
		Last Modified: Sat, 22 Feb 2025 00:37:42 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13d827d5d10e25d56e691281a38fb310acbe73a53d8ecb6c27a3c737305b83d`  
		Last Modified: Sat, 22 Feb 2025 00:37:44 GMT  
		Size: 21.9 MB (21881997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
