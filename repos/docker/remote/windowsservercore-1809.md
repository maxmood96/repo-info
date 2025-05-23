## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:c3dda8e1cfe3b7ff0ae0a6031cc8736fc23d0df01a68ba7b26463720270b7d46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull docker@sha256:d8c9d0051e906b65e6b274145bb1a6bf42c01be2b584e015b2450061a831fb7a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2248271030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80bc6320aabd791b70a61076d88e78589d31d99b579e296e6d9ed671db172f92`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Fri, 23 May 2025 19:01:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 23 May 2025 19:01:50 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 23 May 2025 19:01:51 GMT
ENV DOCKER_VERSION=28.1.1
# Fri, 23 May 2025 19:01:51 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.1.zip
# Fri, 23 May 2025 19:02:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 23 May 2025 19:02:05 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Fri, 23 May 2025 19:02:06 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Fri, 23 May 2025 19:02:06 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Fri, 23 May 2025 19:02:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 23 May 2025 19:02:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Fri, 23 May 2025 19:02:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Fri, 23 May 2025 19:02:17 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Fri, 23 May 2025 19:02:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95a939635fd6bec8c1562dcdbdde2fdb64095d1be9873313939c878db6f7279`  
		Last Modified: Tue, 13 May 2025 17:48:34 GMT  
		Size: 463.4 MB (463449115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bedba5d8bb10709897be0ca11c0fd7aa652325aa9e1ae6cb99499ffb5348423`  
		Last Modified: Fri, 23 May 2025 19:02:32 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1eda583ca07b2852595a7dfa1f3ffae9eef5e9e4299901df7656452d88015f`  
		Last Modified: Fri, 23 May 2025 19:02:32 GMT  
		Size: 364.7 KB (364665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72420287a02085c94def4c22f2ca2f8b3360457c2df6304a88c9286147d4ddc`  
		Last Modified: Fri, 23 May 2025 19:02:31 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adaa2052518fa53328cd0f816e795f6c556cbb16b8e631ada84d61bc3b7e2f0e`  
		Last Modified: Fri, 23 May 2025 19:02:30 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:886ee17b8998b7b6c685ec11fc8880863992fdfb32bbbeb7228b4c2ded3dd72b`  
		Last Modified: Fri, 23 May 2025 19:02:32 GMT  
		Size: 19.9 MB (19901768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1b2fe179779a92d665c0ea748ce755d333ba2072b76552a3bb6705554b8763`  
		Last Modified: Fri, 23 May 2025 19:02:30 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85068da4803dc6274a2db2661b92f564624bdf460cba85c56c400e054648ee14`  
		Last Modified: Fri, 23 May 2025 19:02:29 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d8c76e0c60a668e8f2ed3d2aa9b644e0d25faee78c68cc796ba836d041cc62`  
		Last Modified: Fri, 23 May 2025 19:02:29 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4321b3be2b8f9845f01f6a0503043622534fada9d1f6e960e4067926089509`  
		Last Modified: Fri, 23 May 2025 19:02:31 GMT  
		Size: 22.3 MB (22266672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47afe0e541f0c501cfc4e2b3fa3d95dd7123ff584e51d0a9e126547eb8009a4b`  
		Last Modified: Fri, 23 May 2025 19:02:28 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afdf962e512c522c9753deba814e6a0b63ebaf74fc3beb95bb5f268c88e2e09e`  
		Last Modified: Fri, 23 May 2025 19:02:29 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a93a31e65a4686b2102d0fe84c29161dc421cfe1af37756cc4d6555f1e033c40`  
		Last Modified: Fri, 23 May 2025 19:02:28 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921c35cd822abe89a11c931d38819a21ff6e6f984acaf3de4b3f3242002e2bbe`  
		Last Modified: Fri, 23 May 2025 19:02:32 GMT  
		Size: 22.0 MB (22008812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
