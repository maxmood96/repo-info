## `docker:27-windowsservercore`

```console
$ docker pull docker@sha256:927b9de9aca0e5478c715a44cdf467aca9d841a4005a770a7aac031b7d84d029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2849; amd64
	-	windows version 10.0.17763.6532; amd64

### `docker:27-windowsservercore` - windows version 10.0.20348.2849; amd64

```console
$ docker pull docker@sha256:b4caa3a7f86e589c45dc6c46e1c838f54640d298dee20b8db779079e0a51dc28
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2311496896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c516d9b82a3d21ab2f93794e57937e48dc7b5e96d45c58ff7162d04f870f804`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Mon, 09 Dec 2024 20:30:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 09 Dec 2024 20:31:26 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 09 Dec 2024 20:31:27 GMT
ENV DOCKER_VERSION=27.4.0
# Mon, 09 Dec 2024 20:31:28 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.4.0.zip
# Mon, 09 Dec 2024 20:31:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 09 Dec 2024 20:31:46 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Mon, 09 Dec 2024 20:31:46 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.windows-amd64.exe
# Mon, 09 Dec 2024 20:31:47 GMT
ENV DOCKER_BUILDX_SHA256=6b13e5bdd8a40548886b69cc94716ff2f9a06db513983a0f158f80a3f2486432
# Mon, 09 Dec 2024 20:32:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 09 Dec 2024 20:32:03 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Mon, 09 Dec 2024 20:32:03 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-windows-x86_64.exe
# Mon, 09 Dec 2024 20:32:04 GMT
ENV DOCKER_COMPOSE_SHA256=93fa851954c19e0e19b753817eca37c81c9f4394b0db1853ebc66cd62230ea75
# Mon, 09 Dec 2024 20:32:13 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa234934db0c8d6901160e14d5d8b6af3a4edddf247c194d145abc9e11985b76`  
		Last Modified: Mon, 09 Dec 2024 20:32:23 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bfca828d7ce95d5a55206da494af464ceafebb7e55a0d009330334f09144dc`  
		Last Modified: Mon, 09 Dec 2024 20:32:23 GMT  
		Size: 370.2 KB (370242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7c93537ec0e3172e90fcab9641bc69dfb9543ccaea2d14f7393c8bfab5050e3`  
		Last Modified: Mon, 09 Dec 2024 20:32:21 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b8cc031198c46d9bee9f2d279736cf448a67c3afd907d6727226f4f5b91bf86`  
		Last Modified: Mon, 09 Dec 2024 20:32:21 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187ae01f8b9f66abc7b5244895f04801de03c029a7098bd4d9d65711f39d8dab`  
		Last Modified: Mon, 09 Dec 2024 20:32:23 GMT  
		Size: 19.0 MB (18973035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417791721e44c047a4bc60eb5bc560ae4d0f7d3784c6143ffdb0a69edc5d59c6`  
		Last Modified: Mon, 09 Dec 2024 20:32:19 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e57da3c3518c7bbbb172be1453ace63169d86fa3ed1a85b8f92f001f4c289e4`  
		Last Modified: Mon, 09 Dec 2024 20:32:19 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5098d0a0e66c5f36a1df760ac7bcec16672ba2f64caebfe9f39a9a3058be5a`  
		Last Modified: Mon, 09 Dec 2024 20:32:19 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0bb1f96b8110f0896c755513fcd0c1ca06cf15704f0dd427094a408a58c2f1e`  
		Last Modified: Mon, 09 Dec 2024 20:32:20 GMT  
		Size: 19.6 MB (19623141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98de0d04de34d056c3a1e65d777dccc5f63fb0d2f97f0fd9e8bb70dbcd117c49`  
		Last Modified: Mon, 09 Dec 2024 20:32:17 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:184e745eef5beae6d08573b560e57f0868aa774e058a763625a15f9f29b342dc`  
		Last Modified: Mon, 09 Dec 2024 20:32:17 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a40367f162ac52e4c2e9eec344275ab8c38bbef973093d60aa7ab30849d9c9`  
		Last Modified: Mon, 09 Dec 2024 20:32:17 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:396d7846ed0029d096574e3e9d7d94573541afcdc0b3840c835603a12143fa82`  
		Last Modified: Mon, 09 Dec 2024 20:32:20 GMT  
		Size: 20.0 MB (20034722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27-windowsservercore` - windows version 10.0.17763.6532; amd64

```console
$ docker pull docker@sha256:34a3818e44579ebd5532969744c01891c035713473b5e8efb2e076e6f181a401
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2069794651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e779874656926a0014f559d5327645d9f543b7409d265826be39321303731c94`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Mon, 09 Dec 2024 20:30:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 09 Dec 2024 20:30:57 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 09 Dec 2024 20:30:58 GMT
ENV DOCKER_VERSION=27.4.0
# Mon, 09 Dec 2024 20:30:59 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.4.0.zip
# Mon, 09 Dec 2024 20:31:16 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 09 Dec 2024 20:31:17 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Mon, 09 Dec 2024 20:31:17 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.windows-amd64.exe
# Mon, 09 Dec 2024 20:31:18 GMT
ENV DOCKER_BUILDX_SHA256=6b13e5bdd8a40548886b69cc94716ff2f9a06db513983a0f158f80a3f2486432
# Mon, 09 Dec 2024 20:31:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 09 Dec 2024 20:31:29 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Mon, 09 Dec 2024 20:31:30 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-windows-x86_64.exe
# Mon, 09 Dec 2024 20:31:30 GMT
ENV DOCKER_COMPOSE_SHA256=93fa851954c19e0e19b753817eca37c81c9f4394b0db1853ebc66cd62230ea75
# Mon, 09 Dec 2024 20:31:44 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eeb80b401d5fa455a03f11b3d1f88c06cdf985f6ad627459728be324bfc585e`  
		Last Modified: Mon, 09 Dec 2024 20:31:50 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3016ea1312cdd0cd970a43d9a303baa291dbb41d308e4ce71ebd0f93ac88ce88`  
		Last Modified: Mon, 09 Dec 2024 20:31:50 GMT  
		Size: 474.8 KB (474820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7238b73438c86a6f997db855b71bc46b906a9a2c589baf2475d7a11f6157b633`  
		Last Modified: Mon, 09 Dec 2024 20:31:49 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ee762d9dba7ffbca8d833c5e0228ef9630dc737758988b80d3fcc3423a7961`  
		Last Modified: Mon, 09 Dec 2024 20:31:49 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c616335483b748d1bae54085332c885730b9653bc7dc54d0b50d4688a1738a`  
		Last Modified: Mon, 09 Dec 2024 20:31:50 GMT  
		Size: 19.0 MB (18984472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:549bca78c781b86d2c0b32e46390703ab81213f2d401168dcafac9e7d3a12494`  
		Last Modified: Mon, 09 Dec 2024 20:31:48 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77fb57597c0fa0d79cfdef44fa5f7303a07bf1ef3f3780358aa911b1a104f922`  
		Last Modified: Mon, 09 Dec 2024 20:31:48 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a42a2d2720125633b40577fbb78d27a5ffbbe9062b07612fd595135a9d75938`  
		Last Modified: Mon, 09 Dec 2024 20:31:48 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a09524d0ab580dc3caa8bc2287cc3e0e3fa52ad2db8890210955b1fad52a36eb`  
		Last Modified: Mon, 09 Dec 2024 20:31:49 GMT  
		Size: 19.6 MB (19632421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f97462d84bb9ab796e16e054cf50cf2579a7cd9d7f86ba57ea2d1814d28da2`  
		Last Modified: Mon, 09 Dec 2024 20:31:47 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9316ba57ae879fded0589722ae1c413edeba19b8bdc53edcb14c1c3f8a9985d3`  
		Last Modified: Mon, 09 Dec 2024 20:31:47 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdd25ea4a4b133d3c050e82157e17cf5d761183b6fbfa81847aa7947eae19e8`  
		Last Modified: Mon, 09 Dec 2024 20:31:47 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf16db3915680cf9d485f21272ea7248ee1e9fd9443daeff2c99254290020dfd`  
		Last Modified: Mon, 09 Dec 2024 20:31:49 GMT  
		Size: 20.0 MB (20037504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
