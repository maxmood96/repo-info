## `docker:windowsservercore`

```console
$ docker pull docker@sha256:caea991ba7d71c171d606d2e72216c955562502e5c8f3acc96bdaea5be6136cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2582; amd64
	-	windows version 10.0.17763.6054; amd64

### `docker:windowsservercore` - windows version 10.0.20348.2582; amd64

```console
$ docker pull docker@sha256:84655bc590cff47c7d02d0c49d8e64713dc5766fe526fa665036e6acedadb960
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2198195403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcef632ed27fe139859242ac4a89c9ecaf32572cbef1fc7f5a772730f3318f61`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 03 Jul 2024 10:07:02 GMT
RUN Install update 10.0.20348.2582
# Fri, 12 Jul 2024 01:03:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 12 Jul 2024 01:03:56 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 12 Jul 2024 01:03:57 GMT
ENV DOCKER_VERSION=27.0.3
# Fri, 12 Jul 2024 01:03:58 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.0.3.zip
# Fri, 12 Jul 2024 01:04:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 12 Jul 2024 01:04:08 GMT
ENV DOCKER_BUILDX_VERSION=0.16.0
# Fri, 12 Jul 2024 01:04:09 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.windows-amd64.exe
# Fri, 12 Jul 2024 01:04:09 GMT
ENV DOCKER_BUILDX_SHA256=6521f85836e4bdc1347b38b9de32268ac09987e2c1ea0e424b0e07632ab61025
# Fri, 12 Jul 2024 01:04:16 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 12 Jul 2024 01:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.28.1
# Fri, 12 Jul 2024 01:04:17 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-windows-x86_64.exe
# Fri, 12 Jul 2024 01:04:17 GMT
ENV DOCKER_COMPOSE_SHA256=7dbd8848d9b8dce489c4d2ce1bb4f4b7a3dccb07a08596ae98b85091e1645bcc
# Fri, 12 Jul 2024 01:04:24 GMT
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
	-	`sha256:d9f08a19aec32addc01d21985737857f961960bafa5aa8e49e86761ff912d737`  
		Last Modified: Fri, 12 Jul 2024 01:04:30 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01a416e0588869d5afa5fccffde4092ba71320fa4b648292979ec0c6caf4b62`  
		Last Modified: Fri, 12 Jul 2024 01:04:30 GMT  
		Size: 368.5 KB (368481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367ba714fce474bb5ae219ae6c150ce8bfba1e5c19e1858adf93241a92458c26`  
		Last Modified: Fri, 12 Jul 2024 01:04:29 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55628c0fb30439578ada6716079c90bcb28f41664b4b8ff9d8eb198c6e52618`  
		Last Modified: Fri, 12 Jul 2024 01:04:29 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2198e6b44e9b208c7d2d8fab684d2988cbb7cf8849b29d8c7f7df809c23c9872`  
		Last Modified: Fri, 12 Jul 2024 01:04:31 GMT  
		Size: 19.3 MB (19277611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22851ce89b4706e7247fca31039b2c0843db9156d297fd0a31fcfa7a1082afa7`  
		Last Modified: Fri, 12 Jul 2024 01:04:28 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dd1058aa80c4585e981ed70f9cefb2f30642d87c429b98362273620bb02b4ae`  
		Last Modified: Fri, 12 Jul 2024 01:04:28 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9319ef11a4b608d6002608045ae1851b5a701cc5d73e88f2217914d695824c71`  
		Last Modified: Fri, 12 Jul 2024 01:04:28 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c4a29b316282274d6381cd7e0aa38a22f24c58ed26cbf9b0f3598cf9412304`  
		Last Modified: Fri, 12 Jul 2024 01:04:30 GMT  
		Size: 19.3 MB (19268056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac27215162e179a9047d020ac2ffd5d6d3146e80916cd83f20538273985d024`  
		Last Modified: Fri, 12 Jul 2024 01:04:27 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:184cb6242826cab261a35b4233091c8d2ff6b474acdd35f38c98bc7a82f8ccef`  
		Last Modified: Fri, 12 Jul 2024 01:04:27 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afdb0553dc376c2928b0cdbe1d399974f6afae58bc23a59eb6aadbc9462f9cbf`  
		Last Modified: Fri, 12 Jul 2024 01:04:27 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d614447a37c0c99f43e28ec4c3e44d7cbcc9ec6230c1f36d209a99db556e86ef`  
		Last Modified: Fri, 12 Jul 2024 01:04:30 GMT  
		Size: 19.7 MB (19669372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.6054; amd64

```console
$ docker pull docker@sha256:4e4debc76e22017cf7304ec8f937133d9f6c29e70690ef7d9a3546d5f238beec
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2297153261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f3bafa245be7244edf9a1b99af64ed40431cde7b4defb730842408377e7190b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Fri, 12 Jul 2024 01:06:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 12 Jul 2024 01:07:46 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 12 Jul 2024 01:07:46 GMT
ENV DOCKER_VERSION=27.0.3
# Fri, 12 Jul 2024 01:07:47 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.0.3.zip
# Fri, 12 Jul 2024 01:08:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 12 Jul 2024 01:08:14 GMT
ENV DOCKER_BUILDX_VERSION=0.16.0
# Fri, 12 Jul 2024 01:08:15 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.windows-amd64.exe
# Fri, 12 Jul 2024 01:08:15 GMT
ENV DOCKER_BUILDX_SHA256=6521f85836e4bdc1347b38b9de32268ac09987e2c1ea0e424b0e07632ab61025
# Fri, 12 Jul 2024 01:08:40 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 12 Jul 2024 01:08:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.28.1
# Fri, 12 Jul 2024 01:08:41 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-windows-x86_64.exe
# Fri, 12 Jul 2024 01:08:42 GMT
ENV DOCKER_COMPOSE_SHA256=7dbd8848d9b8dce489c4d2ce1bb4f4b7a3dccb07a08596ae98b85091e1645bcc
# Fri, 12 Jul 2024 01:09:06 GMT
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
	-	`sha256:434dcc61458355544a47caaa5b8bf847ece6125e09f59156e7fafc0756a3bd1a`  
		Last Modified: Fri, 12 Jul 2024 01:09:14 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d82cab1ca448ff75ecb13363be2022e075aed9142585173a4c753ec9e55fecbf`  
		Last Modified: Fri, 12 Jul 2024 01:09:14 GMT  
		Size: 491.1 KB (491084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d79090806c046c70beeca9f9d2e8568d7867fac41798d405a122cd86fdb9f408`  
		Last Modified: Fri, 12 Jul 2024 01:09:12 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d444008e5e58a7453952eab9ec85720c69dd78c9487f3e339c861cba52f4f241`  
		Last Modified: Fri, 12 Jul 2024 01:09:13 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:853930b18086a6b53facc6dbebd0d3abc9ad2fe56050a3113cf1a40916547ead`  
		Last Modified: Fri, 12 Jul 2024 01:09:14 GMT  
		Size: 19.3 MB (19280330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ecd5e7ae5eb6b9a160e1746892395c0377fa7e76ca46f5655669690869da2a0`  
		Last Modified: Fri, 12 Jul 2024 01:09:11 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f603cd95a827520af43f943f8a6307b9c68a8e6baecc9ea29b6222411abd9c`  
		Last Modified: Fri, 12 Jul 2024 01:09:11 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c2b2c5bf51ed56893c9f993571d91b02529c95a3cf8572d2dc11a83ffdb1dda`  
		Last Modified: Fri, 12 Jul 2024 01:09:11 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca829aba4f0860779c5f58941e52537c77927b020a4825d3aaf58d1fb155d91b`  
		Last Modified: Fri, 12 Jul 2024 01:09:13 GMT  
		Size: 19.3 MB (19270563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e74043ae6d2d48589dbab20a5f93dd48887933e5d84754cdec692b7bd5275bf`  
		Last Modified: Fri, 12 Jul 2024 01:09:09 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f6578c771f9f25e95907dbbb3fd779815eae3d4c34d05e35a609f18074abb3`  
		Last Modified: Fri, 12 Jul 2024 01:09:10 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c079a1439fea30469b35eff133cc042a711bc657508389ef22e7f38a905973`  
		Last Modified: Fri, 12 Jul 2024 01:09:10 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a577774727222a8f750b4504e584f985ec41eed091a5f14a801667726afc54e`  
		Last Modified: Fri, 12 Jul 2024 01:09:12 GMT  
		Size: 19.7 MB (19670301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
