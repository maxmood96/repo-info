## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:fb26fa369f6f6262c900c470289c0cf16c3f4837b13f905b65ad5599f246a78a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3453; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.3453; amd64

```console
$ docker pull docker@sha256:3370619ccd432aa92aeb82db6ceb41fb9a2c1d90694f184b93a7fc013216ebb5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335459929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cca8cf5b8b43e5660f7710c121b54b49ba583c85a4332755a99566e58be7eaa1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 04 Apr 2025 23:10:04 GMT
RUN Install update 10.0.20348.3453
# Thu, 17 Apr 2025 18:31:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Apr 2025 18:31:57 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 17 Apr 2025 18:31:58 GMT
ENV DOCKER_VERSION=28.1.0
# Thu, 17 Apr 2025 18:31:58 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.0.zip
# Thu, 17 Apr 2025 18:32:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 17 Apr 2025 18:32:09 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Thu, 17 Apr 2025 18:32:09 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Thu, 17 Apr 2025 18:32:10 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Thu, 17 Apr 2025 18:32:18 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 17 Apr 2025 18:32:19 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.1
# Thu, 17 Apr 2025 18:32:19 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-windows-x86_64.exe
# Thu, 17 Apr 2025 18:32:20 GMT
ENV DOCKER_COMPOSE_SHA256=971d6000e2c70da19c20f8264330a7ec3962b1fd59601afeb7e3636bad89b8c9
# Thu, 17 Apr 2025 18:32:29 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510f1abe0ffe1466f946291b3ac20345b4a5e2063a896736990eae81bbf4bdb4`  
		Last Modified: Tue, 08 Apr 2025 21:40:38 GMT  
		Size: 808.8 MB (808803243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc89a6e0b1598e68afc46c4fd762c3c143b7a6a9ca6d13a0545ffa90a246ece6`  
		Last Modified: Thu, 17 Apr 2025 18:32:40 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8485b6de0a23c7be2467d19ad4e4fa91efed84ac211a385a2d9ca23b35aac182`  
		Last Modified: Thu, 17 Apr 2025 18:32:40 GMT  
		Size: 356.8 KB (356843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9ec570e402cd6771f41e062d7d6ca5e26a619b405a79f72bad46094c5536a3`  
		Last Modified: Thu, 17 Apr 2025 18:32:38 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6790684ad7f44f4cd7a91c47a082c20b0c61dd73bf5b85d7a07913ce2f59e1`  
		Last Modified: Thu, 17 Apr 2025 18:32:38 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd86cc6b81ae033128634b13be5564efd9a67836627df25014144e0375bcb44c`  
		Last Modified: Thu, 17 Apr 2025 18:32:40 GMT  
		Size: 19.9 MB (19894709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a49df8ff1b3aceb7eb937266ec144177a7c4b15ca730b2aace73a2f877ec0de`  
		Last Modified: Thu, 17 Apr 2025 18:32:36 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d125e395249b5f81e16bc146ee6840da492fba8f927e41b1f206d2035d4e6ed5`  
		Last Modified: Thu, 17 Apr 2025 18:32:36 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf14b8452fee435be72ae6a263ba75779d0ab43227b25ae20c2b1350be6c4c0`  
		Last Modified: Thu, 17 Apr 2025 18:32:36 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89f15f838b08d714375b6eaa88ec21f634148d65d3ae6d2ea6b0b925845f1805`  
		Last Modified: Thu, 17 Apr 2025 18:32:37 GMT  
		Size: 22.4 MB (22356793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e20bc799cec825f36c770a446ab96e28f58f0b88b339e86cc99d120952cbc44`  
		Last Modified: Thu, 17 Apr 2025 18:32:34 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc04d2f01c86a938d99ecb87016458ac9f4e1ea9563110c20f8090e9014be30`  
		Last Modified: Thu, 17 Apr 2025 18:32:34 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd962c7e1905c87ee5b53929dd2d92118bb1fd4d4b2ac3bdb76d71b5a5ac384c`  
		Last Modified: Thu, 17 Apr 2025 18:32:34 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f19e8020d1cd200fcd02d473a39957001a180133e91b18400533a685fd1c4f7`  
		Last Modified: Thu, 17 Apr 2025 18:32:38 GMT  
		Size: 21.8 MB (21844326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
