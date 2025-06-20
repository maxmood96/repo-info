## `docker:28-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:28dc4818f2fe58b7e870dc8b31b8673ecf96e12865039607e1ac4bb708d88c3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `docker:28-windowsservercore-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull docker@sha256:dbdb6b3eba7542dc714f65a2d50a670e113cc991f0072599d0e610b8ea9f4c21
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3541992413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0b4aa76a97e3437fc5b474bdefa6ed6e2b60a7456b7392dadf76902bb9b91ae`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Fri, 20 Jun 2025 19:14:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 20 Jun 2025 19:14:17 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 20 Jun 2025 19:14:19 GMT
ENV DOCKER_VERSION=28.2.2
# Fri, 20 Jun 2025 19:14:21 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.2.zip
# Fri, 20 Jun 2025 19:14:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 20 Jun 2025 19:14:35 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Fri, 20 Jun 2025 19:14:37 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Fri, 20 Jun 2025 19:14:38 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Fri, 20 Jun 2025 19:14:53 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 20 Jun 2025 19:14:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.2
# Fri, 20 Jun 2025 19:14:57 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-windows-x86_64.exe
# Fri, 20 Jun 2025 19:14:59 GMT
ENV DOCKER_COMPOSE_SHA256=f52bba6d8031da7e01c5bcf621dadea0afa41a317be09f2946701e15e899f8a4
# Fri, 20 Jun 2025 19:15:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b61d8f1bb5129502a06cea04657715aa68d500a1dc0ddcf37003afcd263c28`  
		Last Modified: Tue, 10 Jun 2025 22:09:36 GMT  
		Size: 1.3 GB (1260866861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129e76bd81e48ef7f479f2b781e5598ac47548638656c893f7ab6c75e9ae030c`  
		Last Modified: Fri, 20 Jun 2025 19:18:47 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22d86d4f7c3e318d4b1072fc669c4b3399be2a2c60dfe3395fa88b26351cafc`  
		Last Modified: Fri, 20 Jun 2025 19:18:47 GMT  
		Size: 400.9 KB (400923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf7b8acb1659f14e2b1e771f868ec9e023012743f1510e149fc933ee94bebec`  
		Last Modified: Fri, 20 Jun 2025 19:18:48 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af82fc9b61f57b670fe556735dff10c6ef42cf0eab25160d8a887ff77fb87b75`  
		Last Modified: Fri, 20 Jun 2025 19:18:48 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8f5463e6be8b0bf5f0bea1ca96e55a8d50f70ee8e1829d9dbd9a5c9155f4fb`  
		Last Modified: Fri, 20 Jun 2025 19:18:52 GMT  
		Size: 20.5 MB (20490557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f68bf3064906bbbd0cc527b5591c0325c6773052e341283e0dae2dd507ea16c`  
		Last Modified: Fri, 20 Jun 2025 19:18:49 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd9b5e37dc9bff925156a4f9664a4708f3fe6fe830491106c2ab6a3af0ddab4`  
		Last Modified: Fri, 20 Jun 2025 19:18:52 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1530fd79d0f2d063eee8cd554d48278577e02e3ebaede1bc9b59a7a6041ba39b`  
		Last Modified: Fri, 20 Jun 2025 19:18:52 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8cf2732a66d3d11b0cdd7535e8809f280275d155d9cab97cd21bb1a9aabb220`  
		Last Modified: Fri, 20 Jun 2025 19:18:56 GMT  
		Size: 22.7 MB (22686812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f06b0a9540b560fa40cd95cc3159a3ef2f56c5bae30204fa9b87f76dd9a0b4`  
		Last Modified: Fri, 20 Jun 2025 19:18:53 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb06eb34b50c0ca8547f40dfc33cd837a1a80f9285b50486b42d34b9422fb9a`  
		Last Modified: Fri, 20 Jun 2025 19:18:53 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e4eabb30838afee41b28c7f31762bdf00046f1ffaf075c7e9a376cd49b0275`  
		Last Modified: Fri, 20 Jun 2025 19:18:54 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d5ade3119f60a944c95a1a54f161b60eea5cdd73cf9db6f1a799ae60c11857b`  
		Last Modified: Fri, 20 Jun 2025 19:18:58 GMT  
		Size: 22.2 MB (22228247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
