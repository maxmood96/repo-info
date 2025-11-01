## `docker:28-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:1bf677c47c7eb661415fafa2ca44e2e6c4422e954a1945abed6b3ffb4917a330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `docker:28-windowsservercore-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull docker@sha256:e43c890001f2d513b7371d576fbad3171a42b38faa0662fec0e461ef90c54819
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1644338394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee163f65b7eacd1f969349f4b32835a6d8395e33fe5b3360e9fa839ea7bc853`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Sat, 01 Nov 2025 00:00:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 01 Nov 2025 00:01:05 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 01 Nov 2025 00:01:06 GMT
ENV DOCKER_VERSION=28.5.1
# Sat, 01 Nov 2025 00:01:07 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.1.zip
# Sat, 01 Nov 2025 00:01:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 01 Nov 2025 00:01:31 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Sat, 01 Nov 2025 00:01:33 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Sat, 01 Nov 2025 00:01:34 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Sat, 01 Nov 2025 00:02:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 01 Nov 2025 00:02:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Sat, 01 Nov 2025 00:02:02 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Sat, 01 Nov 2025 00:02:03 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Sat, 01 Nov 2025 00:02:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46cc5eeeb72e129272dfca31d07a512cf901707d7446bd1b292b96b040ab8787`  
		Last Modified: Sat, 01 Nov 2025 00:14:26 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770c2fb5bce2e932f2ec5e30b01a7aa868f231b36adbf17738f7dce086dfed46`  
		Last Modified: Sat, 01 Nov 2025 00:14:25 GMT  
		Size: 510.8 KB (510820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b08fc4b24b5fe13129b528a695dbdd1b3971c4e1a77cbbc7c57662dd69e85c`  
		Last Modified: Sat, 01 Nov 2025 00:14:26 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7643434ca98bf15b6e614fde9b54bb983600450013015882463d7b8622865f42`  
		Last Modified: Sat, 01 Nov 2025 00:14:25 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e0230600e13e81127a504d8af9bea02f38319bfc6d68d16189615cbeaea34aa`  
		Last Modified: Sat, 01 Nov 2025 00:14:29 GMT  
		Size: 20.8 MB (20781165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a30a2d0f710ad87b5149bf3b271a776e1ff8ef3201a3316f1fcc96da287f261`  
		Last Modified: Sat, 01 Nov 2025 00:14:25 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5b01c38ec1e3ba1915da51be0552f7ca4cf4f84e2803ba2e154b68171fb764`  
		Last Modified: Sat, 01 Nov 2025 00:14:26 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e4404a557f2c4156b01f700e90cb97be9a6f0e926ae399ecaf9ff0a001562ca`  
		Last Modified: Sat, 01 Nov 2025 00:14:26 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ddc0df34aaf874a200bff0d905a909ede57d03c682d8ca08da019952373645`  
		Last Modified: Sat, 01 Nov 2025 00:14:28 GMT  
		Size: 23.2 MB (23163655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4267760ce787b841a05c316b35f91e95bd9e69994373a1dbb323743246cc690a`  
		Last Modified: Sat, 01 Nov 2025 00:14:25 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2c1a000e617ff07bb472c8870dee371438daa6ad5fe7e29060aacd83abd5e4`  
		Last Modified: Sat, 01 Nov 2025 00:14:25 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327f32ebe61d0026b8eb1e20d9257e92c4575b500afc147b3f18cbcff8404715`  
		Last Modified: Sat, 01 Nov 2025 00:14:27 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05169ad8cbc026633c054f283872cc71d9224e4af266ebbf6535a9fe766a7436`  
		Last Modified: Sat, 01 Nov 2025 00:14:29 GMT  
		Size: 22.7 MB (22677991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
