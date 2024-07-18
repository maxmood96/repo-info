## `docker:25-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:a0ef259ff6d60f2287253b39db0892faaf3ce1ec89423363d8d3186918490f39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2582; amd64

### `docker:25-windowsservercore-ltsc2022` - windows version 10.0.20348.2582; amd64

```console
$ docker pull docker@sha256:06fb44bc8a8d65cfe2300d46cae3d37f7d99bd5cd4304e471ab94959ca62b855
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2196894601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:182b215138946463fcbc0a3fa87294ab7105da58c9e91d4e66da09932577fac5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 03 Jul 2024 10:07:02 GMT
RUN Install update 10.0.20348.2582
# Thu, 18 Jul 2024 18:55:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 18 Jul 2024 18:56:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 18 Jul 2024 18:56:34 GMT
ENV DOCKER_VERSION=25.0.5
# Thu, 18 Jul 2024 18:56:35 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-25.0.5.zip
# Thu, 18 Jul 2024 18:56:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 18 Jul 2024 18:56:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.0
# Thu, 18 Jul 2024 18:56:51 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.windows-amd64.exe
# Thu, 18 Jul 2024 18:56:52 GMT
ENV DOCKER_BUILDX_SHA256=6521f85836e4bdc1347b38b9de32268ac09987e2c1ea0e424b0e07632ab61025
# Thu, 18 Jul 2024 18:57:01 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 18 Jul 2024 18:57:02 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.0
# Thu, 18 Jul 2024 18:57:02 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-windows-x86_64.exe
# Thu, 18 Jul 2024 18:57:03 GMT
ENV DOCKER_COMPOSE_SHA256=3dc98cacf0e0a05d8a714cc729827c062ff7ec13ffcd626e7b3767b362ce9b65
# Thu, 18 Jul 2024 18:57:15 GMT
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
	-	`sha256:436dc12baed7c3c475f3b75f641ff7483ed77a98ca2fc2d207ee4ea1d089b898`  
		Last Modified: Thu, 18 Jul 2024 18:57:21 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72903abbd20207fe4dd5217bdc6e141572f440c7548f7e168fb7f8ad4671e9bd`  
		Last Modified: Thu, 18 Jul 2024 18:57:21 GMT  
		Size: 359.7 KB (359666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef5f36590e446da0a661774038385143f555e410db2b58fc95d1ac690fb8309`  
		Last Modified: Thu, 18 Jul 2024 18:57:20 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7433786b448eef846c49eee7864acef43dc28a20e58e7e4c1cf60bcb9315d0`  
		Last Modified: Thu, 18 Jul 2024 18:57:20 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1db1d0a162b5cdc372065420dd96c494c2ec58c6f91c8adb218187c98788c7e`  
		Last Modified: Thu, 18 Jul 2024 18:57:22 GMT  
		Size: 18.0 MB (18038603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b090f124ed8c9a0fc457bb865ddeb8f4e23e5667d4aaf9c252a3cd737f9c2f`  
		Last Modified: Thu, 18 Jul 2024 18:57:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6277b7f7bb3ee8f168f69bf632f7e665ee97a6a90beba4356d766cc6bce9923d`  
		Last Modified: Thu, 18 Jul 2024 18:57:19 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4dc6c8138b11bc2092ab087aeab284baab29fd122757eb772f370eec2f1b318`  
		Last Modified: Thu, 18 Jul 2024 18:57:19 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e6f3a225e63de9e062af5fbecd0461403f558e77aa38aefa4dead1d3e4ba10`  
		Last Modified: Thu, 18 Jul 2024 18:57:21 GMT  
		Size: 19.2 MB (19224917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c852a7f4142e1bd8420fcf60882ebc457e45abf2a01abbc6fb65912df0a905f`  
		Last Modified: Thu, 18 Jul 2024 18:57:18 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b29e6cf2ff099a4965584f2c96a2a15d2f8276126b9e036a351452445c003d`  
		Last Modified: Thu, 18 Jul 2024 18:57:18 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f20e510d502d1454c5cabfafe90f04c36e90acb19f32ffae09636adb63e58e61`  
		Last Modified: Thu, 18 Jul 2024 18:57:18 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c719e4a05ebf1db1dfad36dcb5e59d2c1c9bb558bcf885224c4ccdfecc7c45`  
		Last Modified: Thu, 18 Jul 2024 18:57:21 GMT  
		Size: 19.7 MB (19659331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
