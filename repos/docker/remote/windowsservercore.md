## `docker:windowsservercore`

```console
$ docker pull docker@sha256:fff2cbfd775d2a702eb2289a9ba7bcd1d4bb5ecb4dd7110441a691f4feb8be2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2582; amd64
	-	windows version 10.0.17763.6054; amd64

### `docker:windowsservercore` - windows version 10.0.20348.2582; amd64

```console
$ docker pull docker@sha256:bac034a950f38a3ae8c03768c8f9fa59e6a42efcbedee5e14043467dcf80ddd5
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2198087625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938a6fef0c86e5e4dba145f36d7ea19a022f292cb488194224c703e96362c77b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 03 Jul 2024 10:07:02 GMT
RUN Install update 10.0.20348.2582
# Fri, 19 Jul 2024 17:58:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 19 Jul 2024 17:59:41 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 19 Jul 2024 17:59:41 GMT
ENV DOCKER_VERSION=27.0.3
# Fri, 19 Jul 2024 17:59:42 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.0.3.zip
# Fri, 19 Jul 2024 17:59:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 19 Jul 2024 17:59:59 GMT
ENV DOCKER_BUILDX_VERSION=0.16.1
# Fri, 19 Jul 2024 18:00:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.windows-amd64.exe
# Fri, 19 Jul 2024 18:00:01 GMT
ENV DOCKER_BUILDX_SHA256=34b8bd302364e9df99ebcd86658eae6ade175baf8baf6e74123ae04fcb2675c3
# Fri, 19 Jul 2024 18:00:11 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 19 Jul 2024 18:00:12 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.0
# Fri, 19 Jul 2024 18:00:12 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-windows-x86_64.exe
# Fri, 19 Jul 2024 18:00:13 GMT
ENV DOCKER_COMPOSE_SHA256=3dc98cacf0e0a05d8a714cc729827c062ff7ec13ffcd626e7b3767b362ce9b65
# Fri, 19 Jul 2024 18:00:24 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0206d135152eb909f50159d6ca348a5aead199afacbafc000b770c1b0720f6`  
		Last Modified: Tue, 09 Jul 2024 18:30:31 GMT  
		Size: 751.0 MB (751001543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce0fa1a98ef4d8a75232cdac7df9ac8d12d584f7be46cf70a9c30207b09f326`  
		Last Modified: Fri, 19 Jul 2024 18:00:30 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff5ee0c7efb7848857ff8000eb8fbc139a43b8feff341eb9ea1969f491b7ca6`  
		Last Modified: Fri, 19 Jul 2024 18:00:30 GMT  
		Size: 359.4 KB (359359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba7856ebecae3fa637378a288c71b93b27a3d24ae8929482be9b3b0a3872965`  
		Last Modified: Fri, 19 Jul 2024 18:00:29 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e88116d7f5e32791e9a7aa752ed71c800bd02fc24e0db1c74758e79f9d812d1`  
		Last Modified: Fri, 19 Jul 2024 18:00:29 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e67e6be9405bfccfaaae8933af7a07365c89578e25b6033ee0e87c4b52de7542`  
		Last Modified: Fri, 19 Jul 2024 18:00:31 GMT  
		Size: 19.2 MB (19233364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3f77b1a1615eb65b0ac51a53aefb36e8671c0e4c90a7796b61e300bd12f1775`  
		Last Modified: Fri, 19 Jul 2024 18:00:28 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fee477f2ca03b53d593dad69e3228985798b9978e490801c17261c730623fd`  
		Last Modified: Fri, 19 Jul 2024 18:00:28 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c372962114138bf04b9ab4d3a8c23b4aa0d99ecafabc94d1e23eaba161e82b6e`  
		Last Modified: Fri, 19 Jul 2024 18:00:28 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d514a4480bf9efe40efe2a9f72d25fcd96a24023f63562a9e78a0c84451e12a6`  
		Last Modified: Fri, 19 Jul 2024 18:00:30 GMT  
		Size: 19.2 MB (19224422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9873b049158823fa7286e1a35a9df8de6f2f687ff6c11a14892803c6dd5368`  
		Last Modified: Fri, 19 Jul 2024 18:00:27 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d09c5ad1bc27707e6a6fa79b8d27b3f2d0138754f019f623aa930a742bb28ed`  
		Last Modified: Fri, 19 Jul 2024 18:00:27 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03bc1c2f3f1d11d1402e621fbcfb2969c1a4579316caa4d7e697dc0ae82f87bc`  
		Last Modified: Fri, 19 Jul 2024 18:00:27 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05220546d79e2d04ab9e85e54fcf738f88a10f315e63a6d7e68aa96e993015c4`  
		Last Modified: Fri, 19 Jul 2024 18:00:30 GMT  
		Size: 19.7 MB (19658612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.6054; amd64

```console
$ docker pull docker@sha256:94bacfb293e26a7fcd26adb3550fbf1e0b1727b4d006bc2ad297ee39c5bf3ba2
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2297147041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a80e00bdf31055bf0d11ec5b94a178408c6cce7384245036c58e8529d553112`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Fri, 19 Jul 2024 18:05:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 19 Jul 2024 18:06:06 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 19 Jul 2024 18:06:06 GMT
ENV DOCKER_VERSION=27.0.3
# Fri, 19 Jul 2024 18:06:07 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.0.3.zip
# Fri, 19 Jul 2024 18:06:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 19 Jul 2024 18:06:33 GMT
ENV DOCKER_BUILDX_VERSION=0.16.1
# Fri, 19 Jul 2024 18:06:33 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.windows-amd64.exe
# Fri, 19 Jul 2024 18:06:34 GMT
ENV DOCKER_BUILDX_SHA256=34b8bd302364e9df99ebcd86658eae6ade175baf8baf6e74123ae04fcb2675c3
# Fri, 19 Jul 2024 18:06:58 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 19 Jul 2024 18:06:58 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.0
# Fri, 19 Jul 2024 18:06:59 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-windows-x86_64.exe
# Fri, 19 Jul 2024 18:07:00 GMT
ENV DOCKER_COMPOSE_SHA256=3dc98cacf0e0a05d8a714cc729827c062ff7ec13ffcd626e7b3767b362ce9b65
# Fri, 19 Jul 2024 18:07:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f98e7fe87492b83d7775a348ae0c94412b638ab5bba1a80b03c3a547708acd`  
		Last Modified: Tue, 09 Jul 2024 17:23:28 GMT  
		Size: 587.8 MB (587809033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8af023750251bf7f80d7531b54e268970fc769f62ae281517d72e05903158fd`  
		Last Modified: Fri, 19 Jul 2024 18:07:33 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6565f65870867f7851f7ad66bbf364cea98c3055282faf2195259e74141d65de`  
		Last Modified: Fri, 19 Jul 2024 18:07:32 GMT  
		Size: 486.1 KB (486137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ebb5d461f0e5e03f09963fde7bb3d0590332068044327f30cd7c802c98c620`  
		Last Modified: Fri, 19 Jul 2024 18:07:31 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef6b742c5b04b90411bab835eec45aeaf8f3a1ecb0af9f2c3772a337cc2e2e5`  
		Last Modified: Fri, 19 Jul 2024 18:07:31 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c7b8e8488ed636d9f14a35867db8ea43c2b5cc0a44fd22e49d812240f8cdbc1`  
		Last Modified: Fri, 19 Jul 2024 18:07:33 GMT  
		Size: 19.3 MB (19270704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062a85e20c87c72dc7e9ddcfbc0c5c9cbe3b6000f515a039f20e33ae787fef38`  
		Last Modified: Fri, 19 Jul 2024 18:07:29 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9552250dee36bf3594388998c782b9401835bf081fd3a201d74744bc0674792`  
		Last Modified: Fri, 19 Jul 2024 18:07:29 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41219cf1239f988a81cbe5d135196e5f4db3924b05a0f42fa6ffe5fe48a325a9`  
		Last Modified: Fri, 19 Jul 2024 18:07:29 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f85ad071ccb949c2385f44539189d962a330d2db7ab37a56bd1d2ca16d561dc`  
		Last Modified: Fri, 19 Jul 2024 18:07:30 GMT  
		Size: 19.3 MB (19258189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:612b56d347f16d61baa378760ef8515ef076829452b4c372c24a7d193d225f22`  
		Last Modified: Fri, 19 Jul 2024 18:07:27 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f26763d0fd549cc1bd17ba2d6a6a201d5ffc3ae0237f987b1877258771971a58`  
		Last Modified: Fri, 19 Jul 2024 18:07:27 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7faab39a1cb1e694569de89ed7f327ec90d46ad218301f73ce931e5b95edfba`  
		Last Modified: Fri, 19 Jul 2024 18:07:28 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ac7e67d8760a600292c01639e85bf7368abf958c12791903c0239c8f2128ba`  
		Last Modified: Fri, 19 Jul 2024 18:07:30 GMT  
		Size: 19.7 MB (19690909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
