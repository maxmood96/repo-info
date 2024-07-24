## `docker:26-windowsservercore-1809`

```console
$ docker pull docker@sha256:24aa33679e37730787ba29a5de454961c5d52aa6bebe3236da26adb06daa637c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `docker:26-windowsservercore-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull docker@sha256:a416bb5343d27048f6b89290dc560a75b2413cfac64cc36b1016cbff01096f6b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2297155546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20cc7f93d15104cb0907c1bf7425c672022343951620654f8e8935954b169cd7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Wed, 24 Jul 2024 01:08:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 24 Jul 2024 01:10:34 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 24 Jul 2024 01:10:35 GMT
ENV DOCKER_VERSION=26.1.4
# Wed, 24 Jul 2024 01:10:36 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-26.1.4.zip
# Wed, 24 Jul 2024 01:11:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 24 Jul 2024 01:11:11 GMT
ENV DOCKER_BUILDX_VERSION=0.16.1
# Wed, 24 Jul 2024 01:11:11 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.windows-amd64.exe
# Wed, 24 Jul 2024 01:11:12 GMT
ENV DOCKER_BUILDX_SHA256=34b8bd302364e9df99ebcd86658eae6ade175baf8baf6e74123ae04fcb2675c3
# Wed, 24 Jul 2024 01:11:37 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 24 Jul 2024 01:11:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Wed, 24 Jul 2024 01:11:39 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-windows-x86_64.exe
# Wed, 24 Jul 2024 01:11:40 GMT
ENV DOCKER_COMPOSE_SHA256=c80155bfd2669bcdc7482ae7ccf7ccaf6b5da2149b690d806c7a4d9200abc54e
# Wed, 24 Jul 2024 01:12:06 GMT
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
	-	`sha256:02b209f9f8ffeb7c42c118e3cbb2ff11c7aa173d0dd2c01f856aa14e77fb3bb9`  
		Last Modified: Wed, 24 Jul 2024 01:12:13 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573a8eefd4242501259efc06113ed4f07021470bfd6a172759116a42f983feaa`  
		Last Modified: Wed, 24 Jul 2024 01:12:13 GMT  
		Size: 496.9 KB (496878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aab6d2dc27813eff61c87ca5ce4e177b5a307372ad06d312603ee7470264274`  
		Last Modified: Wed, 24 Jul 2024 01:12:12 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022f186558f30af03ef2ddbd5b9a44e5839b7b3fcdc9c17e2ec9d5893006cacb`  
		Last Modified: Wed, 24 Jul 2024 01:12:12 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d7f9288dfe4d9541f6b8039f9661e7894759fef9086caeaad161a80285c127`  
		Last Modified: Wed, 24 Jul 2024 01:12:13 GMT  
		Size: 19.3 MB (19265286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053dad5e063cb32fb00b90e53da48e42c4c895413eae9c6520c960876beecfbf`  
		Last Modified: Wed, 24 Jul 2024 01:12:11 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:154a8eef3451fc228ad0fa03983a25f807621f74dbc7da46973908c09efbd423`  
		Last Modified: Wed, 24 Jul 2024 01:12:11 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d5eac2cb5256d43ef82701bd1206b93af5898efd3c0be6e7ae0d707ea04e7d`  
		Last Modified: Wed, 24 Jul 2024 01:12:11 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3821e2349119cc9991e0d882e81038ddddeebec4485290517f6040b9c2c24a34`  
		Last Modified: Wed, 24 Jul 2024 01:12:13 GMT  
		Size: 19.3 MB (19261251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd1f9beff1047df630cafb78f3320d57cfb9ccd7efbb8ba3304095bd22a98dcb`  
		Last Modified: Wed, 24 Jul 2024 01:12:10 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57cad215ec83b27e0e230eeb0aaae8191cca22f7db55ba3fd4c542169a6a3ae8`  
		Last Modified: Wed, 24 Jul 2024 01:12:10 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce19729c4494daf6f672481dcb76cf307f7d7bb1eae1a6b37733ff1ca679ec30`  
		Last Modified: Wed, 24 Jul 2024 01:12:10 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db6d933d53382125a2f07e66ce1c38457c95c2ec38db57cf608c3cff75bfba8`  
		Last Modified: Wed, 24 Jul 2024 01:12:13 GMT  
		Size: 19.7 MB (19691086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
