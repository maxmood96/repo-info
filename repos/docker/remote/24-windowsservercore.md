## `docker:24-windowsservercore`

```console
$ docker pull docker@sha256:afccd00cf13ffc16d111c33afd35cee45fb510f4f65f066569ecb3f37085d80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2340; amd64
	-	windows version 10.0.17763.5576; amd64

### `docker:24-windowsservercore` - windows version 10.0.20348.2340; amd64

```console
$ docker pull docker@sha256:c22852bc3ad353866ee030560efa47cdc8e4a0652fd49d62efb01959f2988a60
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2013865366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3fe8386603d2115c959bdf7114d2dfbbc87d38ddd359f659b3fd557f0c4e90`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Mon, 25 Mar 2024 19:12:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Mar 2024 19:12:41 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 25 Mar 2024 19:12:41 GMT
ENV DOCKER_VERSION=24.0.9
# Mon, 25 Mar 2024 19:12:42 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.9.zip
# Mon, 25 Mar 2024 19:12:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 25 Mar 2024 19:12:55 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Mon, 25 Mar 2024 19:12:55 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.windows-amd64.exe
# Mon, 25 Mar 2024 19:12:56 GMT
ENV DOCKER_BUILDX_SHA256=6b113e84cbc3cd645646aa82f00a7f7d3737cc10375b4341e0aca0de0c997c75
# Mon, 25 Mar 2024 19:13:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 25 Mar 2024 19:13:08 GMT
ENV DOCKER_COMPOSE_VERSION=2.26.0
# Mon, 25 Mar 2024 19:13:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-windows-x86_64.exe
# Mon, 25 Mar 2024 19:13:09 GMT
ENV DOCKER_COMPOSE_SHA256=0a9a63442f50b494e8c5b6b1af9da138d9dbbeab094e3076747a709a470bb9e9
# Mon, 25 Mar 2024 19:13:19 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:642dd40899ef03447ebdd7600fd873e9a2e62771376e2c042f1949b6d02bce5e`  
		Last Modified: Mon, 25 Mar 2024 19:13:28 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7de4d9db792b62c2c84804893ed5630a3a7763eb1844d95c3b3b6cad1625388`  
		Last Modified: Mon, 25 Mar 2024 19:13:29 GMT  
		Size: 499.5 KB (499515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b32bef399c684ff7aeeb12696797f51f8154c473a06f4e3a888c03c816310a9e`  
		Last Modified: Mon, 25 Mar 2024 19:13:28 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18bfd96c786bcd3bb2a2dabd30654fc2eb52b2857228fd95a9529e6d98070bbd`  
		Last Modified: Mon, 25 Mar 2024 19:13:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95d1444e9d01d27cc9d3c0507c2e49195b6e6fe903f4c2db20cbc7c42da08f8`  
		Last Modified: Mon, 25 Mar 2024 19:13:29 GMT  
		Size: 17.5 MB (17532328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d3564dcfdac482734b18f8ea02608568246462b273f4fad8a8a90d3d5a60265`  
		Last Modified: Mon, 25 Mar 2024 19:13:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ea763a7057b2161a62dc3e0de1967bace5f0053c0ceba62340dc761140d95a`  
		Last Modified: Mon, 25 Mar 2024 19:13:26 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21915704eca3534abf3d3ffcf0e1495726e0a94ef8647d36ea8d7ae8e66d864e`  
		Last Modified: Mon, 25 Mar 2024 19:13:25 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdb70cebc47969f07d676040fedf6e71c94732a46d0cb482d7a1d1686c6e3f7`  
		Last Modified: Mon, 25 Mar 2024 19:13:26 GMT  
		Size: 18.8 MB (18829243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d2b6e04662f71c9e9322ff737ed4da98fa3f352ce1884ec9d2366d48036295`  
		Last Modified: Mon, 25 Mar 2024 19:13:23 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1400f8bad44a7574ec31f5f8703f271b5e49ac8517497b053623f7af00dfa603`  
		Last Modified: Mon, 25 Mar 2024 19:13:23 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:003656648668a7ccaeab4f6e4309b1489f8a9bba5b013c613782d03b50b29f5e`  
		Last Modified: Mon, 25 Mar 2024 19:13:23 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e50a7c2b4ed775ceab9bfc45e0ef797119188e568225bf125a9a01c2e3486d`  
		Last Modified: Mon, 25 Mar 2024 19:13:26 GMT  
		Size: 19.5 MB (19533656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:24-windowsservercore` - windows version 10.0.17763.5576; amd64

```console
$ docker pull docker@sha256:ad23a7fcb656ead37a465545e9388325b601358ff7ef291e1283f8fa58e454a5
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2181478466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52539df5ed369dabf38f7cb8c36fbac185b9d90f181218440e92ab7608d2e20`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Mon, 25 Mar 2024 19:12:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Mar 2024 19:14:06 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 25 Mar 2024 19:14:06 GMT
ENV DOCKER_VERSION=24.0.9
# Mon, 25 Mar 2024 19:14:07 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.9.zip
# Mon, 25 Mar 2024 19:14:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 25 Mar 2024 19:14:41 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Mon, 25 Mar 2024 19:14:42 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.windows-amd64.exe
# Mon, 25 Mar 2024 19:14:42 GMT
ENV DOCKER_BUILDX_SHA256=6b113e84cbc3cd645646aa82f00a7f7d3737cc10375b4341e0aca0de0c997c75
# Mon, 25 Mar 2024 19:15:16 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 25 Mar 2024 19:15:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.26.0
# Mon, 25 Mar 2024 19:15:18 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-windows-x86_64.exe
# Mon, 25 Mar 2024 19:15:19 GMT
ENV DOCKER_COMPOSE_SHA256=0a9a63442f50b494e8c5b6b1af9da138d9dbbeab094e3076747a709a470bb9e9
# Mon, 25 Mar 2024 19:15:48 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d897d01a892bf86c21bd91068ff3a1e0978a09c67a201bf8ff0b1503a1bf84f8`  
		Last Modified: Mon, 25 Mar 2024 19:15:58 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db60d9049fcc1a1671565962ad9981c481db355f7b3f64cdfce1f01a21aea32`  
		Last Modified: Mon, 25 Mar 2024 19:15:58 GMT  
		Size: 484.7 KB (484696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f917105d6c8c6f3233e917138d86c53ed75c20834e37007ce2d45eab49d71c2`  
		Last Modified: Mon, 25 Mar 2024 19:15:56 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e246cc5013e2058644d08049874602e73e3882517652259569ddd33f636594b`  
		Last Modified: Mon, 25 Mar 2024 19:15:56 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e1bc286708d437122f9c8cb14dfea3f434dfac989dce041e45a9b41092ad3f`  
		Last Modified: Mon, 25 Mar 2024 19:15:58 GMT  
		Size: 17.5 MB (17535963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d06f2c0a33c8c8619b80557f74f78945c30db4d3489b31a6749045b15b266f8b`  
		Last Modified: Mon, 25 Mar 2024 19:15:54 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f7a173888462c9728caaf817401ac7c248a3ae83bed02814f0e653caa8b157`  
		Last Modified: Mon, 25 Mar 2024 19:15:54 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293673c5a404d4bbeecb31d22491777f1ddc4ea8b62d4d4b63af556100a38f84`  
		Last Modified: Mon, 25 Mar 2024 19:15:54 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170ba1da534162f9cbd1542c220d6cb7433c9a4d8eeba11bb7781d9d88e0d9d3`  
		Last Modified: Mon, 25 Mar 2024 19:15:55 GMT  
		Size: 18.8 MB (18821597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de4c3b5bc3a6907cb225bb2863158cd765cf504b74b091e672a80e1b1e81e20`  
		Last Modified: Mon, 25 Mar 2024 19:15:52 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813d1ffa5817ef4aace50cb072288b7d955de846ab06091828971ef293630a8a`  
		Last Modified: Mon, 25 Mar 2024 19:15:52 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cfd156cda129465d99dc22de9f31fef506a33f68964428b6962fdcda2df71b9`  
		Last Modified: Mon, 25 Mar 2024 19:15:52 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fadd14a53853bf339974152ce00144d5b9b2cd946ec264417d97688965f13287`  
		Last Modified: Mon, 25 Mar 2024 19:15:55 GMT  
		Size: 19.5 MB (19524519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
