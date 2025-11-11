## `docker:29-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:640fb0eed94a4f803f7e799f959e7c8a1ca342a0c0c219abf7d7995586e241c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `docker:29-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull docker@sha256:547723ea04909125526cb23fb563a46f2301df0a926f022573f2b0621df0b552
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1835714555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6225acdf513d523a4e5f171654574cf1b2f06e39f7423c786533420be8ad7ae8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:35 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 11 Nov 2025 19:11:36 GMT
ENV DOCKER_VERSION=29.0.0
# Tue, 11 Nov 2025 19:11:36 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.0.zip
# Tue, 11 Nov 2025 19:11:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 19:11:51 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Tue, 11 Nov 2025 19:11:51 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Tue, 11 Nov 2025 19:11:52 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Tue, 11 Nov 2025 19:12:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 19:12:08 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 11 Nov 2025 19:12:09 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Tue, 11 Nov 2025 19:12:09 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Tue, 11 Nov 2025 19:12:32 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442760c8d26f9c34d441d655bfed0213774e9ee1491b0a9d451ba3951353bd99`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77379ef0e0e6736861441fc459538ec29a38e2695e5072007d019bd55c2fa950`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 497.9 KB (497949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:899bdb2c9a06e8c2bd2121c8f6f9737c19f54e7f844bbf73604a3f955247d131`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a997f06dcced75ecdce2c08dc44619e9b9de11091760c69018ec1de6dadc8315`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b071036fe41b378649b062f3a9d6a8501a432a05718e96d042145b4d0d31af4`  
		Last Modified: Tue, 11 Nov 2025 19:18:53 GMT  
		Size: 19.4 MB (19414195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe7a96e400b09393f86048b9d3b56db0ae7eacb0b20e85eccd2496fe5d26d99a`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5198f20bbc902ae2b9e919aa8f67bfb4994f46f9412d09affd43bdb5de4295e1`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e011cb046f9715e7264a714fff85c39cba7caf6d835e6da94de151a415a8d77`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9defe4698fab9ed347e44988419378e6b6bc431be8c5f520706fb34a4099e779`  
		Last Modified: Tue, 11 Nov 2025 19:18:55 GMT  
		Size: 23.2 MB (23158195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eaca05470ddd0a069854418864ae4c00f6bd02495ea14fbae2adeee5662a30a`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285f45b248227884bd5620c2513c0d53a44d08a7a074b2eaa6b45912824505e3`  
		Last Modified: Tue, 11 Nov 2025 19:18:52 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959d3b5c97ff7ce75236dee3b1b8cbdf540f062fb5eff8cfbc214609a9afd6e0`  
		Last Modified: Tue, 11 Nov 2025 19:18:52 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8886e8fb24b2ac72d10b24a72eaddcb7d21a66772414a2196be5e92e1d0107f1`  
		Last Modified: Tue, 11 Nov 2025 19:18:54 GMT  
		Size: 22.7 MB (22670905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
