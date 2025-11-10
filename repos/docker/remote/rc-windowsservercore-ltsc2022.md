## `docker:rc-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:bf721924d903fac670bb05e56f730f411fd14a39d0fda7d3239f7d9d462da3a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `docker:rc-windowsservercore-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull docker@sha256:4e969481286ae13c412cf9826e1472bb5617299312d64cc43f2164b84dfd9423
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1642942479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a944bba80f23f5a8049fee57b13cfb10d7bf6bbc6c2fa5d717733207f4a17e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Mon, 10 Nov 2025 19:46:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 10 Nov 2025 19:58:01 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 10 Nov 2025 19:58:02 GMT
ENV DOCKER_VERSION=29.0.0-rc.3
# Mon, 10 Nov 2025 19:58:03 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-29.0.0-rc.3.zip
# Mon, 10 Nov 2025 19:58:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 10 Nov 2025 19:58:14 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Mon, 10 Nov 2025 19:58:15 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Mon, 10 Nov 2025 19:58:15 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Mon, 10 Nov 2025 19:58:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 10 Nov 2025 19:58:26 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Mon, 10 Nov 2025 19:58:27 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Mon, 10 Nov 2025 19:58:27 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Mon, 10 Nov 2025 19:58:35 GMT
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
	-	`sha256:812bc9a1d91374ca807bd9e023ef98e85f4eddedc06ccf494aa93d48c32cbf4e`  
		Last Modified: Mon, 10 Nov 2025 19:56:04 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:897c66864ac5dfa05350177f831ab4a7a0a1f7c0ba7449bea3099d3f19391280`  
		Last Modified: Mon, 10 Nov 2025 19:58:52 GMT  
		Size: 509.8 KB (509840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734390365fd2789ce29aa275e0c8fa74bd058f467f0eb941119ee8f8e9eed1a8`  
		Last Modified: Mon, 10 Nov 2025 19:58:52 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc15d8ca1b79b5a7fc47e7dc0f53a1caee4e094601b4da4dd6616fc825baf8a`  
		Last Modified: Mon, 10 Nov 2025 19:58:52 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80df375518f40fc478fb4bd3e736287a1bc485219082376af3f7f54149e1e668`  
		Last Modified: Mon, 10 Nov 2025 19:58:53 GMT  
		Size: 19.4 MB (19391039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c737045914c855b1dc71ed4f2fa62b521df1076187a63914a3d03555fb967d4c`  
		Last Modified: Mon, 10 Nov 2025 19:58:52 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d87027e9ff01a5399f62e828f308653e38bc3ad2beac2eeb42b9b9a9b506c98e`  
		Last Modified: Mon, 10 Nov 2025 19:58:52 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a394e2c272b9700910d6e83b715d8851e98869fe987e06c09f3aabd9c3212dbc`  
		Last Modified: Mon, 10 Nov 2025 19:58:52 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7bd207e4d5f893f001debaf3b272bd6d9403bd907c92a9651ff3ecb3ed9ea00`  
		Last Modified: Mon, 10 Nov 2025 19:58:54 GMT  
		Size: 23.2 MB (23161878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00ba958461f370a5f9df5cd1c1e720855648af7cce33ba9067702fbe43aaa5d`  
		Last Modified: Mon, 10 Nov 2025 19:58:52 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8bddeaa848dfa848d6fbfff943f589c665bf1f688407d6404951f6df71b697`  
		Last Modified: Mon, 10 Nov 2025 19:58:52 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:133735cefe1c845966cf2b84346e01868b5e7664dbcbbd17c7491776dc656c18`  
		Last Modified: Mon, 10 Nov 2025 19:58:52 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3c832dec081475863b0fb2e56d4caa4671f12a6a5a550debc38490384de01e`  
		Last Modified: Mon, 10 Nov 2025 19:58:56 GMT  
		Size: 22.7 MB (22675026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
