## `docker:28-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:2b086a57dbe19285df38375e6c45a4d2ef9fc76140e8b1194e686ff0b9ff26cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3453; amd64

### `docker:28-windowsservercore-ltsc2022` - windows version 10.0.20348.3453; amd64

```console
$ docker pull docker@sha256:c52188ff30448d4bd564d8f5b9821e599c58cdd800b453fe4760f3b0389374b4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335786069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:169065c6e336a85a789634081269ab895679800173f02b40e3f800b244104d86`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 04 Apr 2025 23:10:04 GMT
RUN Install update 10.0.20348.3453
# Thu, 10 Apr 2025 21:52:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Apr 2025 21:53:09 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 10 Apr 2025 21:53:10 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 10 Apr 2025 21:53:10 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Thu, 10 Apr 2025 21:53:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 10 Apr 2025 21:53:22 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 10 Apr 2025 21:53:23 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Thu, 10 Apr 2025 21:53:23 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Thu, 10 Apr 2025 21:53:32 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 10 Apr 2025 21:53:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 10 Apr 2025 21:53:35 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-windows-x86_64.exe
# Thu, 10 Apr 2025 21:53:35 GMT
ENV DOCKER_COMPOSE_SHA256=bca44d55a7e612c53a80092661dd5db05aefb936e1eccd7ce06fdb02be7df3c3
# Thu, 10 Apr 2025 21:53:43 GMT
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
	-	`sha256:5f95096b5608a411135efc34fc2fe0da0466d02646c95e3b6ae95fc9887ed53b`  
		Last Modified: Thu, 10 Apr 2025 21:53:48 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88aa197bc0669175b1d1c5acdaf469c32f59443701487c42d1f02801bfb83c9`  
		Last Modified: Thu, 10 Apr 2025 21:53:48 GMT  
		Size: 345.4 KB (345367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6a6006c045633f47db8af9477117a47f2582e45a202e508b57ab1a75ed75f7`  
		Last Modified: Thu, 10 Apr 2025 21:53:47 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d64f0310308299511707465f30acaf6c95add396b2d76e7557126d57c6bb985f`  
		Last Modified: Thu, 10 Apr 2025 21:53:47 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d68f6d308fb6fdd144e545376f1e4ac15c28bb892bc022ec465ed3c634cc08`  
		Last Modified: Thu, 10 Apr 2025 21:53:49 GMT  
		Size: 19.9 MB (19851339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b05ff3f2922ee7a9c70c0700fdd72ccf69cb20fbf637ca1e03c1d015374b9249`  
		Last Modified: Thu, 10 Apr 2025 21:53:46 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4de9a1403666d61119175f2b9806715aab7954df4ba73476fcf99553ff7435d`  
		Last Modified: Thu, 10 Apr 2025 21:53:46 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce17988977b84093ba57ed292411e5ea3309fdb1fe7c2ea9aa0f49822443072f`  
		Last Modified: Thu, 10 Apr 2025 21:53:46 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390cd4355c718d539537a3e62ee22262ff6c08708110b21eabafdf8240b2c3e5`  
		Last Modified: Thu, 10 Apr 2025 21:53:48 GMT  
		Size: 22.8 MB (22754676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caeaff28ebe7ea21623dd172ef1672b8717716e9c62c465682886021d8a87920`  
		Last Modified: Thu, 10 Apr 2025 21:53:45 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c3e7e4d27e6723309b474f8112d6219ec766261d09f8eb6b3822bfb1cd70562`  
		Last Modified: Thu, 10 Apr 2025 21:53:45 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f408c0b2b794279d042fbe1be256e91efe6e1bd73afcbbb65ea94fc05d28c84`  
		Last Modified: Thu, 10 Apr 2025 21:53:45 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a63f5ad7cdd12edc8691d7c7993f1ee8f003f6b2af8cc1513722e744a9d338`  
		Last Modified: Thu, 10 Apr 2025 21:53:48 GMT  
		Size: 21.8 MB (21827318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
