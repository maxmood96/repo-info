## `docker:26-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:fd8ebb8e49da01649402132edc9f3bd9aeb8fbe2ff0e67cb98489f9ed751a24b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2582; amd64

### `docker:26-windowsservercore-ltsc2022` - windows version 10.0.20348.2582; amd64

```console
$ docker pull docker@sha256:c00e9a509136a28f65ccd195b13c6ab4eee8cb69053046770333dc8148ae32ff
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2198166494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b835eec9d11477d150da08feddb850d2eefcc325e36a91503b0bf7f045b8882f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 03 Jul 2024 10:07:02 GMT
RUN Install update 10.0.20348.2582
# Thu, 18 Jul 2024 18:55:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 18 Jul 2024 18:55:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 18 Jul 2024 18:55:42 GMT
ENV DOCKER_VERSION=26.1.4
# Thu, 18 Jul 2024 18:55:43 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-26.1.4.zip
# Thu, 18 Jul 2024 18:55:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 18 Jul 2024 18:55:53 GMT
ENV DOCKER_BUILDX_VERSION=0.16.0
# Thu, 18 Jul 2024 18:55:53 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.windows-amd64.exe
# Thu, 18 Jul 2024 18:55:54 GMT
ENV DOCKER_BUILDX_SHA256=6521f85836e4bdc1347b38b9de32268ac09987e2c1ea0e424b0e07632ab61025
# Thu, 18 Jul 2024 18:56:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 18 Jul 2024 18:56:02 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.0
# Thu, 18 Jul 2024 18:56:03 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-windows-x86_64.exe
# Thu, 18 Jul 2024 18:56:03 GMT
ENV DOCKER_COMPOSE_SHA256=3dc98cacf0e0a05d8a714cc729827c062ff7ec13ffcd626e7b3767b362ce9b65
# Thu, 18 Jul 2024 18:56:12 GMT
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
	-	`sha256:169d1e4234b32382e18c406407885c7506cb6b78567811df533fc4215277384b`  
		Last Modified: Thu, 18 Jul 2024 18:56:22 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf0a36136c65bd999651d99bc5a03f42f513c6cf447f59b66066223e9b11d82`  
		Last Modified: Thu, 18 Jul 2024 18:56:22 GMT  
		Size: 357.1 KB (357115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc4628d2b90cd90ebf8a8a26270b68783e15d40d0e287cf7bf7d25474a77697`  
		Last Modified: Thu, 18 Jul 2024 18:56:20 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d1fe273cd5053554a169736de4e6ccd517b2a8e86f74b314364f18271dd0da`  
		Last Modified: Thu, 18 Jul 2024 18:56:20 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c482c639821a82ebec756a858870c129f6289a860463beb00eba7106b730f4`  
		Last Modified: Thu, 18 Jul 2024 18:56:22 GMT  
		Size: 19.3 MB (19251909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:587e60346672fda703460d77df0c253327345effb32be443332d9bceec941157`  
		Last Modified: Thu, 18 Jul 2024 18:56:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7fecd9289cf6f0c394ba74d5df11592a1872ba3d974c1c19c41138f9cf96f99`  
		Last Modified: Thu, 18 Jul 2024 18:56:18 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df180f469603b83f34943fb7f152cfca520726fd5fef3a0bf47a50294999859`  
		Last Modified: Thu, 18 Jul 2024 18:56:18 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e517d4abfba3f198846b5f6b65532a05dca2d215e9b6725e82f05be7750d82a`  
		Last Modified: Thu, 18 Jul 2024 18:56:19 GMT  
		Size: 19.3 MB (19256363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45bbd5e0633959bfab0b1b5fb48f4c5f19787b79701bfd318ec93769ea13a2fa`  
		Last Modified: Thu, 18 Jul 2024 18:56:16 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992eabdac796b660f7b0ca515318c9886f8416c8e6507c1cbe5c02db7b88030b`  
		Last Modified: Thu, 18 Jul 2024 18:56:16 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c174ff82fb043a99c6f2177e76d125b8bf896eb4bc491d13736c426644b391`  
		Last Modified: Thu, 18 Jul 2024 18:56:16 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3abe1761e411a95510db879d006df059af851024710be870ef9b392ac094935e`  
		Last Modified: Thu, 18 Jul 2024 18:56:19 GMT  
		Size: 19.7 MB (19689195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
