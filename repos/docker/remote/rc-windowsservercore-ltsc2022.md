## `docker:rc-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:14cb84f08912640bf69720d1d19d6994ed61b365aa901690b86023563a4b118c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `docker:rc-windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

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
