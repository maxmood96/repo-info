## `docker:27-windowsservercore`

```console
$ docker pull docker@sha256:ce26a4b6892bb5fff408af70028fd1f7aadf1ba1817049f7c36d386b938f2a31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `docker:27-windowsservercore` - windows version 10.0.20348.2966; amd64

```console
$ docker pull docker@sha256:b59b50eddc96fa024759736642b20d31e812c747839aa0e04e6b3cd306d9c08f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2312956798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dac0ff62690131e5cbadefa8b3173ce78f2fedeb1bedfb9599c99488be059a9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Thu, 19 Dec 2024 06:27:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Dec 2024 06:28:34 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 19 Dec 2024 06:28:35 GMT
ENV DOCKER_VERSION=27.4.1
# Thu, 19 Dec 2024 06:28:36 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.4.1.zip
# Thu, 19 Dec 2024 06:28:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 19 Dec 2024 06:28:58 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Thu, 19 Dec 2024 06:28:59 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Thu, 19 Dec 2024 06:28:59 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Thu, 19 Dec 2024 06:29:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 19 Dec 2024 06:29:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Thu, 19 Dec 2024 06:29:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-windows-x86_64.exe
# Thu, 19 Dec 2024 06:29:12 GMT
ENV DOCKER_COMPOSE_SHA256=5dc7ac86e8d3972c2c68066c6ac370daf0a42b7c8d3338336c9dbde34af06213
# Thu, 19 Dec 2024 06:29:24 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d7502a1bbe13300d252a2f9df8e505261a1640bc1bd25b0948e9c00fcc5b01`  
		Last Modified: Thu, 19 Dec 2024 06:29:29 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14c5b28592218521960824b8276896946f244fbb3651810d08c43452a2582cb`  
		Last Modified: Thu, 19 Dec 2024 06:29:29 GMT  
		Size: 357.3 KB (357322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6330b409518a6d4ccfc671760fb4c29c3aa61745511abc8406e7598afdeb72f4`  
		Last Modified: Thu, 19 Dec 2024 06:29:29 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff2da6ec5d910a6c45c3b7bc2ada4de7ee595addaae450cfea2ba3fba3571f0`  
		Last Modified: Thu, 19 Dec 2024 06:29:28 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981fcf2dca12be8aa09825096e39af48ab18642d75e6e2791014b5511999719c`  
		Last Modified: Thu, 19 Dec 2024 06:29:30 GMT  
		Size: 19.0 MB (18965788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559ffe22c82820dbe4c523868249c3f6a55385142d2e0ead71e852d8a7251d56`  
		Last Modified: Thu, 19 Dec 2024 06:29:27 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458e70a57b4ce24dfc2a913ab05c3222397fe2e8a5d93868622a5da7a9340e81`  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04dd3b199caac21501453ed73a1b07e07e8909c492da3b0c12264e12be24f8f7`  
		Last Modified: Thu, 19 Dec 2024 06:29:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffced5034da239bcce196f61166f31fa32a1046a0b90925f73df0a56a4540555`  
		Last Modified: Thu, 19 Dec 2024 06:29:29 GMT  
		Size: 19.6 MB (19615775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d1d24e414a381ae30c27fae03be0f84206adbad1d9b6b30407bfecceb5e1e5`  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deeb14568d7a7f723c99e08a5b860258c0e121c9b475c7f14d316ac30cb06d68`  
		Last Modified: Thu, 19 Dec 2024 06:29:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a34da183fbb7bde6f718a61627a8077978264175188a7e437d8f791c46033e`  
		Last Modified: Thu, 19 Dec 2024 06:29:26 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bdb77e5d84cc05ce04533280006424bb2742fe825cfe58eb5f5934b7a430dcf`  
		Last Modified: Thu, 19 Dec 2024 06:29:29 GMT  
		Size: 20.1 MB (20132656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27-windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull docker@sha256:c442ec204cc8c3af89a231557d7113d731304aa9004ecc2fd2b7fdea9a2a5ed5
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2073460288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd24b1732cd2a56ef18bd248405211562b17b3b25cc385edc36040b8cea00146`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Thu, 19 Dec 2024 06:27:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Dec 2024 06:28:36 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 19 Dec 2024 06:28:36 GMT
ENV DOCKER_VERSION=27.4.1
# Thu, 19 Dec 2024 06:28:37 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.4.1.zip
# Thu, 19 Dec 2024 06:29:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 19 Dec 2024 06:29:00 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Thu, 19 Dec 2024 06:29:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Thu, 19 Dec 2024 06:29:01 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Thu, 19 Dec 2024 06:29:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 19 Dec 2024 06:29:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Thu, 19 Dec 2024 06:29:15 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-windows-x86_64.exe
# Thu, 19 Dec 2024 06:29:16 GMT
ENV DOCKER_COMPOSE_SHA256=5dc7ac86e8d3972c2c68066c6ac370daf0a42b7c8d3338336c9dbde34af06213
# Thu, 19 Dec 2024 06:29:30 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1cfd0430e259e32b94429bf581ea5f74b25080ea9e68899e17062c55bfdba4f`  
		Last Modified: Thu, 19 Dec 2024 06:29:35 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:089d2b012e4350683f7592078e0330072d47face607cfdcfa1b177015a1d055d`  
		Last Modified: Thu, 19 Dec 2024 06:29:35 GMT  
		Size: 475.3 KB (475261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e54e6e8f743b8e62247f614caa153507aeea30e39ec7d133b120770472d150d`  
		Last Modified: Thu, 19 Dec 2024 06:29:34 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c46ebe5f7bc661958c2410ed2a60431be6d40269618a1223f8bc2c1f5392c26`  
		Last Modified: Thu, 19 Dec 2024 06:29:34 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac2d753848f2b9292c76be0e8c43f38d7c04ed25979be15179b781a3c2b47b9`  
		Last Modified: Thu, 19 Dec 2024 06:29:36 GMT  
		Size: 19.0 MB (18997863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4c651853f033dafb87a17fdd7690c1c3c3a0f4dfb6e083cf06ba8d91234d98`  
		Last Modified: Thu, 19 Dec 2024 06:29:33 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1a3389962e8b333bfcead93ec3aad31713a4bafd7b7be628b737077da7d60b`  
		Last Modified: Thu, 19 Dec 2024 06:29:33 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e030ce22f45d6c461af01d11e768dcd4638cd9b989e6dc8aa7e384b7ccb80129`  
		Last Modified: Thu, 19 Dec 2024 06:29:33 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d987b1383b6b76eb88c20a38bac7e305fe1f8c311242b83bc819be0eee3eb3`  
		Last Modified: Thu, 19 Dec 2024 06:29:35 GMT  
		Size: 19.6 MB (19648080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e0d2a17e8fa800de7106ca7d9cce51ab9562558d2d155ddfaaa0d979138750`  
		Last Modified: Thu, 19 Dec 2024 06:29:32 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d9b36807cefb176cc3c814de379c2bf6a17663ed8e0372f69d2cb06a02cd4e`  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f2c79cb8ac15f188f4afd8366afee1f46ec780fa70082a4c9e991ac09c8537`  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f72ede2a361313c0a7e7b059df25505b175cc277540b12cb48ee012d5a4ba93`  
		Last Modified: Thu, 19 Dec 2024 06:29:35 GMT  
		Size: 20.2 MB (20157227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
