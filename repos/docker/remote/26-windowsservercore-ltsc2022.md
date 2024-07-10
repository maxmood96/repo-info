## `docker:26-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:187cc83e2bb2dc1b58c43c8dab68182794f659981794519c32c000aa7bcdb27f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2582; amd64

### `docker:26-windowsservercore-ltsc2022` - windows version 10.0.20348.2582; amd64

```console
$ docker pull docker@sha256:b89d44be89b2488dba364d15498369cbb475000e9d8e0fdb2eb02191df834d47
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2197895630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aebcbfdbeda281beefd8baae520390d230143ea48f1dcfff98afefe97c1774f7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 03 Jul 2024 10:07:02 GMT
RUN Install update 10.0.20348.2582
# Wed, 10 Jul 2024 17:06:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jul 2024 17:07:05 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Jul 2024 17:07:05 GMT
ENV DOCKER_VERSION=26.1.4
# Wed, 10 Jul 2024 17:07:06 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-26.1.4.zip
# Wed, 10 Jul 2024 17:07:16 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 10 Jul 2024 17:07:17 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Wed, 10 Jul 2024 17:07:18 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.windows-amd64.exe
# Wed, 10 Jul 2024 17:07:18 GMT
ENV DOCKER_BUILDX_SHA256=d28cff3df9fdbb37aa7434edb09d8befe5e90e5ef5887807569b694f25bebd33
# Wed, 10 Jul 2024 17:07:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 10 Jul 2024 17:07:26 GMT
ENV DOCKER_COMPOSE_VERSION=2.28.1
# Wed, 10 Jul 2024 17:07:27 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-windows-x86_64.exe
# Wed, 10 Jul 2024 17:07:27 GMT
ENV DOCKER_COMPOSE_SHA256=7dbd8848d9b8dce489c4d2ce1bb4f4b7a3dccb07a08596ae98b85091e1645bcc
# Wed, 10 Jul 2024 17:07:35 GMT
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
	-	`sha256:f2d9d3de1058a39678546ae37fcf1bae84d4f9ef46e987a8aae464067a2110da`  
		Last Modified: Wed, 10 Jul 2024 17:07:43 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70fc228473c5a99761b4df8a8a2d6480491d148eb2b6226712c02b57c441b8a3`  
		Last Modified: Wed, 10 Jul 2024 17:07:44 GMT  
		Size: 353.7 KB (353690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ffd5f477c1b8d5d76f9614eb3cd5ec902b1ac1f8be64cabef4f2ac67972a1e3`  
		Last Modified: Wed, 10 Jul 2024 17:07:42 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5544bd81947c008123c95c311e73bce204fb5a324352243ca07c226e292a2ad1`  
		Last Modified: Wed, 10 Jul 2024 17:07:42 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b536eb8933d9e23be6e81c349259217c0ff0ac4c811cfaf0f0ff1d1e6c21b0`  
		Last Modified: Wed, 10 Jul 2024 17:07:44 GMT  
		Size: 19.3 MB (19250069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85acd654f2e15df5e3b3d86e685a7df672c9d69ed5fada7fc0a67b055a4eed35`  
		Last Modified: Wed, 10 Jul 2024 17:07:40 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b63cd5a9085fd35a77eba7cbd17d34168b84095f058c4c166ff437454290c8`  
		Last Modified: Wed, 10 Jul 2024 17:07:40 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b050385ea469075e8ac3cd0c01f59b05237fe243752b4af0ba748c499f7c7214`  
		Last Modified: Wed, 10 Jul 2024 17:07:40 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e7223c9cd26ba7de1b396ce8f876f3778a2c9a9742172142b43c200cca0e015`  
		Last Modified: Wed, 10 Jul 2024 17:07:41 GMT  
		Size: 19.0 MB (19022171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f8e9a2edc1e7c0274a5901135c476d5c8aa0e7fdb984c81763b69cc7e2c4c5`  
		Last Modified: Wed, 10 Jul 2024 17:07:39 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cebb7aee2d0caeef03e8450dd9e72a42e73bd3afa18044f08f21c60a9cf0a981`  
		Last Modified: Wed, 10 Jul 2024 17:07:39 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99935b0862983b7826842674ae5c56f9c1e932efbd1a676637a7df28557caa00`  
		Last Modified: Wed, 10 Jul 2024 17:07:39 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918a1533887acb04a5fac682ef1eee07f51aff7be62fc5a0aa9be26002311e70`  
		Last Modified: Wed, 10 Jul 2024 17:07:41 GMT  
		Size: 19.7 MB (19657816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
