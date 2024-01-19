## `docker:rc-windowsservercore`

```console
$ docker pull docker@sha256:82011652182d4a82d2775c820dcb358608befe5a3c41bab4f6168684d206eaed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `docker:rc-windowsservercore` - windows version 10.0.20348.2227; amd64

```console
$ docker pull docker@sha256:e527892fcbe5d13c9175db2c2ad9133a89e41497048e77667a2e7209c7b19db1
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1955803085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c09721b4613fb65cfa2bb052d421000e993f4fc0d27eaa0d9eba045eaea261d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Thu, 18 Jan 2024 23:03:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 18 Jan 2024 23:04:37 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 18 Jan 2024 23:04:39 GMT
ENV DOCKER_VERSION=25.0.0-rc.3
# Thu, 18 Jan 2024 23:04:40 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-25.0.0-rc.3.zip
# Thu, 18 Jan 2024 23:04:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 18 Jan 2024 23:04:58 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Thu, 18 Jan 2024 23:04:59 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.windows-amd64.exe
# Thu, 18 Jan 2024 23:05:00 GMT
ENV DOCKER_BUILDX_SHA256=0ff0853a09960ff8f454d5db7253d5d935f5538856ea4985a276cbd1b28a96a5
# Thu, 18 Jan 2024 23:05:12 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 18 Jan 2024 23:05:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.1
# Thu, 18 Jan 2024 23:05:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-windows-x86_64.exe
# Thu, 18 Jan 2024 23:05:17 GMT
ENV DOCKER_COMPOSE_SHA256=6c94193c282d5fba71563c617fe8ddf8dce9355fb1d0ae93609221c590d06fcb
# Thu, 18 Jan 2024 23:05:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9593493ba8ab8e5478685915edea5f03c5783152d163152334ba622a558cd37`  
		Last Modified: Thu, 18 Jan 2024 23:05:33 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee59a2dd903d07e2061e8bf6edc9246311b32a63f423311b9ca0861c1d98ada`  
		Last Modified: Thu, 18 Jan 2024 23:05:32 GMT  
		Size: 485.8 KB (485794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:102ac1ec0b86e2abfff0c924cddb6e47855b41ddc1998df3da42f2974307b557`  
		Last Modified: Thu, 18 Jan 2024 23:05:31 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e6948e1d43811263a7c707b37c637823b2b1636ed940334c404a6a882b7135`  
		Last Modified: Thu, 18 Jan 2024 23:05:31 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b996b0de359c3dee8e5e6492fb174821cd841fd95def681d1c0e2486fa9570`  
		Last Modified: Thu, 18 Jan 2024 23:05:33 GMT  
		Size: 18.1 MB (18059493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2a77302dfa52bacb29e790fa35c9f48d5896f2ff5215072d95802a02f259d41`  
		Last Modified: Thu, 18 Jan 2024 23:05:30 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a847aff45562c3751e7be590291408b643ee697760c150f8a154d72963b97d`  
		Last Modified: Thu, 18 Jan 2024 23:05:30 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4cc67346b275101de6ee5e508cc4b918c177c7bea77a9e4c7b83fc905e6108e`  
		Last Modified: Thu, 18 Jan 2024 23:05:30 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14837a0cd3ceb8a5eb4fd2c713bab813ec317c065d26c37e2dbc7693400d26b2`  
		Last Modified: Thu, 18 Jan 2024 23:05:31 GMT  
		Size: 18.0 MB (18010730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53cbfb3979c9a8d4a183a3b323441d082600c9f3351d8a2d8032a78b746f3416`  
		Last Modified: Thu, 18 Jan 2024 23:05:29 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21577649c0145f7843b2965b486c34198454f0a57e708b31ba8a85c5ce8d4c8e`  
		Last Modified: Thu, 18 Jan 2024 23:05:29 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beedf8b767c970d70562e1e772535b1ca7543357cf2935ee576fddd2d2fd22f2`  
		Last Modified: Thu, 18 Jan 2024 23:05:29 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3448a701aadebe72d97499ead2406fcb7b49b2ab495b046cc5ffbe0bbc343b54`  
		Last Modified: Thu, 18 Jan 2024 23:05:32 GMT  
		Size: 19.0 MB (19022749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:rc-windowsservercore` - windows version 10.0.17763.5329; amd64

```console
$ docker pull docker@sha256:cdf6aa8c3435340c7c3c56d5714e66c23ea2e7f04c947565b6d8494d8ae361f2
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2125346611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d29d46783289fa8034fbb9aab9ac2bcba053cffa70393bd7f55c8d9b01e2f322`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 18 Jan 2024 23:03:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 18 Jan 2024 23:06:08 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 18 Jan 2024 23:06:08 GMT
ENV DOCKER_VERSION=25.0.0-rc.3
# Thu, 18 Jan 2024 23:06:09 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-25.0.0-rc.3.zip
# Thu, 18 Jan 2024 23:06:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 18 Jan 2024 23:06:44 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Thu, 18 Jan 2024 23:06:44 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.windows-amd64.exe
# Thu, 18 Jan 2024 23:06:45 GMT
ENV DOCKER_BUILDX_SHA256=0ff0853a09960ff8f454d5db7253d5d935f5538856ea4985a276cbd1b28a96a5
# Thu, 18 Jan 2024 23:07:13 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 18 Jan 2024 23:07:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.1
# Thu, 18 Jan 2024 23:07:14 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-windows-x86_64.exe
# Thu, 18 Jan 2024 23:07:15 GMT
ENV DOCKER_COMPOSE_SHA256=6c94193c282d5fba71563c617fe8ddf8dce9355fb1d0ae93609221c590d06fcb
# Thu, 18 Jan 2024 23:07:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e334d5c04f2ddc57fd2b06104cc3c7f01ac08d98323dc444ca98aaa7bec135`  
		Last Modified: Thu, 18 Jan 2024 23:07:44 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffa19a9c81bb3db49595f54eb9462305a0f502077b5003947a70b0b8c454364`  
		Last Modified: Thu, 18 Jan 2024 23:07:44 GMT  
		Size: 493.6 KB (493614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e3a95827dbfd7e9ea56bdf475af99d101bba62cbf1879052df633f320fda0c`  
		Last Modified: Thu, 18 Jan 2024 23:07:43 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322c270919c607ec4d553ef5830b727645ed292a41ca0be14f97812c9be3558c`  
		Last Modified: Thu, 18 Jan 2024 23:07:43 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a55c7fae2d7002fd706805844c1d02064ea7ba9416733ec64d49de452daf73`  
		Last Modified: Thu, 18 Jan 2024 23:07:45 GMT  
		Size: 18.1 MB (18071318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ca05c6e38bebcc7676f92c2615916e8366f09517d3e4f9ceb7477ac967f660`  
		Last Modified: Thu, 18 Jan 2024 23:07:42 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c203a4d0024709f588d0eb307e0a9c36d0c1d8bfee310026a85e0caf4ec3d4`  
		Last Modified: Thu, 18 Jan 2024 23:07:42 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ba8eb3d63a83f07907c942f087ad12ea83a0bed8eeec4a6c160824504632b3`  
		Last Modified: Thu, 18 Jan 2024 23:07:42 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bc0680dbc565956fc2748cafade8d008f364edc6cc6dd10a3012c5a08313b9a`  
		Last Modified: Thu, 18 Jan 2024 23:07:43 GMT  
		Size: 18.0 MB (18020224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff6dd61c0c68c58fec532897f357dc746a39938bc842eb3d37585b43b5eb350`  
		Last Modified: Thu, 18 Jan 2024 23:07:41 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c01d98e357060f1b82efb80bd5b2e8b99355656b064bb245f3cf09de7d10aba3`  
		Last Modified: Thu, 18 Jan 2024 23:07:41 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3dde7f901971e817a7c1f756e91e1f67742924499bb06b17755614c4254705`  
		Last Modified: Thu, 18 Jan 2024 23:07:41 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ae4dddef97660a6bc1279d3ac2b0d3c03b62348d8b71633e40ca74f66fcafe`  
		Last Modified: Thu, 18 Jan 2024 23:07:43 GMT  
		Size: 19.0 MB (19027227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
