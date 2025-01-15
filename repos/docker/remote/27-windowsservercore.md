## `docker:27-windowsservercore`

```console
$ docker pull docker@sha256:3dc453c179e8242a7449e4f8028145e010292915e3230b76aae64d82b49486e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `docker:27-windowsservercore` - windows version 10.0.20348.3091; amd64

```console
$ docker pull docker@sha256:65abbf8e57dc9b9317388e7635b591c02a450877d39a6776468c9329c6f0b244
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2321679678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5d69e1dda4a11c5d64215052395e362481548cde33a8d6a4be0b4b125f4b53`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Tue, 14 Jan 2025 23:30:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:30:49 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Jan 2025 23:30:49 GMT
ENV DOCKER_VERSION=27.5.0
# Tue, 14 Jan 2025 23:30:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Tue, 14 Jan 2025 23:30:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 23:31:00 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Tue, 14 Jan 2025 23:31:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Tue, 14 Jan 2025 23:31:01 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Tue, 14 Jan 2025 23:31:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 23:31:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Tue, 14 Jan 2025 23:31:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-windows-x86_64.exe
# Tue, 14 Jan 2025 23:31:11 GMT
ENV DOCKER_COMPOSE_SHA256=67a0c3ca2fd94c74982917c8bdf54465367fc3a8c0cb17c529eb6525d32b1674
# Tue, 14 Jan 2025 23:31:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e42393aec052ef4ad419b20811d5f8f1f4cef5ae7d1b6da49d51a64a7bded4a`  
		Last Modified: Tue, 14 Jan 2025 23:31:30 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:273b7e9f3e3d8546b60d078c2152236a9749ecd2ce4b8677348fe2d97b5798be`  
		Last Modified: Tue, 14 Jan 2025 23:31:30 GMT  
		Size: 341.3 KB (341285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1cbb7d5116a553e19e688cc78072e8b1eb29afb0b5be4644ed522bf083acd3f`  
		Last Modified: Tue, 14 Jan 2025 23:31:28 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45bfc86e47da2a329fa916e619f50b1572e090a406c11b35b6235548d8bc52ee`  
		Last Modified: Tue, 14 Jan 2025 23:31:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf3634f4abc247a49927973cdf069a2717f0053ec34fae55d8f7014967864fb`  
		Last Modified: Tue, 14 Jan 2025 23:31:30 GMT  
		Size: 19.1 MB (19149523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36028f38b9d36c2624a31329c881064c7c9b02472ec1aecfb6924bd39ef2450`  
		Last Modified: Tue, 14 Jan 2025 23:31:26 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0cfd1d3174eb2bbbce2d334d4fd0e90cdd7ca8747f146ef6da5a8cf8e937a3`  
		Last Modified: Tue, 14 Jan 2025 23:31:26 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834b9a7619d4a8f64af8850acc540189ba984e6f829cde434c43eaa00ac13251`  
		Last Modified: Tue, 14 Jan 2025 23:31:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde3f31a6ef2d6c5cb116f4c7246bdcf8ed9a39ac3ea376b13832a9a90df8d63`  
		Last Modified: Tue, 14 Jan 2025 23:31:27 GMT  
		Size: 19.6 MB (19634023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7331fb5fa54eb509667e318fef4224b22e7267a8b01ab08320597309a61cc9`  
		Last Modified: Tue, 14 Jan 2025 23:31:24 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41addc9937b80bc18e288c60f1f057cce9b501761a6c845a8a385dca9084663e`  
		Last Modified: Tue, 14 Jan 2025 23:31:24 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:752c051f71c979cefbe564869be494631945a5cd1aad02a5904c2715b12c51b0`  
		Last Modified: Tue, 14 Jan 2025 23:31:24 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dff165c12cf41f3471c535f13b2fefdaf7f686d0bc74b8372caf2d7dbb7a08f`  
		Last Modified: Tue, 14 Jan 2025 23:31:27 GMT  
		Size: 20.2 MB (20158014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27-windowsservercore` - windows version 10.0.17763.6775; amd64

```console
$ docker pull docker@sha256:e623df1460d3ebcb3ad8073621cc95b69f52df75ca8d0ab278177ef2085183d4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2181418375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3edf4c3deefe7cfd0ff52fd0d9d60c10b8e24d2facaaff9e581b0bed9b8c7cdc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Tue, 14 Jan 2025 23:37:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:38:50 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Jan 2025 23:38:50 GMT
ENV DOCKER_VERSION=27.5.0
# Tue, 14 Jan 2025 23:38:51 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Tue, 14 Jan 2025 23:39:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 23:39:04 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Tue, 14 Jan 2025 23:39:05 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Tue, 14 Jan 2025 23:39:05 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Tue, 14 Jan 2025 23:39:13 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 23:39:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Tue, 14 Jan 2025 23:39:14 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-windows-x86_64.exe
# Tue, 14 Jan 2025 23:39:15 GMT
ENV DOCKER_COMPOSE_SHA256=67a0c3ca2fd94c74982917c8bdf54465367fc3a8c0cb17c529eb6525d32b1674
# Tue, 14 Jan 2025 23:39:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace576e2b330b24c982543035820a2ecbea8fa58428209b788c8dbc34fe43f5e`  
		Last Modified: Tue, 14 Jan 2025 23:39:28 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d288a76c5d5ee64affc87ec0d46e06ebb6326b17068f33a5792bf7f16641fe84`  
		Last Modified: Tue, 14 Jan 2025 23:39:27 GMT  
		Size: 316.6 KB (316613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d7033573b703663b78be30fbeb8df368a1408341870dee01f3801334d22fdf`  
		Last Modified: Tue, 14 Jan 2025 23:39:27 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200e4ef96719afb123d542fba348a35d1e6b8c7ea5da1d183af90ff0537d8adf`  
		Last Modified: Tue, 14 Jan 2025 23:39:26 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0f7834de3577810e21557605584283e758ff40eae06e414866571f6c2e16df`  
		Last Modified: Tue, 14 Jan 2025 23:39:29 GMT  
		Size: 19.1 MB (19132926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8cc1331cde43f073663e2b9396edd7ccac0f5309292d4f046cbe985d4402471`  
		Last Modified: Tue, 14 Jan 2025 23:39:26 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff86dabfa389add56b99fda4a391700fa18ff5756120341345a47f98a2802312`  
		Last Modified: Tue, 14 Jan 2025 23:39:25 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf8192f34e31a6709287fc3944570a104c942154cde3b91498b2afc544cf1bde`  
		Last Modified: Tue, 14 Jan 2025 23:39:25 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3253d8429e17a419d9f3970970cec0e25ea529d22e9b1f46d68195ccd2ddf9`  
		Last Modified: Tue, 14 Jan 2025 23:39:27 GMT  
		Size: 19.6 MB (19607700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb691e1b2ced8da219bfba3fd2da38afd59e2d41d524d5f93ff610894aab74c`  
		Last Modified: Tue, 14 Jan 2025 23:39:24 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37177f635ff92a20fc9c2edee74a5d7fef05bac391f1261da856a52900a7d2f`  
		Last Modified: Tue, 14 Jan 2025 23:39:24 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e7ed4e2f131f942a5e8a2b6add2e3585ef60fff72094fffe47b43c98ff50f5`  
		Last Modified: Tue, 14 Jan 2025 23:39:25 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c0912a92c0e5091e90b6472cd2d2c89be81d415d84cc5426d62c54b147fdd1`  
		Last Modified: Tue, 14 Jan 2025 23:39:27 GMT  
		Size: 20.1 MB (20137257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
