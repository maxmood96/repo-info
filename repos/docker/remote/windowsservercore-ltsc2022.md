## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:25201587b360a19e0225cf5fbc5ad92eaccf99d6f47cc59bd866c6c27a5d92ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull docker@sha256:a9f0778211b95959cb19b7417fdc93589c0d783b7e182caabefc4952fedf8b06
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1520702440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43adbf914fb93357f6f3df2549660390226ea93e6a7db215c371d6b18201daea`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 13 Sep 2024 18:59:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 13 Sep 2024 18:59:18 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 13 Sep 2024 18:59:18 GMT
ENV DOCKER_VERSION=27.2.1
# Fri, 13 Sep 2024 18:59:19 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.1.zip
# Fri, 13 Sep 2024 18:59:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 13 Sep 2024 18:59:32 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 13 Sep 2024 18:59:33 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.windows-amd64.exe
# Fri, 13 Sep 2024 18:59:33 GMT
ENV DOCKER_BUILDX_SHA256=8751c926b953edf6dd9c7db0b01e567033c407e85bb5f21d559199e2553a07cc
# Fri, 13 Sep 2024 18:59:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 13 Sep 2024 18:59:51 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.3
# Fri, 13 Sep 2024 18:59:52 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-windows-x86_64.exe
# Fri, 13 Sep 2024 18:59:53 GMT
ENV DOCKER_COMPOSE_SHA256=8603f4e6936e752793f7edf3f45ed67cb1b8ed8c7b1dabc5721384299bfebd7f
# Fri, 13 Sep 2024 19:00:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:968ea18f376199a42404723e7d74e681826104b3b96da085e0afaaadbf3e8fab`  
		Last Modified: Fri, 13 Sep 2024 19:00:19 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcce75fa43557965a4edc531888be2952885f977fa5b333aa2217b7806c9af02`  
		Last Modified: Fri, 13 Sep 2024 19:00:19 GMT  
		Size: 360.8 KB (360832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b456b2e5b2b16b9d62f91c3102e673a468531107e7a0910f1492afa5e79c994f`  
		Last Modified: Fri, 13 Sep 2024 19:00:17 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81d34c82b5f3b3e9a67718b5939686b856fc121e7c7f64f1c73c4b5291340bc9`  
		Last Modified: Fri, 13 Sep 2024 19:00:17 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea8d7253b0ce4433e059c594d3be21f4db900e8452c8be82d7ab5f417e2266d7`  
		Last Modified: Fri, 13 Sep 2024 19:00:19 GMT  
		Size: 18.9 MB (18931914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6beac8afa67cd4174b46984a8f75e526b738b9ca8f55dce31819c8dfa71588`  
		Last Modified: Fri, 13 Sep 2024 19:00:15 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecadd56795f72bad4fa0976a1319daa9b7260878ccad4cb57df5fca0768c096f`  
		Last Modified: Fri, 13 Sep 2024 19:00:15 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ed9bf9bc5ad479c75ba68cd06b55c3e6d4e6523e77cad190b34a0bb33d1cb1`  
		Last Modified: Fri, 13 Sep 2024 19:00:15 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee9f4f8c648c2b9e483ef620d1b0cc4124c8d20e0abbc0280b74fc7824bfc07`  
		Last Modified: Fri, 13 Sep 2024 19:00:16 GMT  
		Size: 19.3 MB (19286922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22dc42fd0d1a5f1a25f3be5499ba22a5e343096af2394249e49332f84efb04e`  
		Last Modified: Fri, 13 Sep 2024 19:00:13 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d31dead791a109ee247dff156f82c29aca1d4387cc354a4cf9bc7659a97235c`  
		Last Modified: Fri, 13 Sep 2024 19:00:13 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edcb47b7f34f0822dd337c75df6c23c780e63eaed38c7f999646839159f39647`  
		Last Modified: Fri, 13 Sep 2024 19:00:13 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab6440b3d03fc12928036bb2fbdcdd040c1d426e9acc6fdf60a3337facbf75f9`  
		Last Modified: Fri, 13 Sep 2024 19:00:16 GMT  
		Size: 19.9 MB (19918752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
