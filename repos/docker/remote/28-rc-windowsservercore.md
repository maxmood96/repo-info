## `docker:28-rc-windowsservercore`

```console
$ docker pull docker@sha256:1316d317787a8d7ecf2e915c34120d9977aa5bb776b59d5fba85ba42df25a013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `docker:28-rc-windowsservercore` - windows version 10.0.26100.2894; amd64

```console
$ docker pull docker@sha256:45f02f57befcb8b83a58c4cdb4a8a0cbeff4a6a87f2fa7866f877e455110a240
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2563528458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295569d18a4cf9a52f94effd4819fe569efe8a62aa88b53f222f8d5cc7b84888`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Wed, 12 Feb 2025 23:30:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Feb 2025 23:30:36 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Feb 2025 23:30:37 GMT
ENV DOCKER_VERSION=28.0.0-rc.1
# Wed, 12 Feb 2025 23:30:37 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.0.0-rc.1.zip
# Wed, 12 Feb 2025 23:30:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 12 Feb 2025 23:30:47 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Wed, 12 Feb 2025 23:30:48 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.windows-amd64.exe
# Wed, 12 Feb 2025 23:30:48 GMT
ENV DOCKER_BUILDX_SHA256=39f53ec70c6ce37beca6898809e8eb89a77a1651be35ea50b51629c7a5d3b1f2
# Wed, 12 Feb 2025 23:30:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 12 Feb 2025 23:30:57 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Wed, 12 Feb 2025 23:30:57 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-windows-x86_64.exe
# Wed, 12 Feb 2025 23:30:58 GMT
ENV DOCKER_COMPOSE_SHA256=1324e382e1a79efaee4be288aae847f8a2862acf270d5621c17dff3a10d5ee83
# Wed, 12 Feb 2025 23:31:06 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Wed, 22 Jan 2025 06:04:03 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:057121d01fc4103678adf89d3e8bf50fc883dc3f05807fd3a3ff11ec2587d263`  
		Last Modified: Thu, 13 Feb 2025 00:29:58 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a97148e613d6335e03cb3cea6f4544634135a8645ccabf05d1f17f0f5d0e14c`  
		Last Modified: Thu, 13 Feb 2025 00:30:00 GMT  
		Size: 383.9 KB (383882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a85939f5a310c1cf2f2569230ca238aa7807981a5a162ae94f529e36bc188f77`  
		Last Modified: Thu, 13 Feb 2025 00:30:00 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17dae3c1df07726357d6be5783bb0a7601e01a6d2c5a62be4028711f58c49d1a`  
		Last Modified: Thu, 13 Feb 2025 00:30:00 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5796719a96975887c922ffde447e1baa078fb25297b4089f2563fef06eaf0974`  
		Last Modified: Thu, 13 Feb 2025 00:30:01 GMT  
		Size: 19.8 MB (19813120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a44acd42dc64c89267ff1afbe3230d3147d0fdca438189db6c57a44e97a02f`  
		Last Modified: Thu, 13 Feb 2025 00:30:00 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d93d086a2dd653b369f7c07ca90b29b22e2c4ee15345877f3f2559b45f00ffa`  
		Last Modified: Thu, 13 Feb 2025 00:30:01 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e86bf307571a0ed97fdf5bdc2ad2bddf2d7b76de9f5e53b40b3dc7316be964`  
		Last Modified: Thu, 13 Feb 2025 00:30:01 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f38fdd1ae58583d6753236908b3dde44cbd47835b42f5e5fdd7d9487eb5b1684`  
		Last Modified: Thu, 13 Feb 2025 00:30:03 GMT  
		Size: 21.2 MB (21178458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e85cd36b34dd776091b362b954823c8c7724e53f59df8d3d9780151c1f8e74e8`  
		Last Modified: Thu, 13 Feb 2025 00:30:02 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b71898f5f80f82c1385ba58c91f70e7dca60a84fe3e4c22d51fb4befe1c656`  
		Last Modified: Thu, 13 Feb 2025 00:30:02 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9c7f559a710fe803707784b7e69859af752081a26edd0c7866c1eb979b6607`  
		Last Modified: Thu, 13 Feb 2025 00:30:02 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b7718754a049fda761cc738871841ed48b9e9be5703aed56c2936c7bb32c09`  
		Last Modified: Thu, 13 Feb 2025 00:30:03 GMT  
		Size: 21.9 MB (21863677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-rc-windowsservercore` - windows version 10.0.20348.3207; amd64

```console
$ docker pull docker@sha256:c3528a5260a7ef9d801d994685367622cc3f8e40efbadc45b2cdeb898c924680
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2326998223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6283f5f927780e1359f20bbd6eccaa890f193427cac585c8a0938ea82c1f55ac`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 13 Feb 2025 00:36:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:36:27 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 13 Feb 2025 00:36:28 GMT
ENV DOCKER_VERSION=28.0.0-rc.1
# Thu, 13 Feb 2025 00:36:28 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.0.0-rc.1.zip
# Thu, 13 Feb 2025 00:36:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 13 Feb 2025 00:36:40 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Thu, 13 Feb 2025 00:36:41 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.windows-amd64.exe
# Thu, 13 Feb 2025 00:36:42 GMT
ENV DOCKER_BUILDX_SHA256=39f53ec70c6ce37beca6898809e8eb89a77a1651be35ea50b51629c7a5d3b1f2
# Thu, 13 Feb 2025 00:36:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 13 Feb 2025 00:36:51 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Thu, 13 Feb 2025 00:36:52 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-windows-x86_64.exe
# Thu, 13 Feb 2025 00:36:52 GMT
ENV DOCKER_COMPOSE_SHA256=1324e382e1a79efaee4be288aae847f8a2862acf270d5621c17dff3a10d5ee83
# Thu, 13 Feb 2025 00:37:01 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Wed, 12 Feb 2025 22:14:21 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ac7c3f547de34fd9bf00fcc0acbb7d99c09c97f80242e08eca14fb406e5bc8`  
		Last Modified: Thu, 13 Feb 2025 03:09:29 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38ddf0d7c03cfbc51a4e00937b9b77959e6d8c26215d9a2a2987385ff45531d`  
		Last Modified: Thu, 13 Feb 2025 03:09:29 GMT  
		Size: 368.5 KB (368547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ab8f8392f7709526f276d8c58f97688ac2b23273c0048f8d6bc901cbc22eb65`  
		Last Modified: Thu, 13 Feb 2025 03:09:29 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3347c93e4c2c236997831be12321f7cf7f6044640cbb912f81611b8573353b2`  
		Last Modified: Thu, 13 Feb 2025 03:09:29 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:381e41a674db7d06a451f3228ad05be17bd83f598d033fea6eb201bcc9b81cc9`  
		Last Modified: Thu, 13 Feb 2025 03:09:31 GMT  
		Size: 19.8 MB (19782456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9880e0e2dcdd71624e27a48d65392bbf66eb32e8cd2957f7b2c31f41c0325b5`  
		Last Modified: Thu, 13 Feb 2025 03:09:29 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc77ea84b5c02b3d6416f74d1235c133153de5de9cff7ef0bac8c475dcf2b0a`  
		Last Modified: Thu, 13 Feb 2025 03:09:29 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4279c929b864aff301204e36cea50ae5ac456de370c20be859be3debea2241`  
		Last Modified: Thu, 13 Feb 2025 03:09:29 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b61f5c8582fa5cc8df2420a058798379b40d2f1f6e2831bd2432fa5ef46bb8b2`  
		Last Modified: Thu, 13 Feb 2025 03:09:31 GMT  
		Size: 21.1 MB (21148123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1569aab3fcb826e92ddb614e616caa03787fe24c0b0d5414c247be0001b479ec`  
		Last Modified: Thu, 13 Feb 2025 03:09:29 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d4eb62c5675390de98ac3d412ba1f5573825db449d7b1b6985daf1299267fe`  
		Last Modified: Thu, 13 Feb 2025 03:09:29 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:057c73dce9d693ce24d3408d978d172083d59eb74de89e26577414cb9bce5fc6`  
		Last Modified: Thu, 13 Feb 2025 03:09:30 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d999fcee4253d74d2e11796f967ebff702f62c4aea4004d9573535716b8b3235`  
		Last Modified: Thu, 13 Feb 2025 03:09:32 GMT  
		Size: 21.8 MB (21829539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-rc-windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull docker@sha256:06a79cffaf68da7926340d24f845fed320e9b64a7665900d4f3a658f405722bd
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2199991818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cf536d35ae666d87e1e0cfe20748723083eaeef7c27cb3e48c587ce7311ee8c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:35:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:36:29 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 13 Feb 2025 00:36:29 GMT
ENV DOCKER_VERSION=28.0.0-rc.1
# Thu, 13 Feb 2025 00:36:30 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.0.0-rc.1.zip
# Thu, 13 Feb 2025 00:36:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 13 Feb 2025 00:36:43 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Thu, 13 Feb 2025 00:36:43 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.windows-amd64.exe
# Thu, 13 Feb 2025 00:36:44 GMT
ENV DOCKER_BUILDX_SHA256=39f53ec70c6ce37beca6898809e8eb89a77a1651be35ea50b51629c7a5d3b1f2
# Thu, 13 Feb 2025 00:36:52 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 13 Feb 2025 00:36:53 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Thu, 13 Feb 2025 00:36:54 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-windows-x86_64.exe
# Thu, 13 Feb 2025 00:36:54 GMT
ENV DOCKER_COMPOSE_SHA256=1324e382e1a79efaee4be288aae847f8a2862acf270d5621c17dff3a10d5ee83
# Thu, 13 Feb 2025 00:37:03 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 22:29:28 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4744c3deb7b0b1d3f73097efb8605ad7bc1e941ec01a931aa2a97912359064`  
		Last Modified: Thu, 13 Feb 2025 03:09:35 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:725d9f5f9555ce801b3f3893ceb61bf76e797d392ec7e25267f5d060f28b80b9`  
		Last Modified: Thu, 13 Feb 2025 03:09:35 GMT  
		Size: 345.1 KB (345141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ee6b84b196406beb2b27cc661bc230baa83a1b0f1ae2e511369eed9f96be72`  
		Last Modified: Thu, 13 Feb 2025 03:09:35 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eb3e79be924c98aba3ba8112f16a6b2e6c8b34afdd869c1a2e9b0dc9852aed0`  
		Last Modified: Thu, 13 Feb 2025 03:09:35 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8ef434a7dce698dd2e4c2b8022fa086933e72d19da2e141af2ad423e525dce`  
		Last Modified: Thu, 13 Feb 2025 03:09:37 GMT  
		Size: 19.8 MB (19772525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c150dd7cb9e15b3f07bebff1e0c9449ee9a894a3f85b9d38fa4e31b752af9808`  
		Last Modified: Thu, 13 Feb 2025 03:09:35 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d1f12873ef1acfc6cfd03ad66fb9a471f0cd82c0c01455cfbb7b19084a01d8`  
		Last Modified: Thu, 13 Feb 2025 03:09:36 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ddd950211f965779fc2b9a8daf81948ebb9452b4ebdf7da7f09ede59b849767`  
		Last Modified: Thu, 13 Feb 2025 03:09:35 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39bc156f4fd48cda0f3da6ea579ccf40bb38784f6796cad7ea1ceb5ea5ea5a91`  
		Last Modified: Thu, 13 Feb 2025 03:09:38 GMT  
		Size: 21.1 MB (21138227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2327512adfc75585b198cf66a7f0d6522c9d2619288b4417fef0077d2145c33`  
		Last Modified: Thu, 13 Feb 2025 03:09:35 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d81f2d6c8458fe74a35abfe34ff2bda06bf100fcf3c706b0a83bace3fdc98d0`  
		Last Modified: Thu, 13 Feb 2025 03:09:36 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f12f5bad9a67f336fd3f4138c09542665a9c36569648739ae4754422dcb369`  
		Last Modified: Thu, 13 Feb 2025 03:09:36 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ce536efa2be640d3253db0f0f6ef0aa3ab5e21c78032bbc64395d746d6aff5`  
		Last Modified: Thu, 13 Feb 2025 03:09:39 GMT  
		Size: 21.8 MB (21815437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
