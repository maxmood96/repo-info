## `docker:windowsservercore`

```console
$ docker pull docker@sha256:10abbda5c2e9777082cf6fa1e76d9b3ad9e353117bfd518a8bcddc936a4d8aa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4349; amd64
	-	windows version 10.0.20348.3807; amd64

### `docker:windowsservercore` - windows version 10.0.26100.4349; amd64

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

### `docker:windowsservercore` - windows version 10.0.20348.3807; amd64

```console
$ docker pull docker@sha256:0070239b34a04c084f3ee4e657479cded9190ae381236faa454028290a978714
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2345807998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c23ce98f53b69074b6dd61452588606365c8a64c876173899f0a1680fdb67d5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Fri, 20 Jun 2025 19:08:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 20 Jun 2025 19:09:47 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 20 Jun 2025 19:09:47 GMT
ENV DOCKER_VERSION=28.2.2
# Fri, 20 Jun 2025 19:09:48 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.2.zip
# Fri, 20 Jun 2025 19:10:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 20 Jun 2025 19:10:09 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Fri, 20 Jun 2025 19:10:09 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Fri, 20 Jun 2025 19:10:10 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Fri, 20 Jun 2025 19:10:18 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 20 Jun 2025 19:10:18 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.2
# Fri, 20 Jun 2025 19:10:19 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-windows-x86_64.exe
# Fri, 20 Jun 2025 19:10:19 GMT
ENV DOCKER_COMPOSE_SHA256=f52bba6d8031da7e01c5bcf621dadea0afa41a317be09f2946701e15e899f8a4
# Fri, 20 Jun 2025 19:10:29 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135b66d2bd823902563cf69180b21f684c70c32ebde6cf9d0bb5d50d8d23c589`  
		Last Modified: Fri, 20 Jun 2025 19:10:43 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5232a14630eee850b5503e0068d01482303a0f28c9bcfa7d33598fc29b44f05e`  
		Last Modified: Fri, 20 Jun 2025 19:10:43 GMT  
		Size: 356.9 KB (356875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a166c72ebbcd2ec76368b7a8b5d3a74da6c0e0a28566a139db5cd52452bb796d`  
		Last Modified: Fri, 20 Jun 2025 19:10:43 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d3608a52d107367d42884e798affb8188be08dcb26f5252ff7370062bafede`  
		Last Modified: Fri, 20 Jun 2025 19:10:44 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72cced757c3fcebfaa3c75c0460af9972f28805f301771dada3447919f93c5ef`  
		Last Modified: Fri, 20 Jun 2025 19:10:45 GMT  
		Size: 20.4 MB (20418777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff67351edd1be1daa665dac2683f9cfe4d55a6e6677772c33688f8aa2111f3e5`  
		Last Modified: Fri, 20 Jun 2025 19:10:44 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253c7524d749b138faec0fdb53cab8e4537a4eb8dfff336afbff445485e38175`  
		Last Modified: Fri, 20 Jun 2025 19:10:44 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320b77c58d17f024ff5e90aae63d753f875628c3e1f7af744adff2e261b87e41`  
		Last Modified: Fri, 20 Jun 2025 19:10:45 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705d4446b45a1a46a36de0a0ddcba95996f926c19e031b592ac63f47098f45d1`  
		Last Modified: Fri, 20 Jun 2025 19:10:47 GMT  
		Size: 22.6 MB (22618592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f062ac0544c270b31aa73a0adfce067fa721a84ad2f41ad12784b1e70e18bb`  
		Last Modified: Fri, 20 Jun 2025 19:10:45 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aaecb6f0268c877d624a00ad822ff0fecd9bd82775ca1a1bc5328bcdfac79ef`  
		Last Modified: Fri, 20 Jun 2025 19:10:45 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1894444208e9c4f586cde4547b9dcdca19745d495fb00e12c24e57e2fab6a952`  
		Last Modified: Fri, 20 Jun 2025 19:10:45 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:999f02966556ddccc20538a2c2d58089924bfe56fc17ccb10e7db5396be67c43`  
		Last Modified: Fri, 20 Jun 2025 19:10:47 GMT  
		Size: 22.2 MB (22150578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
