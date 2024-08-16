## `docker:windowsservercore`

```console
$ docker pull docker@sha256:e1ded4b3a2aaf5d101daaca1e22004a6c4002e37cdf0842705f51159f0df81ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2655; amd64
	-	windows version 10.0.17763.6189; amd64

### `docker:windowsservercore` - windows version 10.0.20348.2655; amd64

```console
$ docker pull docker@sha256:722e8fd401b84665b82e0666308e3852fb7e55ef623784849a0ad1a0fbbfcd28
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2199540785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57c9795d7276f4ddea53e5745bd047597db78375c979913534c8fdf874a086a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Fri, 16 Aug 2024 21:04:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 16 Aug 2024 21:04:36 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 16 Aug 2024 21:04:37 GMT
ENV DOCKER_VERSION=27.1.2
# Fri, 16 Aug 2024 21:04:38 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.1.2.zip
# Fri, 16 Aug 2024 21:04:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 16 Aug 2024 21:04:49 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Fri, 16 Aug 2024 21:04:50 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Fri, 16 Aug 2024 21:04:50 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Fri, 16 Aug 2024 21:05:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 16 Aug 2024 21:05:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Fri, 16 Aug 2024 21:05:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Fri, 16 Aug 2024 21:05:02 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Fri, 16 Aug 2024 21:05:11 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd649075383e8df03ea713dfe59e1205716fbaa14450c10ef0d0a24a7b63669`  
		Last Modified: Tue, 13 Aug 2024 17:49:18 GMT  
		Size: 753.2 MB (753166182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e5e515bd55c81feeefd0785d8074f5be7923da2cce4b86409954eafb42a89d`  
		Last Modified: Fri, 16 Aug 2024 21:05:20 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa4236dc1d150b9033a0c12635f2856623e96efcf383d48c97522085f757a77d`  
		Last Modified: Fri, 16 Aug 2024 21:05:21 GMT  
		Size: 374.9 KB (374907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab4df154260eea68dd35cc730282a87fb57915392903c11035c17f519a6c96e`  
		Last Modified: Fri, 16 Aug 2024 21:05:19 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3677549ffed405f5ae64e6403793e352ecfac2b219c9eedb5028ff32996da03`  
		Last Modified: Fri, 16 Aug 2024 21:05:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bfc19c3fa98906bdc20e8a8400afe4f9b414a7340b21d265dccf34ed27ac257`  
		Last Modified: Fri, 16 Aug 2024 21:05:21 GMT  
		Size: 18.4 MB (18421675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d82313e190eab60e8625450d2b286dea76021f5da19bfdebe577415fa461e5c9`  
		Last Modified: Fri, 16 Aug 2024 21:05:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14377702006bc82ef23e61f2b8ed17e316e10b87ba0673db89ec95a79ee87a9`  
		Last Modified: Fri, 16 Aug 2024 21:05:17 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3b0c8b1a15fc09aae430ab9e6a6db5c6f206f1a740c3a1c1b480315148a7f7f`  
		Last Modified: Fri, 16 Aug 2024 21:05:17 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200e06de81cfb77043b8271865cdff0194d0e6754f636fb258b8a95e941f3ccf`  
		Last Modified: Fri, 16 Aug 2024 21:05:18 GMT  
		Size: 19.3 MB (19265658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ee8b6441d22cc15446aee0d2f0675daead9c2e51dbac7d89edc47d99df8303`  
		Last Modified: Fri, 16 Aug 2024 21:05:15 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e105068269a03cdc4679d19d4afb6c5a824ffb43ccfbc2430a18e0a80b35554`  
		Last Modified: Fri, 16 Aug 2024 21:05:15 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c871e44afd26ad9c6e84da90afe24be797cc92c7e5862563a271f080b7d6dc`  
		Last Modified: Fri, 16 Aug 2024 21:05:15 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a3de421425ac0e051642931e6459b4da6f2f3cd7022114cd5b7811b9eca88e`  
		Last Modified: Fri, 16 Aug 2024 21:05:18 GMT  
		Size: 19.7 MB (19701964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.6189; amd64

```console
$ docker pull docker@sha256:6fc12e3169bfe0a9322c7740f4f4079f8f45dd1b79168c426a89a43ad0c6d9fb
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2303121283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dd6dcd72864533d8de94060162775ef92bd31748712fbcd1f03469008647db8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Fri, 16 Aug 2024 20:59:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 16 Aug 2024 21:00:12 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 16 Aug 2024 21:00:13 GMT
ENV DOCKER_VERSION=27.1.2
# Fri, 16 Aug 2024 21:00:13 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.1.2.zip
# Fri, 16 Aug 2024 21:00:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 16 Aug 2024 21:00:35 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Fri, 16 Aug 2024 21:00:35 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Fri, 16 Aug 2024 21:00:36 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Fri, 16 Aug 2024 21:00:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 16 Aug 2024 21:00:56 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Fri, 16 Aug 2024 21:00:57 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Fri, 16 Aug 2024 21:00:57 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Fri, 16 Aug 2024 21:01:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc681518e2d562ce97fc231963b0590c8a4578d640e9226ebc7e7a64072c1c57`  
		Last Modified: Fri, 16 Aug 2024 21:01:22 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf861a9062e8367fea0bf7fd15b3a23566d429c8f7a698862ed56a6b30e5d08`  
		Last Modified: Fri, 16 Aug 2024 21:01:22 GMT  
		Size: 502.8 KB (502826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3a6eef9d04b51a84647684d5ac6acc5bbcf56cf1e9a1677f27f0a451d0dc191`  
		Last Modified: Fri, 16 Aug 2024 21:01:22 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f7463ca73d8038d2384509adeb789ee442a132ab89bd9125fd0d865c0e957c`  
		Last Modified: Fri, 16 Aug 2024 21:01:21 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1096db739f2668906215c2b312cca48af870253ffbbc08f284d90e88e5d9afd0`  
		Last Modified: Fri, 16 Aug 2024 21:01:23 GMT  
		Size: 18.4 MB (18429168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ba54531e0b5e75e9c6afb0f70803c3f19b3297ba195a9a0f0ed65ac1ed6cbb`  
		Last Modified: Fri, 16 Aug 2024 21:01:20 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf33926246d70e6dc5eb83affb3e85e5e70ba479cf02633542f105b7c0f9844c`  
		Last Modified: Fri, 16 Aug 2024 21:01:20 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f26c7e8351ae5c2502dd7735392d69fa658ffb65cb5f1ca900319b9409cf63`  
		Last Modified: Fri, 16 Aug 2024 21:01:20 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14de9ca87757d524465e1db5e32a8e157bd58a897ed38348289c0293a894bb21`  
		Last Modified: Fri, 16 Aug 2024 21:01:22 GMT  
		Size: 19.3 MB (19271416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cca9a181e2403ef565744f377e65fbaeceec043ac17c57026563ab53faa0edc`  
		Last Modified: Fri, 16 Aug 2024 21:01:19 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e61b3946fd8e06fe43f43af8f8d64efafff325bd4e24525b4464c35e4247d30c`  
		Last Modified: Fri, 16 Aug 2024 21:01:19 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d994d497e123945dca78f465e5d4c09bf3d99d78c717f359cf93b78ed69720e1`  
		Last Modified: Fri, 16 Aug 2024 21:01:19 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0130b148c08f6100b5c93d2c5de1ddd3a4a69543356d1c729eb4e1f72bded8dd`  
		Last Modified: Fri, 16 Aug 2024 21:01:22 GMT  
		Size: 19.7 MB (19702913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
